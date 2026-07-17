# ERDPlus SQL Export

Hier der generierte Code aus ERDPlus, er sollte nicht ausgeführt werden ohne dass sichergestellt wird in welche Datenbank geschrieben wird.

```sql
CREATE TABLE Patient
(
  PatientNr INT NOT NULL,
  Nachname VARCHAR(100) NOT NULL,
  Vorname VARCHAR(100) NOT NULL,
  Strasse VARCHAR(100) NOT NULL,
  PLZ CHAR(5) NOT NULL,
  Ort VARCHAR(100) NOT NULL,
  PRIMARY KEY (PatientNr)
);

CREATE TABLE Arzt
(
  ArztNr INT NOT NULL,
  Name VARCHAR(100) NOT NULL,
  Faktor NUMERIC(3,1) NOT NULL,
  PRIMARY KEY (ArztNr)
);

CREATE TABLE MedLeistung
(
  MedLeistungNr INT NOT NULL,
  Bezeichnung VARCHAR(100) NOT NULL,
  Preis NUMERIC(9,2) NOT NULL,
  PRIMARY KEY (MedLeistungNr)
);

CREATE TABLE ZusatzLeistung
(
  ZusatzLeistungNr VARCHAR(5) NOT NULL,
  Bezeichnung VARCHAR(100) NOT NULL,
  Tagespreis NUMERIC(9,2) NOT NULL,
  PRIMARY KEY (ZusatzLeistungNr)
);

CREATE TABLE ErbrachteMedLeistung
(
  ErbrachteMedLeistungID INT NOT NULL,
  Leistungsdatum DATE NOT NULL,
  MedLeistungNr INT NOT NULL,
  ArztNr INT NOT NULL,
  PatientNr INT NOT NULL,
  PRIMARY KEY (ErbrachteMedLeistungID),
  FOREIGN KEY (MedLeistungNr) REFERENCES MedLeistung(MedLeistungNr),
  FOREIGN KEY (ArztNr) REFERENCES Arzt(ArztNr),
  FOREIGN KEY (PatientNr) REFERENCES Patient(PatientNr)
);

CREATE TABLE ErbrachteZusatzleistung
(
  LeistungVon DATE NOT NULL,
  LeistungBis DATE NOT NULL,
  ZusatzLeistungNr VARCHAR(5) NOT NULL,
  PatientNr INT NOT NULL,
  PRIMARY KEY (LeistungVon, ZusatzLeistungNr, PatientNr),
  FOREIGN KEY (ZusatzLeistungNr) REFERENCES ZusatzLeistung(ZusatzLeistungNr),
  FOREIGN KEY (PatientNr) REFERENCES Patient(PatientNr)
);
```
