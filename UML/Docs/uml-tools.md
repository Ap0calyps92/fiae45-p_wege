# Werkzeuge zur Erstellung von UML-Diagrammen

Für den Unterricht brauchen wir ein Tool, das mit möglichst einfacher Bedienung Diagramme in gültiger UML-Notation erstellen kann. **UMLet** erfüllt diese Anforderung ausgezeichnet. Andere Werkzeuge sind oft zu komplex in der Bedienung oder unterstützen die Notation nicht ausreichend, weil z. Bsp. nicht verschiedene Arten von Pfeilspitzen unterschieden werden.

Wir verwenden also im Unterricht UMLet. Ich empfehle Ihnen, im Praktikum ein Profi **CASE-Tool** zu testen (Empfehlungen hierzu unten auf der Seite).

**CASE** steht für *Computer-Aided Systems-Engineering*. Solche Programme können mehr als nur UML-Diagramme erstellen, z. B. aus UML-Diagrammen Programm-Code erzeugen oder vorhandenen Programm-Code mit UML-Diagrammen erklären. Letzteres nennt man auch *Reverse-Engineering*.

## UMLet, unser UML-Tool für den Unterricht

**UMLet** speichert im eigenen **UXF**-Format und exportiert **PNG**- und **PDF**-Dateien. Es ist verfügbar als [VSCode Extension](https://marketplace.visualstudio.com/items?itemName=TheUMLetTeam.umlet), als Online-Tool [UMLetino](https://umletino.com/), als Plugin für die Eclipse IDE und als Java-basiertes Desktop-Programm [UMLet](https://www.umlet.com)

**Wichtig:** FÜr die Diagrammtypen [Activity](../Umlet-Paletten/IAD%20Activity.uxf), [State](../Umlet-Paletten/IAD%20State%20Machine.uxf) und [Sequence](../Umlet-Paletten/IAD%20Sequence.uxf) finden Sie im Ordner *Umlet-Paletten* alternative Werkzeugpaletten für UMLet als Fehlerkorrektur oder zur Bereitstellung nützlicher Zeichenobjekte. Prüfen Sie immer, ob die angebotenen Objekte die Notationsregeln des Diagrammtyps erfüllen.

- In VSCode mit UMLet VSCode-Extension
  - [https://marketplace.visualstudio.com/items?itemName=TheUMLetTeam.umlet](https://marketplace.visualstudio.com/items?itemName=TheUMLetTeam.umlet)
  - Export-Funktionen über Befehls-Palette mit Stichwort UMLet
- Alternativ UMLetino im Browser
  - [https://umletino.com/](https://umletino.com/)
- oder UMLet Desktop Programm (erfordert Java Runtime)
  - [https://www.umlet.com](https://www.umlet.com)

  - Portfolio von mit UMLet erstellten Beispieldieagrammen
    - [https://www.itmeyer.at/umlet/uml2/](https://www.itmeyer.at/umlet/uml2/)
    - Diese Seite präsentiert Beispiel-Zeichnungen, nicht in jedem Fall Muster für einwandfreie Umsetzung der UML-Notation.

## Professionelle CASE-Tools

mit Empfehlung zum Testen im Praktikum:

### StarUML

- [https://staruml.io/](https://staruml.io/)
- ab $129
- 30-Tage Demo verfügbar
- Code Generierung mittels Extensions
- Soll einen leichten Einstieg in Case-Tools bieten.

### Altova UModel

- [https://www.altova.com/umodel](https://www.altova.com/umodel)
- ab €179
- 30-Tage Demo verfügbar, benötigt Aktivierungscode
- Empfehlenswert wegen seiner Integration mit anderen Altova Programmen.

### Visual Paradigm

- [https://www.visual-paradigm.com/](https://www.visual-paradigm.com/)
- ab $99 - $1999
- Community Edition (frei nach Aktivierung)
- [https://www.visual-paradigm.com/download/community.jsp](https://www.visual-paradigm.com/download/community.jsp)

### Enterprise Architect

- [https://www.sparxsystems.de/enterprise-architect/](https://www.sparxsystems.de/enterprise-architect/)
- Lizenzen von €225 — €879
- 30 Tage Testversion verfügbar

## Weitere populäre Diagrammtools

...nicht für dieses Unterrichtsmodul!

### PlantUML

Diagrammerstellung ist texttbasiert, das heißt sie erfordert zusätzlich zum Erlernen der graphischen Notation das Erlernen der Editor-Befehle.

Die Darstellung der Diagramme weicht teilweise vom Standard ab.

Als textbasiertes und barrierefreies Werkzeug wird PlantUML von blinden oder stark sehbehinderten Fachinformatikern benutzt, wie etwa in der Marburger Blindenstudienanstalt.

- [https://editor.plantuml.com/](https://editor.plantuml.com/)
- [https://www.planttext.com/](https://www.planttext.com/)

### Mermaid

- [https://mermaid.ai/](https://mermaid.ai/)
- Das Aktivitätsdiagramm ist nicht unterstützt.
- Die Diagrammerstellung Text-basiert und neuerdings KI-gesteuert.

### Dia

- [http://dia-installer.de/](http://dia-installer.de/)
- Zeichenprogramm.
- Nicht empfohlen bei strenger Betrachtung der UML-Notation

### ArgoUML

- [https://argouml-tigris-org.github.io/tigris/argouml/](https://argouml-tigris-org.github.io/tigris/argouml/)
- Java-basiertes Case Tool für UML 1.4
- Wurde einmal im FI Kurs eingesetzt und wegen nerviger GUI aufgegeben.
