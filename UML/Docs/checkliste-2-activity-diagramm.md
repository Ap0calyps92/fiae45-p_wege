# Checkliste: Activity Diagramm

- Jede Aktion im Diagramm soll eindeutig sein. Über entsprechende Kanten und Zusammenführungen kann die gleiche Akton mehrfach ausgeführt werden. Sprungmarken helfen, das Überschneiden von Kanten zu vermeiden.

- In jede Aktion darf nur eine Kante hinein und eine herausführen. Sollen mehrere Kanten zu einer Aktion hinführen, dann ist eine Raute zur Zusammenführung erforderlich.

- Die Bedingungen an Kanten nach Entscheidungsknoten müssen sich gegenseitig ausschließen und alle Fälle abdecken. Sie müssen als boolesche Ausdrücke in eckigen Klammern notiert werden.

- Werden in den Anforderungen verschiedene Akteure unterschieden und sollen Aktionen zuständigen Akteuren zugewiesen werden, dann zeichnen Sie hierzu Swimlanes in Ihr Diagramm.

- Wird gefordert, dass Aktionen gleichzeitig ablaufen, dann brauchen Sie schwarze Balken als Splitting und später als Synchronisation.

- Endet ein Informationsfluss, aber die Aktivität geht weiter, zeichnen sie einen ablaufenden Knoten (x im Kreis).
Endet die ganze Aktivität, zeichnen Sie einen Endknoten (schwarzer Punkt im Kreis).
