# State-Diagramme

Zu diesem Diagrammtyp haben wir zwei Diagramme erstellt: die Zustände eines Touch
Plus-Controllers und die Ladezustände des Akkus im Headset.

## 1. Controller

### Kurze Zusammenfassung des Diagramminhalts

Das Diagramm zeigt, in welchen Zuständen sich ein Touch Plus-Controller befinden kann,
wodurch er von einem Zustand in den nächsten wechselt und wie er seinen jeweiligen
Zustand über seine LED anzeigt.

### Diagramm

![State Diagramm Controller](png/4-1-State-Diagram.png)

### Beschreibungstext

Zu Beginn ist der Controller ausgeschaltet. Wird er eingeschaltet, hängt es davon ab,
ob er bereits mit dem Headset gekoppelt ist. Ist er noch nicht gekoppelt, ist er
zunächst nur bereit und zeigt dies durch weißes Blinken an. Ist er bereits gekoppelt,
verbindet er sich automatisch mit dem Headset.

Aus dem bereiten Zustand kann der Nutzer den Kopplungsmodus starten, indem er die
entsprechenden Tasten gedrückt hält. Im Kopplungsmodus blinkt die LED wiederholt
zweimal. Sobald die Verbindung mit dem Headset hergestellt ist, gilt der Controller
als gekoppelt und ist verbunden, was die LED durch einmaliges Blinken anzeigt. Wird der
Controller wieder entkoppelt, kehrt er in den bereiten Zustand zurück.

Solange der Controller eingeschaltet ist, also egal ob er gerade bereit, im
Kopplungsmodus oder verbunden ist, können zwei Situationen eintreten. Ist die Batterie
leer, erlischt die LED und der Controller kann nicht mehr verwendet werden. Tritt ein
Fehler auf, zeigt die LED ein SOS-Signal. In beiden Fällen hilft es, die Batterie
herauszunehmen und wieder einzusetzen bzw. durch eine neue zu ersetzen. Danach ist der
Controller wieder ausgeschaltet und kann erneut gestartet werden.

## 2. Akku

### Kurze Zusammenfassung des Diagramminhalts

Das Diagramm zeigt die Ladezustände des fest eingebauten Akkus der Meta Quest 3 und
wie die Status-LED am Headset den jeweiligen Zustand anzeigt.

### Diagramm

![State Diagramm Akku](png/4-2-State-Diagram.png)

### Beschreibungstext

Zu Beginn ist das Headset nicht an ein Netzteil angeschlossen. Wird es angeschlossen,
beginnt der Akku zu laden und die Status-LED leuchtet orange. Ist der Akku vollständig
geladen, wechselt die LED auf grün. Wird das Netzteil abgezogen, egal ob während des
Ladens oder danach, ist das Headset wieder nicht angeschlossen.

Wird das Headset ohne Netzteil benutzt, bis der Akku vollständig entladen ist, zeigt
die Status-LED rot. Sobald das Headset dann wieder an das Netzteil angeschlossen wird,
beginnt der Ladevorgang erneut.
