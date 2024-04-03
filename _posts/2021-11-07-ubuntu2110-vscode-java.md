---
layout: post
title: "Java lernen mit Visual Studio Code unter Ubuntu 21.10"
author: Henriette Baum
---
Erklärt werden die nachstehenden Einrichtungsschritte:

1. Visual Studio Code über die Softwareverwaltung installieren.
2. Extension- Pack installieren
3. Java- Umgebung einrichten
4. Ein Java Projekt erstellen

## Visual Studio Code installieren
Unter Ubuntu steht VSCode als Snap-Paket zur Verfügung. Es kann einfach über die Softwareverwaltung installiert werden. 

## Extension- Pack für Java installieren: 

Über das Symbol mit den vier Quadraten in der Seitenleiste öffnet man eine Übersicht. Bereits nach Eingabe des Buchstabens `j` in das Suchfeld oben werden passende Erweiterungen angeboten. 



![image-vscode-java-get-started](/assets/images/2021-11-07-ubuntu2110-vscode-java/image-20211107115646541.png)

Nach der Installation der Erweiterung öffnet sich ein neuer Einrichtungsassistent für Java, über den man einen Überblick über die bereits installierten Java- Versionen (installed JDK's) erhält oder einen Downloadlink (Install a JDK) wählen kann.

## Java einrichten

Um Java- Programme erstellen zu können, benötigt man ein Java Development Kit, kurz JDK. Angeboten wird es zum Download von [Oracle](https://www.oracle.com/java/technologies/downloads/) oder als Opennsource- Version [openJDK](https://openjdk.java.net) .

 Statt des Downloads ist unter Linux der einfachere Weg die Installation eines openJDK über die Paketquellen. Die von der Ubuntu- Wiki [wiki-ubuntuusers](https://wiki.ubuntuusers.de/Java/Installation/OpenJDK/) empfohlenen Pakete installiert man über das Terminal:

```bash
sudo apt-get install openjdk-17-jdk openjdk-17-demo openjdk-17-doc openjdk-17-jre-headless openjdk-17-source 
```

Anschließend die Installation im Terminal überprüfen:

```bash
java --version
# für den Compiler:
javac --version
```

![image-ubuntu-terminal-control-java-version](/assets/images/2021-11-07-ubuntu2110-vscode-java/image-20211107123948012.png)



## Umgebungsvariablen setzen

Damit auf das JDK und den Compiler zugegriffen werden kann, müssen noch die Umgebungsvariablen `JAVA_HOME` und `PATH` gesetzt werden. Dies erfolgt durch einen Eintrag in die Datei `bashrc` 

```bash
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
export PATH=${PATH}:${JAVA_HOME}/bin
```

![image-ubuntu-bashrc-java-home-and-path](/assets/images/2021-11-07-ubuntu2110-vscode-java/image-20211107131733079.png)

Die erfolgreiche Einrichtung im Terminal überprüfen:

![image-ubuntu-terminal-test-java-home-andpath](/assets/images/2021-11-07-ubuntu2110-vscode-java/image-20211107131511013.png)

___

**Hinweis**:

Die Variable JAVA_HOME verweist auf den Installationsort der JDK im Dateibaum, PATH verweist auf den Ort des Compilers. Vereinfacht gesagt verwenden VSCode oder eingesetzte Build- Tools diese Variablen, um ausführbare Programme oder benötigte Dateien im System zu finden, ohne dass man jedes Mal den vollständigen Pfadnamen angeben muss.

___



In VSCode nach der Installation des JDK das Fenster neu laden (Schaltfläche: "Reload Window"). Das installierte JDK unter dem Reiter "Installed JDK's" angezeigt.

![image-vscode-java-installed-jdk](/assets/images/2021-11-07-ubuntu2110-vscode-java/image-20211107132543156.png)

Nun kann man bereits  ein erstes Java-Projekt anlegen und ausprobieren oder mit dem Assistenten fortfahren. 

![image-vscode-java-assistent-step2](/assets/images/2021-11-07-ubuntu2110-vscode-java/image-20211107134925973.png)

Hier werden zusätzliche empfohlene Erweiterungen vorgeschlagen.

Die folgenden Punkte führen dann Schritt für Schritt zum ersten Java-Projekt:

![image-vscode-java-assistent-steps](/assets/images/2021-11-07-ubuntu2110-vscode-java/image-20211107135224592.png)



## Ein Java- Projekt erstellen

Üblicherweise werden java- Programme in Projekten organisiert. Innerhalb des Projekts wird eine konventionelle Ordnerstruktur verwendet.

Über den Einrichtungsassistent - "Open project folder"  wählt man zunächst einen Ordner für das neue Projekt aus. Anschließend  wählt man ein Build-Tool, hier reicht für das erste Ausprobieren die Option "No build tool". Dann muss ein Projektname vergeben werden. Unter diesem Namen wird automatisch ein neuer Projektordner erstellt, der weitere Unterordner für die java- Dateien (Ordner: src) und die kompillierten Programme (Ordner: bin) und einen Ordner für Bibliotheken (Ordner: lib).



![image-vscode-java-project-structure-and-hello-world-programm](/assets/images/2021-11-07-ubuntu2110-vscode-java/image-20211108023443340.png)

Im Ordner `src` befindet sich bereits eine java- Datei mit dem Namen "App.java". Die kann man direkt ausführen über die kleine dreieckige Schaltfläche oben rechts, über das Menü oder durch Anklicken des Schriftzuges "Run" innerhalb der Datei im Editor.

Die Datei wird unmittelbar kompilliert und ausgeführt. Das Ergebnis wird im Terminal unterhalb des Editorbereichs angezeigt.

Das kompilierte Programm wird automatisch im Ordner `bin` abgelegt.

## Fazit

Der Einstieg in die Programmiersprache Java und die Verwendung einer Integrierten Entwicklungsumgebung (IDE)  wird mit Visual Studio Code deutlich erleichtert. Der Einrichtungsassistent bietet eine sehr gute Unterstützung bei den ersten Schritten. 