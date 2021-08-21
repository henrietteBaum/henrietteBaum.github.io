---
layout: post
title: "Einstieg in Java mit Visual Studio Code unter Windows"
author: Henriette Baum
---


Voraussetzung um Java- Programme kompilieren und ausführen zu können:

- Visual Studio Code (Download unter [Visual Studio Code - Code Editing. Redefined](https://code.visualstudio.com/) )

- JDK (Java Development Kit) ab Version 11, SE (Standard Edition)

  

In VS Code installiert man zunächst das Extension-Pack für Java. Dazu in der linken Seitenleist das Symbol für "Extensions" auswählen. In der sich dann öffnenden Liste findet man eine Erweiterung am schnellsten durch Eingabe des Suchbegriffs "java" in das Suchfeld:

![image-java-extension](/assets/images/java-vscode-win/image-20210818233000265.png)

Ist bereits eine JDK- Version auf dem System vorhanden, kann man - nach einem Neustart von VS Code - Java- Programme direkt in der IDE erstellen und ausführen. Üblicherweise werden Java-Programme in Projekten angelegt und nicht als einzelne Datei.  Im nächsten Schritt also ein neues Java-Projekt erstellen und in diesem dann die `.java` - Programmdatei.



![image-button-new-java-project](/assets/images/java-vscode-win/image-20210819002851988.png)

Ist noch keine JDK- Version auf dem Computer vorhanden, wird beim Versuch, ein neues Projekt anzulegen, eine Fehlermeldung angezeigt:

![image-java-warning](/assets/images/java-vscode-win/image-20210819003143243.png)

Ein Click auf den Button "Get the Java Development Kit" führt zur Downloadseite von Red Hat.

![image-downloadpage-RedHat](/assets/images/java-vscode-win/image-20210819004026817.png)

Alternativ kann man auch ein Oracle-JDK installieren, ebenfalls über einen Installer :

[Java SE Development Kit 16 - Downloads (oracle.com)](https://www.oracle.com/java/technologies/javase-jdk16-downloads.html)

![image-download-java-installer](/assets/images/java-vscode-win/image-20210819000731235.png)

Nach dem Download den Installer starten:

![image-oracle-java-installer](/assets/images/java-vscode-win/image-20210819004507636.png)



![image-java-successfully-installed](/assets/images/java-vscode-win/image-20210819004629918.png)

Der Button "Next Steps" führt zur Oracle- Webseite mit der  Dokumentation.

Nach der Installation des JDK VS Code neu starten. Nun kann man ein neues Java-Projekt erstellen. Bei der Abfrage "Select the project type"  für einen ersten Test zunächst die Option "No build tools" auswählen.

![image-new-project-no-build-tools](/assets/images/java-vscode-win/image-20210819005727121.png)

Danach den Ordner bestimmen, in dem das Projekt gespeichert werden soll und einen Namen für das Projekt vergeben.

In der Seitenleiste wird dann die Dateistruktur des neuen Projekts angezeigt.

![image-vscode-explorer-project-tree](/assets/images/java-vscode-win/image-20210819010233424.png)

Im Ordner `src` (source) befindet sich bereits eine erste Datei mit dem Namen "App.java" die das obligatorische Hello-World-Programm enthält. Das Programm startet man über die dreieckige Schaltfläche oben rechts über dem Editorbereich, alternativ über das Menü oder direkt im Programmfenster durch anklicken von `Run` : 

![image-App-java-in-editor](/assets/images/java-vscode-win/image-20210819011237162.png)

Durch den Aufruf von `Run` wird das Programm kompiliert und die Ausgabe in einem Terminalfenster im unteren Bereich angezeigt. Das kompilierte Programm (mit der Endung `.class` ) befindet sich im Ordner "bin".

![image-compile-and-run-programm](/assets/images/java-vscode-win/image-20210819011914459.png)

Das Terminal schließen über die Schaltfläche "Java Process Console -> Kill Terminal" :

![image-close-terminal](/assets/images/java-vscode-win/image-20210819015516678.png)



Ein eigenes Java- Programm erstellt man, indem man den Ordner `src` in der Seitenleiste auswählt und dort durch Anklicken des Dateisymbols oberhalb des Dateibaums eine neue Datei mit der Endung `.java` anlegt.



![image-new-java-file](/assets/images/java-vscode-win/image-20210819020040944.png)

Die Dateinamen müssen mit einem Großbuchstaben beginnen, die Datei muss den gleichen Namen haben, wie die   Klasse, die in ihr erstellt wird.

![image-new-java-class](/assets/images/java-vscode-win/image-20210819020721358.png)

Ausführbar ist die Java- Datei nur, wenn sie eine `main` - Methode enthält. VS Code bietet das automatische Erstellen der Methode an, sobald die ersten beiden Buchstaben eingegeben werden:

![image-create-main-method-automaticaly](/assets/images/java-vscode-win/image-20210819021234346.png)

Dies spart viel Tipparbeit:

![image-java-main-method](/assets/images/java-vscode-win/image-20210819021413857.png)

Nun kann man innerhalb der `main` - Methode weitere Anweisungen, hinzufügen. 

### Packages

Oftmals werden zusammengehörende Programmdateien in Packages zusammengefasst. Dies sind eigentlich nur Ordner. Eclipse und IntelliJ bieten eigene Dialoge zum Erstellen, in VS Code legt man in `src` einfach einen Unterordner an und erstellt die neue Programmdatei darin. 

![image-windows-vscode](/assets/images/java-vscode-win/image-20210819022936309.png) 

Package mit neuer Datei:

![image-new-package-with-file](/assets/images/java-vscode-win/image-20210819022712510.png) 

Die Zugehörigkeit zu einem Package muss in der Datei explizit angegeben werden. die erfolgt in der ersten Zeile mit der Anweisung `package` :

![image-package-declaration-inside-file](/assets/images/java-vscode-win/image-20210819023405763.png)

Die Anweisung wird von VS Code automatisch eingefügt. 

Eine Möglichkeit, umfangreichere Projekte zu strukturieren, bieten die sog. Build-Tools. Häufig genutzt werden Maven und Spring.  Deren Verwendung bietet VS Code auch beim Erstellen eines neuen Java- Projekts an. Für erste Übungen braucht man sie aber noch nicht.
