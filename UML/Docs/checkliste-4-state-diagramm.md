# Checkliste: State Diagramm

- Verbindungspfeile zwischen Zuständen heißen Transitionen. 
- Mehrer Transitionen können zu einem Zustand hin oder heraus führen. 
- Es gibt auch Selbst-Transitionen, die zum selben Zustand zurück führen. 
- An der ersten Transition darf keine Bedingung stehen.

- Eine Transition ohne Angabe von Auslöser oder Bedingung findet automatisch und sofort statt. Achten Sie entsprechend darauf, alle Transitionen zu beschriften.
- Bedingungen an Transitionen stehen als boolesche Ausdrücke in eckigen Klammern (wie im Aktivitäts-Diagramm).

Gibt es ein Klassendiagramm zur Aufgabe? Das sollte wichtige Hinweise für Ihr Zustandsdiagramm enthalten:

- Verschiedene Werte eines Attributs der Klasse bedeuten unterschiedliche Zustände eines Objekts.
- Aufrufe von Operationen können Attributwerte verändern und Transitionen auslösen.
