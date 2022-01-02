---
layout: post
title: "Foliate - Ebooks lesen unter Linux"
author: Henriette Baum
---


Foliate ist aktuell das einzige Programm unter Fedora, mit dem man Ebooks im epub- Format lesen kann und das auch die Möglichkeit bietet, den Text vorlesen zu lassen. Auch ist die Bedienoberfläche für den Bildschirmleser zugänglich, die Schaltflächen sind beschriftet.

Das Programm steht über die Gnome- Softwareverwaltung als Flatpack bzw. als Snap -Pack zur Verfügung.

![image-fedora gnome-software: install foliate](/assets/images/foliate-fedora-35/image-20211229230708083.png)

Beim Öffnen des Programms wird zunächst die leere Bibliothek angezeigt. Man kann nun über die beiden Optionen

- Datei öffnen oder
- Kataloge durchsuchen

eigene Ebooks oder Bücher aus Online- Portalen zu seiner Bibliothek hinzufügen.

![image-foliate-start, Datei oder Katalog öffnen](/assets/images/foliate-fedora-35/image-20211229231802182.png)

## Ebook- Datei öffnen

Die Schaltfläche `Datei öffnen`führt zum Datei- Explorer des Betriebssystems:

![image-fedora-dateien](/assets/images/foliate-fedora-35/image-20211229235617693.png)

Nach der Auswahl einer Datei wird das Buchcover präsentiert und man kann unmittelbar mit dem Lesen beginnen.

![image-foliate mit geöffnetem Ebook](/assets/images/foliate-fedora-35/image-20211229232618430.png)

Durch Überfahren mit der Maus wird die obere Menüleiste sichtbar, durch Drücken der **alt**- Taste werden obere Menüleiste und die untere Leiste mit einer Anzeige für den Lesefortschrit sichtbar.

![image-foliate-menüleiste](/assets/images/foliate-fedora-35/image-20211229234424153.png)

Mit der Schaltfläche links oben öffnet man das Inhaltsverzeichnis des Buches, mit dem Hamburger- Menü rechts das Programm- Menü.



## Bücher aus einem Online- Portal

Über die Schaltfläche `Katalog durchsuchen` lassen sich Bücher aus Online-Portalen zur Bibliothek hinzufügen. Angeboten werden hier bereits Bücher aus den Portalen 

- Standard Ebooks
- Freebooks
- Projekt Gutenberg

Über das `+` - Symbol oben links lassen sich weitere Kataloge hinzufügen.

![image-foliate-kataloge](/assets/images/foliate-fedora-35/image-20211229234944630.png)

Von hier aus können Bücher auf den PC herunterladen werden. Das Beispiel zeigt eine Downloadoption von Projekt Gutenberg.

![image-foliate-katalog-download](/assets/images/foliate-fedora-35/image-20211230001319560.png)



Alle Bücher die einmal hinzugefügt wurden, egal ob als Datei oder aus einem Katalog, findet man über die Ansicht **Bibliothek**. Dabei werden die Bücher nach dem jeweils letztn Zugriff sortiert,  das zuletzt gelesene Buch wird also an erster Stelle angezeigt. Die Darstellung lässt sich umschalten zwischen Cover- und Listenansicht.

## Buchtext lesen

Für das Blättern im Buch stehen mehrere Wege zur Verfügung:

- mit der Maus in das Fenster klicken
- mit Pfeiltaste rechts `->` oder links zurück
- mit Pfeil-hoch oder Pfeil-runter
- auf dem Touchpad mit einer Zwei-Finger- Wischgeste

Sehr nützlich ist die Funktion zum Vergrößern des Buchtextes mit der Tastenkombination `Strg` + `+` bzw. Verkleinern mit `Strg`+ `-` . 

Markiert man einen Absatz im Text (durch Doppelklick) stehen weitere Optionen, wie u.a. Markieren für Anmerkungen, Nachschlagen und vor allem auch Vorlesen  zur Verfügung:

![image-foliate-kontext](/assets/images/foliate-fedora-35/image-20211230023520546.png)

Über das Stiftsymbol markiert man den ausgewählten Text, die Farbe hierfür ist wählbar und eigene **Anmerkungen** können hinzugefügt werden:

![image-foliate-anmerkungen](/assets/images/foliate-fedora-35/image-20211230024010202.png)

Die Anmerkungen lassen sich später über den Menüpunkt `Buch` in verschiedenen Formaten exportieren.

![image-foliate-anmerkungen-exportieren](/assets/images/foliate-fedora-35/image-20211230024758271.png)

Ausgewählten Text kann man direkt in zahlreiche Sprachen übersetzen lassen:

![image-foliate-text-übersetzen](/assets/images/foliate-fedora-35/image-20211230032036638.png)



Auch die **farbliche Darstellung** lässt sich über vorgefertigte Themen ändern. Die Themen selbst kann man auch noch an die eigenen Vorlieben anpassen.

Zusätzlich kann man mit der Taste `F5` die **Vorlesefunktion** starten und stoppen. Dazu muss zunächst in den Einstellungen die verwendete Sprachausgabe festgelegt werden.

## Tastenkombinationen

Einen Überblick über alle Tastenkombinationen findet man über das Menü -> Tastenkürzel für die Bereiche 

- Bibliothek
- Reader
- Bildbetrachter

![image-foliate-tastenkürzel](/assets/images/foliate-fedora-35/image-20211230031223069.png)

## Anpassen über das Einstellungsmenü

Foliate bietet vielfältige und praktische Einstellungsmöglichkeiten, um das Programm an die eigenen Vorlieben anzupassen.

