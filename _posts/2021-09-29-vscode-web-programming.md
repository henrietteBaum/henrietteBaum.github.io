---
layout: post
title: "Web-Programmierung mit Visual Studio Code"
author: Henriette Baum
---

Für die Entwicklungsumgebung (IDE) Visual Studio Code findet man Installer auf der Homepage des Herstellers. Unter Ubuntu kann man einfach über die Softwareverwaltung installieren. 

VSCode hat bereits die Unterstützung für alle drei Sprachen(HTML, CSS, JavaScript) an Bord, man kann also direkt loslegen. 

Empfehlenswert sind dennoch die Erweiterungen "HTML-Preview" und "Open in Browser". Beide lassen sich bequem über das Symbol in der Seitenleiste und das dort angebotene Suchfeld finden und installieren:

![image-vscode-extension-html-preview](/assets/images/vscode-web-programming-images/vscode-web-prog_01.png)



![image-vscode-extension-open-in-browser](/assets/images/vscode-web-programming-images/vscode-web-prog_02.png)

Um verschiedene Gestaltungsvariationen mit CSS oder JavaScript Programme ausprobieren zu können, legt man zunächst ein einfaches HTML- Dokument an. In dieses werden dann die zu testenden Stylesheets oder JavaScript- Dateien eingebunden.

![image-vscode-create-html-document](/assets/images/vscode-web-programming-images/vscode-web-prog_03.png)

Schon bei der Eingabe des ersten Zeichens wird eine Vervollständigung angeboten.

![image-vscode-create-html-document-body](/assets/images/vscode-web-programming-images/vscode-web-prog_04.png)

Auch Tags werden nach Eingabe der ersten Buchstaben vorgeschlagen und durch Bestätigen mit `Return` eingefügt.

___

**Hinweis**: Für HTML-Dokumente werden nach Konvention nur Einrückungen von 2 Leerzeichen verwendet.  Die Einstellung erreicht man über Settings -> Editor-Tab Size:

![image-20210928220600958](/assets/images/vscode-web-programming-images/vscode-web-prog_05.png)

___

Das vollständige (minimalistische) HTML- Dokument:

```html
<!DOCTYPE html>
<html lang="de=DE">
<head>
  <meta charset="UTF-8">
  <link rel="stylesheet" href="styles/ ">
  <title>Testen von ... </title>
</head>
  <body>
    <h1>Testseite</h1>  

    <script> </script>
  </body>
</html>
```

Dieses Grundgerüst lässt sich schnell in eine neue HTML-Datei, mit neuem Namen kopieren, um damit ein neues Projekt auszuprobieren.

Zudem benötigt dann natürlich die entsprechende CSS-Datei bzw. JavaScript-Datei. Beide Datei-Formate werden jeweils in separaten Ordnern  (**styles** und **scripts**) abgelegt. Die Ordner kann man direkt in VSCode erstellen, u.a. über die Symbole im Explorerbereich der Seitenleiste:

![image-vscode-create-folder](/assets/images/vscode-web-programming-images/vscode-web-prog_06.png)

Beim Einbinden einer Datei muss dann der entsprechende Ordnername vorangestellt werden. Auch hier hilft die Autovervollständigung und zeigt eine Liste der im Ordner verfügbaren Dateien.

Für eine CSS-Datei z.B.:

```html
<link rel="stylesheet" href="styles/main.css">
```

Und eine JavaScript- Datei:

```html
<script src="scripts/main.js"></script>
```
Alternativ zur oben gezeigten konventionellen Ordnerstruktur für Webseiten kann man für kleinere Übungsbeispiele oder Aufgaben jeweils einen eigenen Ordner anlegen, indem dann einfach HTML- Dokument, CSS- und JavaScript- Datei abgelegt werden.

![image-vscode-exercise-folder](/assets/images/vscode-web-programming-images/vscode-web-prog_16.png)
## Vorschau

