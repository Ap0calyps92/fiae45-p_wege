# Sequence Diagramm

Das Sequenzdiagramm zeigt, wie Objekte miteinander Nachrichten austauschen. Wenn ein Klassendiagramm zur Aufgabe vorliegt, können Sie daraus entnehmen, welche Nachrichten möglich sind: Eine Nachricht ist der Aufruf einer Operation am Objekt der Klasse. Hat die Operation einen Rückgabewert, so ist eine **synchrone** Nachricht erforderlich, zu der eine Antwortnachricht mit dem Rückgabewert notiert werden muss. Bei Selbstaufrufen kann das Zeichnen der Antwortnachricht eventuell entfallen.

Eine Operation, die keinen Rückgabewert hat, kann mit einer **asynchronen** Nachricht aufgerufen werden.

Die Arten der Nachrichten werden durch **unterschiedliche Pfeilspitzen und Linien** der Pfeile ausgedrückt. Auf die richtige Pfeilspitze und Linie ist deshalb besonders zu achten. Für Destruktionsnachrichten können unterschiedliche Arten von Nachrichten verwendet werden. Hier ist wichtig, dass an der Pfeilspitze die Lebenslinie des Empfängers mit einem X endet.

Objekte, die Nachrichten empfangen, werden aktiv. Das zeigt sich in **Aktivierungsbalken** auf der Lebenslinie des Objekts.

**Interaktionsrahmen** zeigen, ob Nachrichten nur unter Bedingungen oder in Schleife ausgeführt werden. Die Bedingungen der Ausführung sind als boolesche Ausdrücke in eckigen Klammern zu notieren. Die Art der Interaktion steht in der linken oberen Ecke des Interaktionsrahmens. Häufig gebraucht sind: **OPT** (bedingt, ohne sonst), **ALT** (if mit else, evtl. mit else if), **LOOP** (Schleife).
