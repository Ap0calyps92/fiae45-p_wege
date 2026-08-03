# Datenbanken Tag 1
## Themen für die Woche
Mo, Di, => Git, Markdown <br>
Fr => DP-900 Azure Daten Grundlagen

Datenbank Modellierung
- Entity Relationship Model (ER-Modell)
- Relation Modell (UML-Klassendiagramm)
- Normalisierung
- Anomalien
- SQL-Abfragen

Was geht in die Noten ein?
2 Klausuren
20% tägliche Mitarbeit und Notizen => täglicher Commit und Push, rest die Klausuren

Für Projektdokumentationen:
keine Darkmode Screenshots!

## Warnhinweise zu Git:
- Git vergisst nichts
- Git Repositories können nicht verschachtelt werden

## Zustände von Dateien in Git
- Untracked (U) • nicht von Git beobachtet
- Staged, Index Added (A) • geaddet nach Hinzufügen oder Änderung
- Modified (M) • geändert seit letztem Add oder Commit
- Unchanged (keine Markierung) • Keine Änderung seit Commit

## Befehle
- git init • neues Repository im aktuellen Ordner erstellen
- git clone `<url>` • bestehendes Repository kopieren
---
- git add `<datei>` • Datei zum Staging Bereich hinzufügen
- git add . • alle geänderten / neuen Dateien hinzufügen
- git rm --cached `<datei>` • Datei aus dem Staging entfernen
- git status • zeigt aktuelle Zustände aller Dateien
- git diff • zeigt genaue Änderungen im Vergleich zum letzten Commit
- git restore `<Datei>`
- git restore --staged `<Datei>` • Staging wird zurückgenommen
---
- git commit -m "`<message>`" • speichert Snapshot mit einer Message
- git log • Historie aller Commits anzeigen
- git log --oneline • kompakte Historie
---
- git push • lokale Commits zum Remote-Repository hochladen
- git pull • Änderungen vom Remote-Repository holen und einfügen
- git fetch • Änderungen vom Remote holen, aber nicht einfügen
---
- git branch • Zeigt vorhandene Branches
- git branch `<name>` • neuen Branch erstellen
- git checkout `<name>` / git switch `<name>` • zu Branch wechseln
- git merge `<name>` • Branch in aktuellen Branch einfügen
---
- git remote -v • zeigt verknüpfte Remote-Repositories
- git config --global user.name "Name" • Nutzername global setzen
- git config --global user.email "mail@..." • Email global setzen