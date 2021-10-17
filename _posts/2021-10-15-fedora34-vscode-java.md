---
layout: post
title: "Java mit Fedora 34 und Visual Studio Code"
author: Henriette Baum
---


Vorbereitungen:

- Visual Studio Code und die erforderlichen Erweiterungen Installieren

- Java auf dem Betriebssystem einrichten

Unter Fedora kann man Visual Studio Code nicht einfach über die Softwareverwaltung installieren. 

Auf der Herstellerseite erhält man jedoch ein Skript, mit dem das rpm- Paket über die Kommandozeile installiert und auch die Softwarequelle hinzugefügt wird: 

https://code.visualstudio.com/docs/setup/linux

Um Java-Programme mit VSCode  zu erstellen, installiert man zunächst das Erweiterungspaket "Extension Pack for Java", das alle nötigen Werkzeuge mitbringt:

![image-vscode-java-extension-pack](/assets/images/fedora-34-java/14_vscode-java-extension-pack.png)

Nach dem Neustart von VSCode wird ein Fenster mit den auf dem Betriebssystem vorhandenen Java- Versionen angezeigt. Wird keine verwendbare Version gefunden, erhält man einen Vorschlag zum Download.

![04_vscode-java-download](/assets/images/fedora-34-java/04_vscode-java-download.png)

Unter Fedora kann man Java aber einfacher über die relativ aktuellen Paketquellen installieren. Genauer: benötigt wird das JDK oder Java Development Kit. Dies ist eine Implementierung der Java Environment, Standard Edition und ist Voraussetzung für die Java-Entwicklung. Die Open Source Version ist das openJDK 

Dazu öffnet man das Terminal und lässt sich mit dem Befehl

`dnf search openjdk` 

zunächst die zur Verfügung stehenden Versionen anzeigen.

![01_bash-openjdk-version](/assets/images/fedora-34-java/01_bash-openjdk-version.png)

In der Abbildung oben ist die Version, die wir installieren wollen markiert. Installiert wird dann mit:

`sudo dnf install java-latest-openjdk-devel.x86_64 `  

![03_bash-install-openjdk](/assets/images/fedora-34-java/03_bash-install-openjdk.png)



Damit die Java- Installation und der Compiler (javac) auch gefunden werden, muss man zusätzlich noch die Umgebungsvariablen  `JAVA_HOME` und `PATH` setzen.  Dazu werden in der Datei `.bashrc` zwei Zeilen eingefügt. Die Datei befindet sich im Home- Verzeichnis (Persönlicher Ordner).  Damit sie angezeigt wird, muss das Häckchen bei "verborgene Dateien anzeigen " gesetzt sein. 

  ![10_nemo-show-hidden-files](/assets/images/fedora-34-java/10_nemo-show-hidden-files.png)

Die Datei .bashrc wurde in der nachstehenden Abbildung mit dem Editor "gedit" geöffnet. 

![12_bashrc-java-settings](/assets/images/fedora-34-java/12_bashrc-java-settings.png)

Die beiden Zeilen am Textende (hier die Zeilen 29 und 31) ergänzen und anschlißend speichern.

___

**Hinweis**: 

Sind mehrere Java- Versionen auf dem Betriebssystem vorhanden, trifft man zunächst eine Auswahl im Terminal:

`sudo alternatives -config java` 

![08_bash-select-java-version](/assets/images/fedora-34-java/08_bash-select-java-version.png)

Im Beispiel oben stellt man also durch Eingabe von `2` auf Version 17 um.

___

Hat alles funktioniert, kann man dies im Terminal überprüfen mit den Befehlen: 

```bash
echo $JAVA_HOME
echo $PATH
```

![13_bash_echo](/assets/images/fedora-34-java/13_bash_echo.png)



Beim erneuten Öffnen von VSCode werden die  gefundenen openJDK- Versionen angezeigt:

![05_vscode-installed-jdk](/assets/images/fedora-34-java/05_vscode-installed-jdk.png)

Zum ersten Ausprobieren legt man am Besten einen separaten Ordner an (über das Menü "Datei" oder das Ordnersymbol in der linken Seitenleiste). Anschließend kann man eine java-Datei erstellen und direkt aus VSCode heraus ausführen.

![06_vscode-run-java](/assets/images/fedora-34-java/06_vscode-run-java.png)

Das Ergebnis wird in der integrierten Konsole angezeigt:

![07_vscode-terminal-java](/assets/images/fedora-34-java/07_vscode-terminal-java.png)



Ein detaillierte Anleitung zum Einrichten von Java findet sich unter:

https://computingforgeeks.com/how-to-set-java_home-on-centos-fedora-rhel/

JDK Versionen:

https://fedoraproject.org/wiki/JDK_on_Fedora#OpenJDK_and_project_IcedTea







