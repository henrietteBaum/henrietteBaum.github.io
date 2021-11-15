---
layout: post
title: "Das Terminal anpassen für bessere Lesbarkeit"
author: Henriette Baum
---
Auch das Terminal - die Konsole - lässt sich für bessere Lesbarkeit anpassen. Dies ist auf allen Betriebssystemen möglich. Beispielhaft wird hier die Anpassung der Bash, des Standard- Terminals unter Ubuntu 20.04 gezeigt.

Während der aktuellen Verwendung kann man die Schriftgröße mit der hierfür für viele Programme gleichen Tastenkombination `Strg` + `+` erhöhen und entsprechend mit ` Strg` + `-` wieder verringern.

Dauerhafte Änderungen führt man über die Einstellungen durch. Diese sind über das Hamburger-Menü oben rechts zu erreichen. 

![image-ubuntu-terminal-menu](/assets/images/terminal-settings/image-20211115013118752.png)

Hier kann man unter dem Menüpunkt "Profile" nicht nur die Schriftgröße, sondern unter anderem auch die angezeigte Fenstergröße oder das Farbschema festlegen.

Schrift und Fenstergröße:

![image-terminal-settings-profile](/assets/images/terminal-settings/image-20211115012900836.png)

Farbschema:

![image-terminal-settings-color-scheme](/assets/images/terminal-settings/image-20211115012158190.png)

Die geänderten Einstellungen werden beim Schließen der Einstellungsverwaltung automatisch unter dem Profil "Unbenannt" gespeichert. Man kann einen eigenen Namen für das Profil verwenden und dann auch mehrere verschiedene Profile erstellen.

![image-20211115012626492](/assets/images/terminal-settings/image-20211115012626492.png)

## Prompt

Standardmäßig enthält der Prompt den Benutzernamen und den Hostnamen, getrennt durch ein `@` - Zeichen. Beim Wechsel in andere Verzeichnisse wird der vollständige Pfad daran angehängt, was insbesondere bei einer erhöhten Schriftgröße schon mal die ganze Zeile einnehmen kann. 

![image-bash-prompt-standard](/assets/images/terminal-settings/image-20211115013913042.png) 

Alternativ kann man sich einen eigenen, kürzeren Prompt erstellen. Hierzu wird eine Zeile mit entsprechenden Anweisungen in die Datei `.bashrc` eingefügt.

**Hinweis**: Die Datei findet man im Ordner "Persönlicher Ordner", damit sie angezeigt wird, muss die Option "Verborgene Dateien anzeigen" aktiviert sein:

![image-ubuntu-filemanagement-file-bashrc](/assets/images/terminal-settings/image-20211115014541969.png)

Mit einem Doppelklick öffnet sich die Datei im Standardeditor des Systems, hier "gedit".

![image-editor-gedit-with-open-file-bashrc](/assets/images/terminal-settings/image-20211115014817442.png)

In Zeile 121, am Ende der Datei, wurden die neuen Vorgaben für den Prompt eingefügt. Nach Speichern und erneuten Öffnen des Terminals erscheint dann der neue Prompt.

![image-open-terminal-with-new-short-prompt](/assets/images/terminal-settings/image-20211115015044454.png)

Am einfachsten erstellt man die erforderliche Zeichenfolge für den neuen Prompt mit einem der im Internet verfügbaren Prompt- Generatoren, hier wurde der 

[scriptim bash-prompt-generator](https://scriptim.github.io/bash-prompt-generator/) 

benutzt, mit dem man dem Prompt auch verschiedene Farbvarianten zuordnen kann.

Im Beispiel oben wurde die Option "Hostname short", ein Bindestrich und anschließend "Working Directory (Basename)" gefolgt von dem Zeichen `>`gewählt  sowie die Farbe geändert.

![image-website-github-prompt-generator-with-example](/assets/images/terminal-settings/image-20211115021718645.png)

Die einzelnen Variablen kann man aber auch selbst zusammenstellen, eine Anleitung und Übersicht über die Syntax findet sich hier:

[ss64.com](https://ss64.com/bash/syntax-prompt.html)

## Fazit

Die drei Anpassungsmöglichkeiten

- aktuelle Schriftgröße
- dauerhafte Anpassung über die Einstellungen
- Ändern des Prompt

erleichtern die Nutzung des Terminals deutlich. In ähnlicher Weise lassen sich auch das Terminal auf einem Mac, die ZSH, und das Windows- Terminal anpassen.
