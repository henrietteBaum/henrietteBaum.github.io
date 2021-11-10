---
layout: post
title: "Fedora 35 in einer Virtuellen Maschine unter Windows 11"
author: Henriette Baum
---
Wer Linux ausprobieren möchte, kann dies in einer Virtuellen Maschine tun, ohne damit das Betriebssystem des eigenen Rechners in Gefahr zu bringen. 

Auch ist Linux eine echte Alternative für Rechner, auf denen Windows 11 nicht mehr installiert werden kann.  Im nachstehenden Artikel wird Schritt für Schritt die Installation von **Fedora 35 - Workstation** in einer Oracle Virtual Box erklärt.  

Stand Fedora früher in dem Ruf, nur für erfahrene Linux- Anwender geeignet zu sein, ist es inzwischen  ähnlich komfortabel zu bedienen wie andere gängige Linux- Distributionen oder Windows. Manches funktioniert hier sogar besser als unter Windows. Fedora Workstation nutzt den aktuellen Gnome- Desktop. Damit sind alle alltäglichen Funktionen über die grafische Benutzeroberfläche zu erreichen. 



Voraussetzungen: 

- ein Windows Rechner mit bereits installierter Software Oracle Virtual Box:  aktuell die Version 6.1.22 Base-Pack und das Extension Pack, [Oracle](https://www.oracle.com/de/virtualization/technologies/vm/downloads/virtualbox-downloads.html)
- eine ISO-Image Datei von Fedora 35:  [getfedora.org](https://getfedora.org/de/workstation/download/)



Zunächst wird nun also eine leere Virtuelle Maschine (VM) eingerichtet und anschließend darin Fedora installiert.

# Die VM einrichten

Eine Anleitung zum Einrichten der VM findet sich hier:

[VM mit Ubuntu](https://henriettebaum.github.io/vm/2021/07/23/win-vbox-ubuntu.html)

Die grundlegenden Schritte zum erstellen der VM sind unabhängig vom später installierten Betriebssystem erst einmal gleich.

![vm-fedora35-start_01](/assets/images/vm-fedora35/vm-fedora35-start_01.png)

Nun kann man die neue leere VM starten.

## Fedora installieren

Nach dem Start erhält man eine Auswahl "Fedora ausprobieren" oder "Fedora installieren".  Die Installation beginnt mit drei Auswahloptionen:

![vm-fedora35-install_03](/assets/images/vm-fedora35/vm-fedora35-install_03.png)

In der Regel ist der Punkt "Installations- Ziel rot oder orange markiert. Das weist darauf hin, dass noch kein Ziel ausgewählt wurde. Durch Anklicken gelangt man in das nächste Fenster:

![vm-fedora35-install_04](/assets/images/vm-fedora35/vm-fedora35-install_04.png)

Klickt man das unter lokale Speichermedien aufgeführte Icon (hier ATA VBOX...) mit der Maus an, wird ein Haken gesetzt und das Speichermedium ist als Installationsziel ausgewählt. Die Auswahl mit der  nun blauen Schaltfläche "Fertig" bestätigen und man gelangt zurück zum Installationsstart. Dort ist jetzt die Schaltfläche "Installieren" blau hinterlegt, ggf. noch die Lokalisierung anpassen. 

Nach dem Start informiert eine Fortschrittsanzeige über das aktuelle Geschehen:

![vm-fedora35-install-progress_05](/assets/images/vm-fedora35/vm-fedora35-install-progress_05.png)

Nach erfolgreicher Installation muss die VM neu gestartet werden. Dazu nicht die Option "Restart..." verwenden, sonst wird nur die virtuelle Installations- CD erneut gestartet. Statt dessen Fedora herunterfahren mit "Power off".

![vm-fedora35-install-restart_06](/assets/images/vm-fedora35/vm-fedora35-install-restart_06.png)

Nach dem Herunterfahren von Fedora muss man die virtuelle Installations-CD auswerfen. Man findet sie im VirtualBox Manager unter dem Punkt "Massenspeicher - Optisches Laufwerk".  Durch Anklicken öffnet man das Kontextmenü und kann dort das Medium entfernen.

![vm-fedora35-optical-medium_07](/assets/images/vm-fedora35/vm-fedora35-optical-medium_07.png)



Startet man nun über den grünen Pfeil die VM, gelangt man in eine ganz normales, installiertes Betriebssystem, das sich fast nicht von einem echten (Hardware-) Rechner unterscheidet. 

### Weiterführende Informationen:
Eines von zahlreichen Video- Tutorials gibt es auf [YouTube](https://www.youtube.com/watch?v=cuh_K2fCbxw), allerdings für Fedora 34, die Schritte sind aber identisch.

## Einrichtungsassistent

![vm-fedora35-first-start_08](/assets/images/vm-fedora35/vm-fedora35-first-start_08.png)

Der Fedora- Einrichtungsassistent führt den Benutzer durch verschiedene Einstellungsmöglichkeiten. Unter anderem die Möglichkeit Drittanbieterquellen einzubinden, das beinhaltet auch Treiber und sollte normalerweise aktiviert werden. Auch Benutzername und Passwort werden hier vergeben.

Eine geführte Tour durch den Gnome- Desktop erklärt das grundlegende Bedienungskonzept.

![vm-fedora35-gnome-wellcome_09](/assets/images/vm-fedora35/vm-fedora35-gnome-wellcome_09.png)

Klickt man auf "Nein danke" sitzt man anschließend vor einem leeren Desktop  ohne die von Windows gewohnten unzähligen Programm- Icons und wundert sich.  Ein Druck auf die Windows- Taste bringt das Dock und die Arbeitsflächenübersicht zum Vorschein. Über die gepunktete Schaltfläche ganz rechts erreicht man die übrigen Programme.



![vm-fedora35-dock_13](/assets/images/vm-fedora35/vm-fedora35-dock_13.png)

Für bessere Lesbarkeit empfiehlt es sich, in den Vollbildmodus umzuschalten, zu erreichen über den Menüpunkt "Anzeige" oder kürzer mit der Tastenkombination `rechte Strg-Taste + F` , mit der man dann auch wieder zurück wechseln kann. Die rechte `Strg` - Taste wird auch als "Host"- Taste bezeichnet.

![vm-fedora35-fullscreen_10](/assets/images/vm-fedora35/vm-fedora35-fullscreen_10.png)

Wer die Knöpfe in der oberen Fensterleiste vermisst: die Fenstergröße und weitere Optionen findet man durch einen Rechtsklick auf die Fensterleiste. Sie lassen sich aber auch mit dem Tool "Gnome- Optimierungen" nachrüsten.



## Update

Und zu guter Letzt - aber extrem wichtig: auf Updates prüfen. Hinter dem Einkaufstaschen- Symbol im Dock verbirgt sich die Softwareverwaltung, die entsprechend der Voreinstellung automatisch auf Updates prüft aber nach einer Neuinstallation besser selbst angestoßen werden sollte. 

![vm-fedora35-software-update](/assets/images/vm-fedora35/vm-fedora35-software-update_14.png)

Die Update- Einstellungen selbst findet man über das Hamburger- Menü oben rechts.

Jetzt steht dem Ausprobieren nichts mehr im Wege. War man zu mutig und hat das System "zerschossen", ist die VM schnell gelöscht und auch schnell eine Neue eingerichtet. Reagiert Fedora nicht mehr, lässt sich die VM über den Menüpunkt "Maschine - Ausschalten per ACPI"  oder die Tastenkombination `rechte Strg-Taste + H` abschalten. 

