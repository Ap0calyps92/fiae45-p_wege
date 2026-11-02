# Sequence-Diagramm

## Kurze Zusammenfassung des Diagramminhalts

Das Diagramm zeigt, wie der Kontoinhaber einen Controller über die Meta Horizon-App mit
dem Headset koppelt und welche Nachrichten dabei zwischen App, Headset und Controller
ausgetauscht werden.

## Diagramm

![Sequence Diagramm](png/5-Sequence-Diagramm.png)

## Beschreibungstext

Der Kontoinhaber wählt in der Meta Horizon-App aus, dass er einen Controller, hier den
rechten, koppeln möchte. Die App fragt zuerst beim Headset nach, ob es eingeschaltet
ist, denn nur dann kann die Kopplung gelingen.

Ist das Headset eingeschaltet, beauftragt die App das Headset, den Controller zu
koppeln. Der Kontoinhaber hält nun am Controller die vorgesehenen Tasten gedrückt,
wodurch der Controller in den Kopplungsmodus wechselt. Darauf muss er nicht warten,
er drückt nur die Tasten. Das Headset nimmt daraufhin die Verbindung zum Controller
auf, und der Controller bestätigt die erfolgreiche Verbindung. Das Headset meldet der
App, dass die Kopplung geklappt hat, und die App zeigt dem Kontoinhaber das Ergebnis
an.

Ist das Headset dagegen nicht eingeschaltet, findet keine Kopplung statt. Die App
teilt dem Kontoinhaber direkt mit, dass der Controller nicht gekoppelt werden konnte.