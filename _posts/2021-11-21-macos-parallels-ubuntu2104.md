---
layout: post
title: "Parallels- Desktop auf dem Mac, Parallels-Tools einrichten"
author: Henriette Baum
---

Auf einem Mac lässt sich eine Virtuelle Umgebung mit einem anderen Betriebssystem besonders komfortabel einrichten. Erforderlich hierfür ist das Programm Parallels- Desktop. 

![bild: Mac, Parallels-Desktop Startfenster zum Erstellen einer neuen VM](/assets/images/parallels-tools/image-20211121233330707.png)

Damit der volle Funktionsumfang der Virtuellen Maschine (VM) zur Verfügung steht, benötigt man die Parallels- Tools, Sie sind vergleichbar mit den Gasterweiterungen von VirtualBox.

Nutzt man die von Parallels angebotene Option zum automatischen Erstellen einee neue VM mit einem der unter "Kostenlose Systeme"  vorgeschlagenen Betriebssysteme, werden auch die Parallels- Tools gleich mit eingerichtet.

Verwendet man ein eigenes ISO- Image, so  mössen die Parallels- Tools im Gast- Betriebssystem manuell installiert werden. 

Als Beispiel wird hier eine virtuelle Maschine mit dem Betriebssystem Ubuntu 21.04 erstellt.

Voraussetzungen:

- die ISO- Datei des gewünschten Betriebssystems herunterladen, hier also Ubuntu 21.04
- eine neue VM erstellen

Nach dem ersten Start der neuen VM erscheint in der oberen rechten Bildschirmecke ein kleines gelbes Warndreieck. Klickt man es an, erhält man einen Popup- Dialog "Parallels- Tools installieren", diesen anklicken.

![Ubuntu-Desktop mit Parallels- Menülieste und gelbem Hinweissymbol](/assets/images/parallels-tools/mac-parallels-ubuntu_01.png)

Ein Dialogfenster erläutert das weitere Vorgehen, man bestätigt mit "Fortfahren":

![bild: Ubuntu-Desktop mit Dialogfenster Parallels-Tools, Option Fortfahren](/assets/images/parallels-tools/mac-parallels-ubuntu_02.png)

Die Dateien mit den Tools werden als virtuelle CD in ein virtuelles CD- Luafwerk eingehängt. Anschließend findet man das entsprechende CD- Icon im Dock und auf dem Desktop. 

![bild: Ubuntu- Desktop mit Icon der eingelegten Parallels-Tools-CD](/assets/images/parallels-tools/mac-parallels-ubuntu_03.png)

Ein Doppelklicken öffnet sie Dateimanager:

![bild: Ubuntu- Dateimanager zeigt Dateien der Parallels-Tools-CD](/assets/images/parallels-tools/image-20211121230010924.png)

Nach Anklciken der Datei `install-gui`  öffnet sich eine Passwortabfrage, hier muss das root-Passwort des Gast- Betriebssystems eingegeben werden.  Ein Dialogfenster informiert über den Fortschritt der Installation:

![Dialogfenster mit Fortschrittsbalken während der Installation](/assets/images/parallels-tools/mac-parallels-ubuntu_05.png)

___

Hinweis: 

Kommt es zu einer Fehlermeldung, zunächst prüfen, ob die Datei ausführbar ist. Dazu die Datei mit der rechten Maustaste anklicken, um das Kontextmenü zu erreichen und über den Punkt "Eigenschaften" ->  "Zugriffsrechte"  bei "Datei als Programm ausführen" einen Haken setzen. 

![bild: Kontextmenü für Datei- Zugriffsrechte und Ausführbarkeit](/assets/images/parallels-tools/mac-parallels-ubuntu_04.png)

___

Alternativ kann man die Installation auch über das Terminal anstoßen, wie es oben im Dialog vorgeschlagen wird. Dazu ein neues Terminal am Ort der Parallels-Tools CD öffnen:

Am einfachsten geht dies, indem man das CD- Icon mit der rechten Maustaste anklickt und im Kontextmenü "im Terminal öffnen" auswählt.

![bild: ubuntu-desktop-mit-parallels-tools-cd-und-kontextmenü](/assets/images/parallels-tools/mac-parallels-ubuntu_07.png)

Im Terminal den Befehl `sudo ./install`  eingeben, dann wird auch hier das Passwort abgefragt, das Ubuntu- Passwort eingeben (es werden keine Punkte oder Sternchen beim Eintippen angezeigt, man sieht also bei der Passworteingabe keinerlei Reaktion des Cursors). Mit Enter bestätigen und fertig.

![bild: ubuntu terminal mit install-befehl](/assets/images/parallels-tools/mac-parallels-ubuntu_08.png)

Nach abgeschlossener Installation das Gast- Betriebssystem neu starten.

![bild: Dialogfenster mit Meldung über die erfolgreiche Installation der Tools](/assets/images/parallels-tools/mac-parallels-ubuntu_06.png)

Anschließend kann man standardmäßig auf das Home- Verzeichnis des Host-Betriebssystems (Mac) und auch auf ICloud vom Gast-Betriebssystem (Ubuntu) aus zugreifen.

![bild: Ubuntu Dateimanager mit gemeinsamen Ordnern](/assets/images/parallels-tools/mac-parallels-ubuntu_09.png)


Über das Parallels- Konfigurationsmenü  kann man aber festlegen, welche Rechte man dem Gast-Betriebssystem einräumen möchte:

![bild: Parallels- Einstellungsmenü für Freigabe von Verzeichnissen](/assets/images/parallels-tools/image-20211121232131197.png)
