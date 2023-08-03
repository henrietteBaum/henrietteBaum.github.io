---
layout: post
title: Wordpress unter macOS ausprobieren mit XAMPP 
author: Henriette Baum
tags: Wordpress, macOS, XAMPP
---



Mit XAMPP erhält man eine Kombination aus Apache-Web-Server und SQL-Datenbank. Beides ist Voraussetzung für das Betreiben einer lokalen Wordpress-Instanz auf dem eigenen Rechner. Die eignet sich gut, um neue Themen oder Plugins in Wordpress auszuprobieren und mit Einstellungen für Accessibility und bessere Lesbarkeit einer Webseite zu experimentieren.

Auf der Webseite des Herstellers werden XAMPP-Installationsprogramme für Windows, macOS und Linus bereitgestellt.

[Apache-Friends](https://www.apachefriends.org/de/index.html)

Nach dem Herunterladen wird der Installer mit Doppelklick gestartet. Hierfür muss die Installation eines fremden Programmes explizit in den Mac-Einstellungen unter Datenschutz und Sicherheit erlaubt werden.

Nach der Installation öffnet sich ein Kontrollzentrum, in dem man zunächst den Web-Server und die Datenbank startet.

![xampp Kontrollzentrum](/assets/images/2023-08-02-wp-xampp-mac/xampp-controlcenter.png)


Für die jeweiligen Betriebssysteme findet  man eine Sammlung von FAQ's unter:

[XAMPP FAQ macOS](https://www.apachefriends.org/de/faq_osx.html)

___



![Im Browser hier Safari - localhost aufrufen](/assets/images/2023-08-02-wp-xampp-mac/safari-xampp-startpage-localhost.png)



Über den Reiter `phpmyadmin` erreicht man die SQL-Datenbank. 

💡**Hinweis**: Um hier phpmyadmin starten zu können, muss zuvor der SQL-Server gestartet worden sein.



## Wordpress

Herunterladen: https://de.wordpress.org und entpacken .

Anschließend den Wordpress-Ordner in das Verzeichnis `htdocs` von XAMPP kopieren.

Ruft man nun im Browser die Seite

[localhost/wordpress](localhost/wordpress ) 

auf, gelangt man zur Startseite der Installation.

![Wordpress Startseite](/assets/images/2023-08-02-wp-xampp-mac/wp-install-start.png)



## Vorbereitung für diese Installation

1. eine neue Datenbank anlegen, hier als Beispiel `wordpress1`,  der Name ist frei wählbar, muss dann aber auch so in allen anderen Bereichen eingesetzt werden.
2. einen Benutzer für diese Datenbank anlegen und ein Passwort vergeben

Beides über phpmyadmin:

![phpmyadmin: neue Datenbank anlegen](/assets/images/2023-08-02-wp-xampp-mac/sql-create-new-db.png)



![phpmyadmin mit neuer Wordpress Datenbank wordpress1](/assets/images/2023-08-02-wp-xampp-mac/phpmyadmin-new-wp-daabase.png)



## Wordpress Installation

Startet man nun die eigentliche Installation mit "Los geht's", werden Datenbankname, Benutzername und Passwort abgefragt. Server und Präfix sind schon mit localhost und wp_ vorgegeben und können so bleiben.

Da die Installation an dieser Stelle keine Datei `wp-config` findet, erstellt die Installationsroutine den erforderlichen Inhalt, den man dann nur noch kopieren und als `wp-config.php`  im Wordpress-Verzeichnis, hier `wordpress1` speichern muss. 

Alternativ könnte man die bereits vorhandene Beispieldatei `wp-sample-config.php` duplizieren und umbenennen und deren Inhalt entsprechend anpassen.

Nachdem die Datei angelegt wurde, kann man die Installation fortsetzen und dann auch den Namen für die neue Website festlegen. Nach Abschluss wird man automatisch zur Anmeldung weitergeleitet.

![Wordpress-Backend nach der ersten Anmeldung](/assets/images/2023-08-02-wp-xampp-mac/safari-wp-startwindow.png)



## Updates und neue Themen installieren

Um Aktualisierungen und neue Themen installieren zu können, muss Wordpress auf die erforderlichen Ordner zugreifen können. Konkret muss das Verzeichnis: 

`Applications/XAMPP/xamppfiles/htdocs/` 

mit entsprechenden Benutzerrechten versehen werden[^1]. 


Ohne Terminal erreicht man die Einstellung für die Zugriffsrecht unter macOS mit einem Rechtsklick auf den Ordner > Informationen > Teilen & Zugriffsrechte. Nach dem Entsperren über das Schlosssymbol die Rechte für "everyone" auf "Lesen und Schreiben" setzen.

<center><img src="/assets/images/2023-08-02-wp-xampp-mac/finder-informatio-zugriffsrechte.png" alt="macOS Ordner- Zugriffsrechte" style="zoom: 33%;"/></center>

Erhält man von Wordpress die Fehlermeldung, auf das upgrade-Verzeichnis könne nicht zugegriffen werd, kann man das Verzeichnis `upgrade` selbst erstellen.



💡 **Hinweis**: Alle angesprochenen Ordner kann man schnell über den Menüpunkt Programme in der Seitenleiste erreichen. Dort findet man das Verzeichnis XAMPP, den Ort der Unterverzeichnisse ruft man von hier aus mit einem Rechtsklick und "Original zeigen" auf.



## Neustart

Um auf Wordpress nach einem Neustart des Rechners zugreifen zu können, muss auch XAMPP neu gestartet werden. Das App-Icon `manager-osx.app` für XAMPP erreicht man über das Launchpad oder über das Programm-Verzeichnis:

![Alt text](/assets/images/2023-08-02-wp-xampp-mac/max-launchpad-xampp.png)


![XAMPP neu starten](/assets/images/2023-08-02-wp-xampp-mac/finder-program-manager-osx-app.png)



## Fazit

Um in Wordpress neue Themen und Einstellungen auszuprobieren ist XAMPP sicherlich eine gute Wahl, weil man nicht selbst einen Web-Server und die erforderliche Datenbank aufsetzen muss. Alternativ hierzu bietet sich aber auch die Nutzung einer Komplettlösung von Bitnami: https://bitnami.com/stacks#wordpress ,  der Einsatz eines Docker-Containers  oder einer VM (Virtual Machine) an: https://bitnami.com/stack/wordpress/virtual-machine.


### Weiterlesen:

[Installation von XAMPP unter Windows bei hiese.online](https://www.heise.de/download/blog/Wordpress-mit-XAMPP-auf-dem-eigenen-Rechner-ausprobieren-3286703)

[YouTube Beitrag von Aroma Meia für die Einrichtung unter  macOS](https://www.youtube.com/watch?v=M6vgABWvCGU)

[YouTube Beitrag von Tom Media, Einrichtung unter macOS ](https://www.youtube.com/watch?v=UJ4YMxAFlz4&t=18s)
___



[^1]: Quelle: Stackoverflow: https://stackoverflow.com/questions/60165824/failed-to-connect-to-ftp-server-on-xampp-mac