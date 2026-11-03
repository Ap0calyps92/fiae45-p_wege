# Unterrichtsmaterialien – Fachinformatiker Anwendungsentwicklung (Umschulung)

Dieses Repository enthält meine Unterlagen, Übungen und Notizen aus der Umschulung zum **Fachinformatiker für Anwendungsentwicklung**.

Das Repo wird parallel auf **GitLab** und **GitHub** gepflegt.

## 📚 Inhalte

| Bereich | Themen |
|---|---|
| **Datenbanken** | ER-Modellierung (Entity → Primärschlüssel → Attribute → Relationenschema), Normalisierung, T-SQL (DDL/DML, JOINs, Unterabfragen, PIVOT/UNPIVOT, Window Functions, Transaktionen), JSON/XML-Export, Backup & Wiederherstellung |
| **UML** | Use-Case-, Aktivitäts-, Klassen-, Zustands- und Sequenzdiagramme mit UMLet, Übungsaufgaben und Gruppenprojekt |

Weitere Themenbereiche aus der Umschulung (OOP in Python & C#, Netzwerktechnik, digitale Prozesse, WiSo/Recht) kommen im Verlauf dazu.

## 🗂 Struktur

```text
├── db/
│   ├── markdown-uebung/           # Einstieg: Markdown-Übung
│   ├── modelle/                   # Datenbankmodellierung (je Projekt: ERDPlus → SQL → Notebooks)
│   │   ├── Bikeshop/
│   │   ├── Carsharing_CarStar/
│   │   ├── Flugbuchung/
│   │   ├── Getraenkebestellung/
│   │   ├── Immobilien/
│   │   └── MacFitt/
│   ├── notizen/                   # Tagesnotizen aus dem Unterricht
│   └── sql-praxis/                # SQL-Abfragen an fertigen Datenbanken
│       ├── BikeShop Abfragen/
│       ├── Delikatessen-Abfragen/
│       ├── Töpfermarkt-Abfragen/
│       ├── Protokoll/             # Unterrichtsprotokoll Tag 1–9
│       └── sql-praxis.code-workspace
│
├── DB-Klausur-P_Wege/             # Klausur Datenbanken: Patienten-Abrechnungssystem
│   ├── erdplus/                   # ER-Modell in 4 Schritten
│   ├── png/
│   ├── A5_SQL-Export-P_Wege.md
│   ├── A6_DB-Objekte-P_Wege.ipynb
│   ├── A7_Daten-P_Wege.ipynb
│   ├── A8_Abfragen-Views-P_Wege.ipynb
│   └── Protokoll-P_Wege.md
│
├── UML/
│   ├── Docs/                      # Belegsätze, Checklisten, Projektvorgaben, Tools
│   ├── Praxis/                    # Übungsaufgaben nach Diagrammtyp
│   │   ├── _Bilder/               # Aufgabenstellungen
│   │   ├── 1-Use-Case/
│   │   ├── 2-Activity/
│   │   ├── 3-Class/
│   │   ├── 4-State/
│   │   └── 5-Sequence/
│   ├── Projekt/                   # Gruppenprojekt „VR-Ausrüstung“ (Meta Quest 3)
│   │   ├── bedienungsanleitung/   # Quellen (Meta-Hilfeseiten, Sicherheitshinweise)
│   │   ├── uxf/                   # UMLet-Dateien
│   │   ├── png/
│   │   ├── pdf/
│   │   ├── 1-Use-Case-Diagram.md … 5-Sequence-Diagram.md
│   │   └── Arbeitsteilung.md
│   ├── Referenz/                  # UML-2.5.1-Spezifikation, Notationsübersicht, Poster, Zusammenfassung
│   ├── Umlet-Paletten/            # Eigene UMLet-Paletten (Activity, Sequence, State Machine)
│   └── UML.md
│
├── .gitignore
└── README.md
```

## 🗄 Datenbanken

**Modelle** (`db/modelle/`) – Jedes Projekt folgt demselben Ablauf:

1. ER-Modell in ERDPlus, schrittweise: Entitäten → Primärschlüssel → Attribute → Relationenschema
2. SQL-Export aus ERDPlus (`ERDPlus-Export.md`)
3. Datenbankobjekte anlegen (`Datenbank-Objekte.ipynb`)
4. Testdaten erfassen (`Datenerfassung.ipynb`)

Projekte: Bikeshop, Carsharing (CarStar), Flugbuchung, Getränkebestellung, Immobilien, MacFitt (Fitnessstudio)

**SQL-Praxis** (`db/sql-praxis/`) – Abfrageübungen an vorgegebenen Datenbanken (Backups als `.bak`):

- **BikeShop** – Kunden & Bestellungen, Mitarbeiter, Produktkategorien/-typen, PIVOT/UNPIVOT
- **Delikatessen** – Lieferanten, Kunden, Mitarbeiter, Artikel, Prozentberechnungen, Unterabfragen
- **Töpfermarkt** – Abfragen und Datenänderungen (INSERT/UPDATE/DELETE)
- **Protokoll** – Unterrichtsprotokolle Tag 1–9, u. a. JSON-/XML-Ausgabe

**Klausur** (`DB-Klausur-P_Wege/`) – Patienten-Abrechnungssystem: ER-Modell, SQL-Export, Datenbankobjekte, Daten, Abfragen & Views.

## 📐 UML

**Praxis** (`UML/Praxis/`) – Je Aufgabe UMLet-Datei (`.uxf`) plus PNG/PDF-Export:

| Diagrammtyp | Aufgaben |
|---|---|
| Use Case | Helpdesk, Schließsystem, Webshop, Terminbuchung, Gebäudemanagement, Helferlein-Webanwendung, Lagerverwaltung |
| Aktivität | Rechnungseingang, Onlineshop, Fingerabdruck, EC-Automat, Bewässerung, Brauerei |
| Klasse | Kunden, Getränke, Beziehungen, Kursrechnung, Helferlein (Proxy-Pattern) |
| Zustand | Trainingsgerät, Ladegerät, Immobilienverkauf, Lichtsteuerung, Impfzentrum |
| Sequenz | Trainingsgerät, Solaranlage, Helferlein |

**Projekt** (`UML/Projekt/`) – Gruppenprojekt zur **Meta Quest 3**, modelliert in allen fünf Diagrammtypen. Alle Inhalte stützen sich auf öffentlich zugängliche Herstellerdokumentation (siehe `bedienungsanleitung/`). Pro Diagrammtyp gibt es eine Markdown-Datei mit Erläuterung; die Aufgabenverteilung steht in `Arbeitsteilung.md`.

## 🎯 Zweck

- persönliche Lern- und Nachschlagesammlung
- Versionierung von Übungsaufgaben und Projekten
- Vorbereitung auf Prüfungen (Zwischen- und Abschlussprüfung)

## 🛠 Verwendete Tools

- **Visual Studio Code** – SQL-Notebooks (`.ipynb`), UMLet-Extension
- **SQL Server** / T-SQL
- **ERDPlus** (ER-Modelle)
- **UMLet** (UML-Diagramme)
- **Jupyter Book** (`_config.yml` / `_toc.yml`)
- **Git**, GitLab & GitHub

## 📄 Lizenz

Privates Lern- und Übungsrepository. Keine kommerzielle Nutzung vorgesehen.