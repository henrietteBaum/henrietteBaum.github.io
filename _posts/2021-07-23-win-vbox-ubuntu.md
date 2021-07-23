---
layout: post
author: Henriette Baum
categories: VM
---

# VirtualBox unter Windows

Um ein neues Betriebssystem auszuprobieren oder bei den ersten Versuchen mit einer neu zu lernenden für eine Programmiersprache und Einrichtung der entsprechenden Entwicklungsumgebung eignet sich die Verwendung einer Virtuellen Maschine (VM) mit Oracle VirtualBox besonders gut. 

Ein Installer steht auf der Oracle- Seite für zahlreiche Betriebssysteme zum Download zur Verfügung.

[Oracle VM VirtualBox - Downloads](https://www.oracle.com/de/virtualization/technologies/vm/downloads/virtualbox-downloads.html)

Eine ausführliche Dokumentation:

[Oracle VM VirtualBox - Oracle VM VirtualBox Documentation](https://docs.oracle.com/en/virtualization/virtualbox/index.html)

![VirtualBox-Download Bild](/assets\images\VirtualBox-unter-Windows-images\virtualbox-win-ubuntu_00.png)

Die Installation ist selbsterklärend. Wer mag, kann eine separate Partition für die VMs einrichten. 

![VirtualBox, eigene Ordner in separater Partition](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_01.png)

Das erhöht die Übersichtlichkeit, ansonsten wird alles in Laufwerk C gespeichert.

## Eine VM einrichten

Nach der Installation VirtualBox öffnen und über die Schaltfläche Neu oder das Menü Maschine - Neu eine leere VM einrichten.

![VirtualBox-neue-VM](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_02.png)

Es öffnet sich dann ein Fenster, in dem  man einen Namen für die neue VM vergeben und den Speicherort auswählen muss. Das Programm erkennt bereits am vergebenen Namen, um welche Art von Betriebssystem es sich handelt, Typ und Version werden automatisch gewählt, lassen sich aber auch ändern.

![VirtualBox-neue-VM](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_03.png)

Gibt man statt im Beispiel oben Windows an, wird als Typ Windows 7 angeboten, über das Pull-Down Menü aber auch zahlreiche andere Versionen.

![VirtualBox-neue-VM](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_04.png)

Hinweis: Hier wird noch kein Betriebssystem installiert, es handelt sich immer noch um eine leere VM

Über die Schaltfläche weiter gelangt man zur Auswahl der Größe des Arbeitsspeichers für die neue VM.

![VirtualBox-neue-VM Bild(V
Dazu sollte der Rechner wenigstens 8 GB Arbeitsspeicher haben, so dass für die VM 4 GB zur Verfügung gestellt werden können.

Die folgenden Schritte kann man so bestätigen, wie angeboten.

![VirtualBox-neue-VM](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_05.png)

Die Größe der Festplatte lässt sich vor der eigentlichen Installation noch erhöhen, die angebotenen 10  GB sind in der Regel zu knapp.

Über Erzeugen gelangt man zur Auswahl des Datentyps für die Festplatte, diesen bei VDI belassen.

![VirtualBox-neue-VM-Datentyp-wählen Bild](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_06.png)

Im nächsten Fenster dynamisch alloziert beibehalten.

![VirtualBox-neue-VM Bild](../assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_07.png)
Im nächsten Schritt können Ordnername und Maximalgröße der  VM- Festplatte verändert werden. Bis zu dieser Maximalgröße dürfen sich später die Daten der VM ausbreiten. Die VM nimmt immer nur den Speicherplatz ein, der ihrer aktuellen Datenmenge entspricht, das kann also auch deutlich unter der Maximalgröße liegen. Um spätere Probleme zu vermeiden, sollte man die Maximalgröße lieber großzügig bemessen.

Mit Erzeugen wird die VM fertiggestellt und eine Übersicht angezeigt. Die VM ist aktuell noch ausgeschaltet. Mit Starten gelangt man zur Installation des Betriebssystems.

![VirtualBox-neue-VM Bild(V
Im Folgenden erscheint ein Auswählfenster für das ISO-Image. Hier wird das zuletzt verwendete Image angezeigt, über das Pull-Down Menü erhält man auch nur die bereits verwendeten ISO-Dateien. Erst der Klick auf das Ordnersymbol öffnet ein neues Fenster, wo man wiederum über Hinzufügen den Zugriff auf weitere ISO-Images irgendwo auf der Festplatte, dem USB-Stick oder DVD erhält 

![VirtualBox-neue-VM Bild](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_08.png)

Im Windows-Explorer, die gewünschte Iso-Datei auswählen und mit Öffnen bestätigen. Anschließend erscheint die Datei im Auswahlfenster.

![VirtualBox-neue-VM Bild](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_09.png)

Mit Auswählen bestätigen, dann gelangt man wieder in das anfangs erschienene Fenster und kann dort die Installation mit dem ausgewählten ISO starten.

![VirtualBox-neue-VM Bild](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_10.png)

Der Boot-Manager von Ubuntu erscheint, mit Enter wird gestartet.

![VirtualBox-neue-VM Bild](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_11.png)

Man kann nun Ubuntu als Live-Version testen oder in die neue VM installieren.

![VirtualBox-neue-VM Bild](/assets/images/VirtualBox-unter-Windows-images/virtualbox-win-ubuntu_12.png)

Ubuntu installieren führt zur regulären Installationsroutine des Betriebssystems. 

Hinweis: nach dem Abschluss der Installation kann man die Aufforderung, das Installationsmedium zu entfernen (... press Enter) einfach mit der Eingabetaste bestätigen, ohne ein Medium entfernen zu müssen.

## Gasterweiterungen

Damit die VM nicht nur in einem kleinen Fenster angezeigt wird und man das Gastbetriebssystem nutzen kann, wie einen "ganz normalen Rechner", müssen die Gasterweiterungen eingehängt werden.

Auch ist erst dann die Verbindung zum Host- Betriebssystem, beispielsweise mit einer gemeinsamen Zwischenablage oder gemeinsamen Ordnern möglich.

