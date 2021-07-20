---
layout: post
title: Unter MacOs Java mit Visual Studio Code einrichten
categories: vscode
---

### Java-Extension Pack installieren

Microsoft bietet eine Zusammenstellung aller für Java erforderlichen Extensions an. Über das Extension- Symbol der Seitenleiste und Eingabe des Suchbegriffs "java" wird das Paket gleich ganz oben angezeigt.

![MacOs-setup-java-environment-vscode](/assets/images/MacOs-setup-java-env-vscode/mac-java-setup-vscode_10.png)

Anschließend VS Code neu starten.

Nach dem Start der IDE öffnet sich dann ein Assistent, der die bereits auf dem System vorhandenen Java- Versionen ermittelt.

![MacOs-setup-java-environment-vscode](/assets/images/MacOs-setup-java-env-vscode/mac-java-setup-vscode_01.png)

Wenn keine JDK gefunden wird, bietet der Assistent den Download an.

Als nächstes die gewünschte Version auswählen, der Click auf "Download" führt dann direkt zur Downloadseite des Anbieters:

Standardmäßig wird die OpenJDK Version von AdoptOpenJDK angeboten. 

![MacOs-setup-java-environment-vscode](/assets/images/MacOs-setup-java-env-vscode/mac-java-setup-vscode_02.png)

Unter dem Tab "Others" sind aber auch andere wählbar.

![MacOs-setup-java-environment-vscode](/assets/images/MacOs-setup-java-env-vscode/mac-java-setup-vscode_03.png)

Nach dem Download die Installation durch Anklicken des Paketsymbols anstoßen:

![MacOs-setup-java-environment-vscode](/assets/images/MacOs-setup-java-env-vscode/mac-java-setup-vscode_04.png)

Es öffnet sich ein Dialog, der durch die Installation führt:

![MacOs-setup-java-environment-vscode](/assets/images/MacOs-setup-java-env-vscode/mac-java-setup-vscode_05.png)

Nach der Installation in VS Code die Option "Reload Window" wählen. anschließend wird die neu installierte JRE aufgeführt:

![MacOs-setup-java-environment-vscode](/assets/images/MacOs-setup-java-env-vscode/mac-java-setup-vscode_06.png)

![MacOs-setup-java-environment-vscode](/assets/images/MacOs-setup-java-env-vscode/mac-java-setup-vscode_07.png)

Hier ist es auch möglich, für verschiedene Projekte unterschiedliche Java oder besser JDK- Versionen zu bestimmen.

Beim erneuten Öffnen von Visual Studio Code erhält man ein Startfenster, von dem aus man alle gängigen Aktivitäten erreicht.

![MacOs-setup-java-environment-vscode](/assets/images/MacOs-setup-java-env-vscode/mac-java-setup-vscode_08.png)

Scrollt man im Explorer- Bereich, also in der linken Seitenleiste nach unten, wird auch die Schaltfläche zum Erstellen eines neuen Java-Projekts sichtbar.

![MacOs-setup-java-environment-vscode](/assets/images/MacOs-setup-java-env-vscode/mac-java-setup-vscode_09.png)
