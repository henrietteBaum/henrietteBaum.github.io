---
layout: post
title: Markdown-Notebook mit Visual Studio Code
author: Henriette Baum
---


Mit der Markdown-Syntax lassen sich schnell gut lesbare Texte schreiben. Die Formatierung wird mit Hilfe von Tastenkombinationen zugeordnet.

Bereits ohne die Installation zusätzlicher Extensionen kann man mit VSCode Texte im Markdown-Format erstellen. Auch eine Option für die Vorschau ist bereits integriert.

## Markdown-Notebook

Sehr gut geeignet, um Code-Snippets zu dokumentieren oder auch für Vorlesungsmitschriften ist die Erweiterung **Markdown-Notebook**.


![screenshot markdown-notebook extension](/assets/images/vscode-md-notebook/screen-vscode-md-notebook.jpg)


Nach der Installation kann man bereits vorhandene Markdown-Dateien mit der Notebook-Erweiterung öfnen und im Notebook-Format bearbeiten. 
Dazu klickt man mit der rechten Maustaste im Explorer auf den Dateinamen.

Damit öffnet sich die Command-Palette in der nun die Option "Markdown Notebook" zur Verfügung steht. 


![screenshot open file with markdown-notebook](/assets/images/vscode-md-notebook/screen-open-with.jpg)


Die Bedienung ist selbsterklärend: es gibt zwei Schaltflächen mit denen man entweder einen Block im Markdown-Format oder einen Code-Block erstellt und ein kleines Menu. Im Dokument werden die Schaltflächen jeweils beim Überfahren des oberen oder unteren Zellenrandes eingeblendet. Das Verhalten des Notebooks lässt sich aber auch über die Einstellungen ändern.


![screenshot markdown-cell](/assets/images/vscode-md-notebook/md-cell.jpg) 


Für die Formatierung des Codeblocks (Syntax-Highlighting) stehen zahlreiche Programmiersprachen zur Verfügung. Durch Anklicken des Schritzuges "Plain Text" öffnet sich eine Auswahl in der Command-Palette. Mit dem Eintippen weniger Buchstaben filtert man schnell die angebotene Liste.


![screenshot choose syntax for code-block](/assets/images/vscode-md-notebook/code-block-syntax.jpg)


Die Bearbeitung selbst bietet den von VSCode gewohnten Komfort zum Vergrößern des Textes mit dem Mausrad bei gedrückter STRG-Taste oder die Bracket Pair Colorization innerhalb eines Code-Blocks. Für beides muss aber zunächst die entsprechebnde Option in den Einstellungen aktiviert sein. 

Zu beachten ist, dass sich bei einigen Color-Themes der Hintergrund des Blocks oder der Zelle nur wenig farblich vom Dokument-Hintergrund abhebt (z.B. GitHub-Dark-Default oder One Dark Pro). Ausprobiert habe ich hier beispielhaft "Tomorow Night Blue" und "Mariana Pro Cool", bei denen die Farbdarstellung gute Lesbarkeit bietet. Dafür helfen aber einige Themes mit einem blauen Focus um die aktive Zelle.


![screenshot markdown-cell with focus](/assets/images/vscode-md-notebook/vscode-dark-focus.jpg)


Neue Zellen fügt man beliebig zwischen vorhandene Blöcke mithilfe er oberen oder unteren Schaltfläche. Mit der Maus kann man auch einen ganzen Block verschieben.

Jede Zelle zeigt oben ein kleines Menü mit hilfreichen Funktionen. Durch Anklicken des Häckchens am oberen Rand der Zelle wechselt man in einen Vorschau-Mudus, für jede Zelle separat, und wieder zurück zur Bearbeitung über das Stift-Symbol. Zellen lassen sich an der Cursor-Position teilen, kopieren, ausschneiden, einfügen oder Zeilennummern einblenden.

Beim anschließenden Speichern der Datei bleibt auch nach der Bearbeitung im Notebook das ursprüngliche Dateiformat (.md) erhalten. So lässt sich das Dokument dann auch als PDF oder HTML Datei exportieren. 

**Hinweis:** Nicht alle Syntax-Stile werden in den "normalen" Markdown-Text übernommen. So z.B. beim oben ausgewählten Highlighter für `JavaSvript-React`, ein solcher Code-Block wird dann nur als Plain-Text angezeigt. Abhilfe schafft die Auswahl von nativem `JavaScript`als Highlighter.


## Fazit

Das Markdown Notebook ist eine sehr hilfreiche Erweiterung zum schnellen Verfassen von Markdown-Texten mit Codeblöcken, das viel Tipparbeit spart.

Alle Funktionalität, die VSCode auch sonst bietet, wie u.a.skalierbare Editorschrift, individuelle Farbanpassung, Bracket-Pair-Highlighting, stehen auch im Notebook zur Verfügung und erleichtern das Arbeiten damit sehr. Unter MacOs und Windows kann ein Screenreader den Text vorlesen, das vermeidet Schreibfehler, die man selbst nicht mehr sehen würde.

Weil das Notebook kein eigenes Format benutzt, kann man die bearbeitete Datei problemlos in andere Formate, wie PDF oder HTML exportieren. Damit ersetzt es einen vollwertingen Markdown-Editor, der auf allen Betriebssystemen gleichermaßen gut funktioniert.
