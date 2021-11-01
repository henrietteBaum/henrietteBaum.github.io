---
layout: post
title: "Gasterweiterung für eine VM mit Ubuntu einrichten"
author: Henriette Baum
---


Einige Funktionen der VirtualBox stehen erst zur Verfügung, wenn die Gasterweiterungen eingerichtet sind. Erst dann kann man z.B. das Audiosystem des Host- Betriebssystems und damit die Sprachausgabe des Gast-Betriebssystems nutzen, eine gemeinsame Zwischenablage und gemeinsame Ordner können verwendet werden.

Als Beispiel dient hier eine Virtuelle Maschine mit Ubuntu 21.04 (Gast- Betriebssystem) auf einem Windows 11 Host- Betriebssystem.  

## Gasterweiterungen einlegen

Die Gasterweiterungen sind eine Zusammenstellung von Programmpaketen, die in einer virtuellen CD zusammengefasst sind, daher auch die Bezeichnung "einlegen". Sie werden also in das virtuelle CD- Laufwerk der virtuellen Maschine eingelegt.

Dazu öffnet man die Systemeinstellungen von VirtualBox, dort den Menüpunkt "Geräte" -> "Gasterweiterungen einlegen ". 



![insert-guestadd](/assets/images/vbox-win-ubuntu-guestext/insert-guestadd.png)

___

Hinweis:

Manchmal werden nicht alle Menüpunkte angezeigt, der Menüpunkt "Geräte" fehlt. Über den Menüpunkt "Anzeige" -> "Menüleiste" ist einstellbar, welche Menüpunkte angezeigt werden.

![vbox-menu-settings](/assets/images/vbox-win-ubuntu-guestext/vbox-menu-settings.png)

___

## Installation auf dem Gastbetriebssystem:

Sind die Gasterweiterungen eingelegt, erscheint das CD- Symbol im Dock und im Dateiexplorer von Ubuntu:

![additions-run](/assets/images/vbox-win-ubuntu-guestext/additions-run.png)

Über die Schaltfläche "Anwendung starten" kann man nun das Installations- Skript "VBoxLinuxAddition.run" starten. Zunächst erscheint ein Warnhinweis für ausführbare Dateien und eine Passwortabfrage. Anschließend öffnet sich ein Terminal, wo die einzelnen Installationsschritte verfolgt werden können.

## Voraussetzungen für die Installation

Um die Erweiterung auf dem Gastsystem installieren zu können, müssen bestimmte Programme, wie der Compiler gcc dort bereits vorhanden sein. Die hat Ubuntu standardmäßig nicht an bord. Fehlen diese erhält man nach dem Start des Installations- Skripts eine Fehlermeldung im Terminal:

![ubuntu-terminal-missing-tool](/assets/images/vbox-win-ubuntu-guestext/ubuntu-terminal-missing-tool.png)

Mit dem Paket `build-essential` richtet man alle erforderlichen Werkzeuge und Abhängigkeiten ein. Im Terminal:

```bash
sudo apt update
sudo apt install build-essential
```

Die erfolgreiche Installation überprüfen mit den Befehlen im Terminal:

```bash
gcc --version
make --version
```



![ubuntu-terminal-buildtoll-test](/assets/images/vbox-win-ubuntu-guestext/ubuntu-terminal-buildtoll-test.png)

Anschließend die VM neu starten.

___

War die Installation der Gasterweiterungen muss die VM neu gestartet werden.

![ubuntu-terminal-ga-installed-restart](/assets/images/vbox-win-ubuntu-guestext/ubuntu-terminal-ga-installed-restart-16357294628191.png)

War die Installation erfolgreich,  stehen Anzeigeeinstellungen wie Vollbild- oder Skalierter Modus zur Verfügung, Audioeinstellungen des Gast- Betriebssystems, gemeinsame Zwischenablage oder gemeinsame Ordner.

Allerdings muss in den Grundeinstellungen von VirtualBox ausgewählt werden, welche Geräte genutzt werden dürfen. Die erreicht man über das gelbe Zahnradsymbol: "Ändern" im VirtualBox Manager. 

![vm-change-settings](/assets/images/vbox-win-ubuntu-guestext/vm-change-settings.png)

Über den Menüpunkt "Benutzerschnittstelle" -> "Geräte" kann dann bestimmt werden, welche der Geräte der VM grundsätzlich zur Verfügung stehen sollen. Dies ist aber noch nicht die tatsächliche Einrichtung des Geräts!

![image-vm-userinterface](/assets/images/vbox-win-ubuntu-guestext/image-20211101023839812.png)



## Gemeinsame Zwischenablage

Je nach Einstellung können über die gemeinsame Zwischenablage Bilder oder allgemein Dateien vom Gast- zum Host- Betriebssystem und umgekehrt (bidirektional) kopiert werden.

![image-vm-zwischenablage](/assets/images/vbox-win-ubuntu-guestext/image-20211101022429985.png)



## Gemeinsame Ordner

Ebenfalls über das Menü "Geräte" kann man Ordner für die gemeinsame Nutzung mit dem Host- Betriebssystem bestimmen.

![ga-shared-folders](/assets/images/vbox-win-ubuntu-guestext/ga-shared-folders.png)

Die Ordner des Host- Betriebssystems werden unter Ubuntu üblicherweise in das Verzeichnis `/media` eingehängt. 

![image-ga-schared-folder](/assets/images/vbox-win-ubuntu-guestext/image-20211101030802442.png)

Auf das eingehängte Verzeichnis hat aber der normale Nutzer keinen Zugriff, wenn er nicht der Gruppe  `vboxsf` angehört. Den Benutzer dieser Gruppe hinzuzufügen über das Terminal:

```bash
sudo usermod -a -G vboxsf $USER
```

Anschließend die VM neu starten, danach ist der Zugriff möglich.

## Fazit

Mit den Gasterweiterungen und insbesondere im Vollbildmodus lässt sich eine VM nutzen, wie ein "richtiger" Computer. Der Bildschirm kann skaliert werden und auch der Bildschirmleser funktioniert.

Quellen und weiterführende Informationen:

[techadmin.net](https://tecadmin.net/install-development-tools-on-ubuntu/)

[pragmaticlinux.com](https://www.pragmaticlinux.com/2021/02/how-to-mount-a-shared-folder-in-virtualbox/)

