# UML-Projekt

Zum Üben von Analyse und Entwurf mit UML-Diagrammen erstellen Sie arbeitsteilig in Zweiergruppen ein Projekt mit folgendem Rahmen:

- Jedes Projekt bezieht sich auf ein Gerät (*Gadget*) mit einiger Komplexität, zu dem eine Bedienungsanleitung öffenlich zugänglich ist. Die Bedienungsanleitung wird dem Projektordner beigefügt.
- Jede Gruppe bearbeitet ein anderes Thema aus den Themenvorschlägen (siehe unten)
- Das Projekt umfasst mindestes jeweils ein Diagramm der fünf im Unterricht behandelten Diagrammtypen nach Vorgaben zur erwarteten Komplexität und Qualität.
- Die Diagramme sind mit UMLet zu erstellen und das Ergebnis ist jeweils als UXF-, PDF- und PNG-Datei abzugeben. Die Ordnerstruktur hierfür ist schon angelegt.
- Zu jedem Diagrammtyp ist eine Markdown-Datei angelegt. Darin wird die PNG-Datei eingebunden und ein Beschreibungstext zu dem Diagramm verfasst. *Beschreibung* bedeutet hierbei Fließtext in Sätzen, nicht stichwortartige Aufzählung.
  - Geben Sie beim Einbinden der Bilder relative Dateipfade an, so dass die Bilder auch auf dem Dozentenrechner angezeigt werden.
- Sie achten innerhalb Ihres Teams auf faire Arbeitsteiiung und dokumentieren diese in der hierzu angelegten Markdowndatei.

## Projektthemen

- Multifunktionsgerät HP Smart Tank 7306 All-in-One
- Saugroboter DJI ROMO P2 (Wassertank-Version)
- Wallbox Ladestation für E-Auto
- Ninja CREAMi Scoop & Swirl 13-in-1 Softeis- und Eismaschine
- Tefal OptiGrill Elite XL
- Wärmepumpe
- Dyson Raumklimagerät
- Systemkamera
- VR Ausrüstung
- Teleskop

Wir können gerne über einen anderen Themenwunsch sprechen. Themen, die von früheren Projektgruppen behandelt wurden, schließe ich aus.

## Erwartete ideale Detailtiefe je Diagrammtyp

- Ich kann keine pauschale Aussage zur gewünschten Anzahl Details in einem Diagramm oder zur Textlänge der Beschreibungen machen. Was sinnvoll ist, wird sich aus dem Thema ergeben und daraus, wo das Team Schwerpunkte in der Betrachtung setzt.
- Die Diagramme sollen übersichtlich und verständlich sein. Daraus ergeben sich Grenzen für die die mögliche Menge an Details.
- Es kann sinnvoll sein, anstelle eines einzelnen detailreichen Diagramms mehrere einfache Diagramme zu erstellen.
- Ich gebe Ihnen im Projektverlauf gerne Rückmeldung auf Ihre Entwürfe.

### Use-Case Diagramm

- System eingrenzen. Welche Eigenschaften des Gadgets sollen betrachtet werden?
- Nach bester Möglichkeit mehrere Akteure identifizieren.
- Falls zutreffend, Vererbungs-Beziehungen zwischen Akteuren abbilden.
- Eine nicht zu kleine, aber noch übersichtliche Anzahl Anwendungsfälle.
- Verschiedene Arten von Beziehungen zwischen Anwendungsfällen.
- Verständliche Benennung von Akteuren und Anwendungsfällen.

### Activity Diagramm

- Eine nicht zu kleine, aber noch übersichtliche Anzahl Aktionen.
- Diverse Kontrollstrukturen (Entscheidungen, Zusammenführungen, Splitting und Synchronisation)
- Gerne Swimlanes für mehrere Akteure.

### Class Diagramm

- Entsprechend den Funktionen des Gadgets eine Aufteilung in Klassen vornehmen.
- Attribute und Operationen eintragen.
- Beziehungen zwischen den Klassen identifizieren.
- Sie benötigen eines oder mehrere Klassen-Diagramme als Grundlage für Ihre Zustands- und Sequenz-Diagramme.

### State-Machine Diagramm

- Identifizieren Sie mögliche Zustände des Gadgets.
- Definieren Sie mögliche Transitionen mit Funktionsaufrufen, Guards und Verhalten in Übereinstimmung mit Ihren Klassendiagrammen.

### Sequence Diagramm

- Welche Akteure kommunizieren bei der Verwendung des Gadgets?
- Zeigen Sie den Nachrichtenfluss mit Kontrollstrukturen stimmig zu Ihren Klassendiagrammen.

## Erwartungen an die Beschreibungstexte zu den Diagrammen

Das Erstellen der Beschreibungstexte soll die Kommunikation in Ihrem Team fördern. Sie vergewissern sich, dass Sie die Notationsregeln der einzelnen Diagrammtypen verstanden haben und sie sachgemäß zur Modellierung des gewählten Gadgets angewendet haben. Die Beschreibung soll nicht die Symbole der UML-Notation erklären, sondern in allgemeinverständlicher Sprache die Aussagen wiedergeben, die das Diagramm über das Gadget macht, so als würden Sie mit einem Kunden sprechen.

Falls Ihr Diagramm sehr viele Details enthält, soll der Text nicht jedes Detail beschreiben, sondern die wichtigsten Fakten zum Verständnis des Diagramms priorisieren.

## Qualitätskriterien und Bewertung

- Ihre Diagramme machen verständliche Aussagen über das Gadget als System.
- Die Aussagen zum System können durch die beigefügte Bedienungsanleitung bestätigt werden. Es soll keine Widersprüche zwischen der Anleitung und den Aussagen Ihrer Diagramme geben.
- Die UML-Notation der Diagramme ist möglichst fehlerfrei.
- Der Beschreibungstext zu den einzelnen Diagrammen ist stimmig mit der Aussage der Diagramme. Auch hier soll es keine Widersprüche geben.
- Die Beschreibung der Diagramme ist angemessen ausführlich.
- Das erwartete Ergebnis entspricht auch formal den Vorgaben (geforderte Dateien sind vorhanden, die gegebene Struktur wurde eingehalten).
- Die Arbeitsteilung ist angemessen belegt, so dass das Team eine gemeinsame Note erhalten kann.

Ich verwende bei der Sichtung Ihrer Projekte folgende [Checkliste](UML-Projekt-Checkliste.pdf).

### Zusammensetzung der Note für das IAD-Zeugnis

- Mitarbeit und tägliche Bereitstellung der Ergebnisse über GitLab: **20%**
- Team-Projekt: **40%**  
- Eine Klausur auf Papier: **40%**
