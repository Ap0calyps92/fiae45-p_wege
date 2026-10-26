# Checkliste: Use Case Diagramm

- Akteure werden immer außerhalb des Systemrahmens gezeichnet.

- Identifizieren Sie als erstes die Akteure, die in den Anforderungen genannt werden. Wenn Akteure gemeinsame Anwendungsfälle haben, könnten sie voneinander erben oder beide von einem abstrakten Akteur erben. Das ist genau zu untersuchen.

- Für einen erbenden Akteur werden keine Assoziationen zu den Anwendungsfällen gezeichnet, mit denen der übergeordnete Akteur verbunden ist.

- Es gibt auch Vererbung zwischen Anwendungsfällen. Diese kommt, zumindest in IHK-Aufgaben, sehr selten vor.

- Suchen Sie in der Formulierung der Aufgabe nach Hinweisen auf «include» und «extend» Beziehungen. Je nach Formulierung kann zum Beispiel ein Login das Eine oder das Andere sein!

- Untersuchen Sie genau, ob ein Anwendungsfall als INCLUDE oder EXTEND zu behandeln ist.
  - Ein INCLUDE wird ausnahmslos immer ausgeführt, um den übergeordneten Anwendungsfall zu vervollständigen. Der gestrichelte Pfeil zeigt auf den inkludierten Anwendungsfall.
  - Ein EXTEND wird nur dann ausgeführt, wenn eine Bedingung wahr wird. Die Bedingung wird als boolescher Ausdruck als "condition" in einer Notiz an die Beziehung geheftet. Der gestrichelte Pfeil zeigt auf den Erweiterungspunkt im übergeordneten Anwendungsfall.

- Es ist nicht Zweck des Use Case Diagramms, Reihenfolgen von Abläufen darzustellen. Dazu würde man ein Aktivitätsdiagramm nehmen.