![image-foliate-menü-einstellungen](/assets/images/foliate-fedora-35/image-20211230004546785.png)

### Sprachausgabe

Über den Menüpunkt `Text-zu-Sprache Befehl` wird die Vorlesefunktion konfiguriert. Auf den meisten Linux- Distributionen ist bereits `espeak` vorhanden, weil der Bildschirmleser Orca diese verwendet. 

![image-foliate-text-zu-sprache-konfiguration](/assets/images/foliate-fedora-35/image-20211230005644324.png)

Mit der Auswahl von `eSpeak NG` lässt sich ohne zusätzliche Installation die Vorlesefunktion konfigurieren.

Welche Stimme verwendet wird, legt man über die Einstellungen von Orca direkt fest. Diese erreicht man über die Tastenkombination `Einf` + `Leertaste` (die Einf- Taste des Nummernblocks, bei ausgeschaltetem Nummernblock) oder über ein Terminal mit dem Befehl `orca -s` .

![image-fedora-bildschirmlese-einstellungen](/assets/images/foliate-fedora-35/image-20211230010901775.png)



### Farbanpassungen

Im Menüpunkt `Themen` kann man die Farbdarstellung des Buchtextes anpassen.

![image-foliate-menü](/assets/images/foliate-fedora-35/image-20211230011541651.png)

Die nachstehende Abbildung zeigt  das Thema `Invertiert` .

![image-foliate-thema-invertiert](/assets/images/foliate-fedora-35/image-20211230011943328.png)

Je nach ausgewähltem Buch und Farb- Thema kann es vorkommen, das der Text schlecht lesbar  dargestellt wird oder gar nicht zu sehen ist.  Nachstehende Abbildung zeigt das Thema "Grovbox (dunkel)".

![image-foliate-thema-grovbox](/assets/images/foliate-fedora-35/image-20211230012345816.png)



Abhilfe schafft die Umstellung der Darstellung auf `invertiert` , zu erreichen über Thema -> Benutzerdefiniertes Thema hinzufügen...

Dort vergibt man zunächst einen neuen Namen für das Thema, z.B. `myNord` und kann dann eigene Anpassungen am Thema vornehmen.

![image-foliate-benutzerdefiniertes-thema](/assets/images/foliate-fedora-35/image-20211230013232992.png)

Nun ist der Text wieder gut sichtbar

![image-foliate-theme-grovbox-dark-invertierte-darstellung](/assets/image-20220102121551765.png)

 Hier mit dem Thema Nord und invertierter Darstellung:

![image-20211230013458283](/assets/images/foliate-fedora-35/image-20211230013458283.png)



## Seitendarstellung

Insbesondere wenn man die Textgräße stark erhöht, empfiehlt es sich, die Seitendarstellung auf `fortlaufend` umzustellen. Diese Option ermöglicht es, den Text jeweils um nur eine Zeile statt um eine Seite oder Seitenabschnitt weiter zu schieben. Das ist z.B. für Codebeispiele im Text sehr nützlich.

 Foliate wechselt den Darstellungsmodus aber auch selbständig, wenn man einen bestimmten Zoomfaktor überschreitet.

![image-foliate-einspaltige-darstellung](/assets/images/foliate-fedora-35/image-20211230015441130.png)

Der Menüpunkt `Erweitert` bietet hier mehrere Optionen an.

![image-foliate-menü-erweitert](/assets/images/foliate-fedora-35/image-20211230014418946.png)

## Schrift und Helligkeit

Direkt im Hauptmenü findet man einen Schieber für die Anpassung der Helligkeit und eine Auswahl von Schriften:

![image-20211230015110995](/assets/images/foliate-fedora-35/image-20211230015110995.png)

## Text mit Codebeispielen

Möchte man Ebooks lesen, deren Text Codebeispiele enthält, ist oftmals die Darstellung in der Verlagsschriftart besser lesbar.  Zu finden ist diese Option über das Menü `Erweitert -> Text` .   Das Codebeispiel wird dann in Relation zum Haupttext in einigen Büchern besser vergrößert.

![image-foliate-text-mit-code](/assets/images/foliate-fedora-35/image-20211230020338728.png)

![image-foliate-text-code-vergrößert](/assets/images/foliate-fedora-35/image-20211230021058008.png)

Die Darstellung kann sich aber je nach Buch unterscheiden.



## Fazit

Foliate ist ein gut durchdachter, gut zu bedienender und sehr vielseitig anpassbarer Ebook- Reader. Aktuell ist es das einzige Ebook- Programm unter Linux, das auch für Menschen mit Augenproblemen gut geeignet ist. Die Programmoberfläche ist für den Bildschirmleser Orca zugänglich, der Buchtext selbst allerdings leider nicht. Dafür steht aber eine eingebaute Vorlesefunktion zur Verfügung. 

Die Themen- und Farbauswahl für die Textdarstellung lassen kaum Wünsche offen. 

Markierungen und exportierbare Anmerkungen ermöglichen das Arbeiten mit Texten und Lehrbüchern. Der eingebaute Übersetzer hilft bei fremdsprachigen Texten.

Über die komfortable Bibliothek behält man den Überblick über die gelesenen Bücher und den Lesefortschritt.

Foliate ist eine Empfehlung für alle, die Ebooks am Computer lesen möchten oder müssen.

[Foliate - Website](https://johnfactotum.github.io/foliate/)

![image-foliate-mitwirkende](/assets/images/foliate-fedora-35/image-20211230033740444.png)