Die Vorschau des HTML-Dokuments öffnet man mit der Schaltfläche oben rechts über dem Editorfenster oder per Tastenkombination.

![image-vscode-open-html-preview](/assets/images/vscode-web-programming-images/vscode-web-prog_07.png)

Es öffnet sich ein neuer Tab auf der rechten Seite:

![image-vscode-html-preview](/assets/images/vscode-web-programming-images/vscode-web-prog_08.png)

Im Preview wird nur das HTML-Dokument mit Formatierung angezeigt, keine JavaScript-Anweisungen.

Hierfür kann man nun die Erweiterung "Open in Browser" nutzen und HTML-Dokument nebst JavaScript im Browser seiner Wahl öffnen. Mit einem Rechtsklick im Editorfenster der HTML-Datei erreicht man ein Kontextmenü:

![image-vscode-contextmenu](/assets/images/vscode-web-programming-images/vscode-web-prog_09.png)

Um den "Default Browser" zu verwenden, muss man diesen zunächst in den Einstellungen festlegen. "Other Browser" öffnet das Menü der Command-Palette mit einer Browserauswahl.

![image-vscode-select-browser](/assets/images/vscode-web-programming-images/vscode-web-prog_10.png)

___

Hinweis: Command-Palette - das ist ein Menü, über das man alle in VSCode verfügbaren Befehle erreichen kann, ohne dass man wissen muss, hinter welchem Menüpunkt diese zu finden sind. Aufruf per Tastenkombination `Ctrl + Umschalt + P` bzw. `Cmd + Umschalt + P` auf dem Mac.

![image-vscode-command-palette](/assets/images/vscode-web-programming-images/vscode-web-prog_11.png)

An oberster Stelle stehen die zuletzt verwendeten Befehle. Gibt man Text in das Suchfeld ein, wird die Ansicht entsprechend des Suchbegriffs gefiltert.

![image-vscode-command-palette-search-item](/assets/images/vscode-web-programming-images/vscode-web-prog_12.png)

___



![image-html-document-with-js-dialogbos-in-browser](/assets/images/vscode-web-programming-images/vscode-web-prog_13.png)

Lässt man das Browserfenster geöffnet, werden zwischenzeitlich durchgeführte Änderungen im HTML-Dokument, CSS und JavaScript erst durch "Seite neu laden" angezeigt.

Wer mag, kann dann auch noch für  - zusätzliches -schnelles Ausprobieren die Entwicklerwerkzeuge des Browsers nutzen (Browsermenü -> Weitere Werkzeuge -> Werkzeuge für Web-Entwickler).

![image-firefox-developertools](/assets/images/vscode-web-programming-images/vscode-web-prog_14.png)

Über den Tab "Konsole" erhält man einen Prompt, an dem man JavaScript Code eingeben kann.

![image-firefox-developertools-console-with-javascript](/assets/images/vscode-web-programming-images/vscode-web-prog_15.png)



## Fazit

Die oben beschriebene Vorgehensweise benötigt etwas Einarbeitung in die Entwicklungsumgebung Visual Studio Code und Vorbereitungszeit für das Einrichten der Ordner. Man hat aber den Vorteil, gerade erlernte oder getestete Codebeispiele immer zur Verfügung zu haben, zum späteren Nachschauen oder Wiederverwenden. 

Ein Programm im Editor zu schreiben, nimmt dem Menschen viel Arbeit ab und hilft, Eingabefehler zu vermeiden.

Zudem kann man Visual Studio Code für alle gängigen Programmiersprachen und Markupsprachen verwenden. Wer die grundlegenden Funktionen einmal kennt, kommt dort schnell auch mit anderen sprachspezifischen Funktionen zurecht.

Hinweis: Wer möchte, kann für eine erste Orientierung in VSCode das deutsche Sprachpaket installieren, die gesamte Benutzeroberfläche erscheint dann in deutscher Sprache. Diese Option bietet das Programm sogar in einem Popup-Fenster unten rechts nach jedem Programstart an.
