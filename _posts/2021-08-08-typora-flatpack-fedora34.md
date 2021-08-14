---
layout: post
title: "Typora unter Fedora 34"
---


Typora ist ein sehr vielseitiger und an die persönlichen Bedürfnisse anpassbarer Markdown- Editor. Für Windows und MacOS gibt es einen Installer, für Ubuntu kann man Typora über die Softwareverwaltung installieren. Eine Version für Fedora gibt es leider nicht. Statt dessen kann man aber das entsprechende Flatpack  verwenden.  Diese Programmform findet man auf der Internetplattform Flathub:

![Typora-on-Flathub-image](/assets/images/Typora-Flatpack-Fedora34-images/typora-flatpack-fedora34_0.png)

Dazu muss zunächst Flathub als Softwarequelle unter Fedora eingerichtet werden. Eine Anleitung hierzu findet man hier:

[https://flatpak.org/setup/Fedora/](https://flatpak.org/setup/Fedora/)

![Typora-flatpack-Softwarequelle-einrichten-image](/assets/images/Typora-Flatpack-Fedora34-images/typora-flatpack-fedora34_1.png)

Der Klick auf den Button öffnet den Download- Dialog. Bereits vorgewählt ist "Öffnen" und man kommt zur regulären Installation der Software.

![Typora-Flatpack-Download-image](/assets/images/Typora-Flatpack-Fedora34-images/typora-flatpack-fedora34_2.png)

Nach dem erneuten Starten der Fedora- Softwareverwaltung werden die Metadaten von Flathub eingelesen und  `flathub`  ist als Softwarequelle aktiviert.

![Typora-Fedora-Softwarequelle-flatpack-image](/assets/images/Typora-Flatpack-Fedora34-images/typora-flatpack-fedora34_3.png)

Hinweis die Übersicht über die vorhandenen Softwarequellen erreicht man über das Hamburger- Menü oben rechts.

Anschließend kann man alle auf FlatHub angebotenen Pakete über die Softwareverwaltung von Fedora installieren:

![Typora-flatpack-installieren-image](/assets/images/Typora-Flatpack-Fedora34-images/typora-flatpack-fedora34_4.png)

Die Installation eines Flatpack dauert etwas länger, als die Installation von rpm- Paketen.

Nach der Installation lässt sich das Aussehen von Typora sehr einfach durch die Auswahl eines Themes anpassen. Zusätzliche Themes können installiert werden. Auf der Website von Typora findet man diese direkt  unter dem Menüpunkt Themes. Von dort aus wird man zum Download von der jeweiligen Themen- Website weitergeleitet.

![Typora-Themes-Website-image](/assets/images/Typora-Flatpack-Fedora34-images/typora-flatpack-fedora34_5.png)

Mein persönlicher Favorit ist das Thema "Nord", das mit angenehmen dunkelen aber nicht zu dunklen Grautönen eine gute Lesbarkeit bietet.

Nach Download und Entpacken die css- Datei und den Ordner "nord" in die Zwischenablage kopieren.

![Typora-Files-for-Theme-Nord-image](/assets/images/Typora-Flatpack-Fedora34-images/typora-flatpack-fedora34_6.png)

Nun kann man in der Einstellungsverwaltung von Typora über den Menüpunkt "Aussehen" den Themenordner öffnen und dort dann css- Datei und Ordner "nord" aus der Zwischenablage wieder einfügen.

![Typora-Settings-open-themefolder-image](/assets/images/Typora-Flatpack-Fedora34-images/typora-flatpack-fedora34_7.png)

Nach dem Neustart von Typora steht das neue Thema unter dem Menüpunkt Themes zur Verfügung:

![Typora-menubar-themes-image](/assets/images/Typora-Flatpack-Fedora34-images/typora-flatpack-fedora34_8.png)

## Markdown

Nicht nur für Menschen mit Augenproblemen ist das Schreiben von Texten mit Hilfe von Markdown- Syntax eine sehr komfortable Vorgehensweise. Die Syntaxregeln für einen normalen Text sind schnell erlernt, unter dem Menüpunkt "Hilfe"  findet man eine Referenz. Markdown erspart die Suche nach Schaltflächen oder im Menüband. Man kann einfach mit dem Curser im Text bleiben und eben nur Schreiben. Auch ist der dunkle Hintergrund im Editor meist angenehmer für die Augen als die weiße Seite in einem Textverarbeitungsprogramm.