# ERDPLUS-Export

Nachfolgender SQL-Code wurde von ERDPlus generiert und darf so nicht ausgeführt werden, weil die Angabe fehlt, in welche Datenbank geschrieben wird:
```sql
CREATE TABLE LIEFERANT
(
  Lieferant_ID INT NOT NULL,
  Name VARCHAR(100) NOT NULL,
  Straße VARCHAR(100) NOT NULL,
  PLZ VARCHAR(100) NOT NULL,
  Ort VARCHAR(100) NOT NULL,
  PRIMARY KEY (Lieferant_ID)
);

CREATE TABLE BESTELLUNG
(
  Bestell_ID INT NOT NULL,
  Datum DATE NOT NULL,
  Lieferant_ID INT NOT NULL,
  PRIMARY KEY (Bestell_ID),
  FOREIGN KEY (Lieferant_ID) REFERENCES LIEFERANT(Lieferant_ID)
);

CREATE TABLE ARTIKEL
(
  Artikel_ID INT NOT NULL,
  Bezeichnung VARCHAR(100) NOT NULL,
  UVP NUMERIC(9,2) NOT NULL,
  Gebinde VARCHAR(100) NOT NULL,
  PRIMARY KEY (Artikel_ID)
);

CREATE TABLE ENTHäLT
(
  Menge INT NOT NULL,
  Einzelpreis NUMERIC(9,2) NOT NULL,
  Bestell_ID INT NOT NULL,
  Artikel_ID INT NOT NULL,
  PRIMARY KEY (Bestell_ID, Artikel_ID),
  FOREIGN KEY (Bestell_ID) REFERENCES BESTELLUNG(Bestell_ID),
  FOREIGN KEY (Artikel_ID) REFERENCES ARTIKEL(Artikel_ID)
);

CREATE TABLE BIETET_AN
(
  Angebotspreis NUMERIC(9,2) NOT NULL,
  Lieferant_ID INT NOT NULL,
  Artikel_ID INT NOT NULL,
  PRIMARY KEY (Lieferant_ID, Artikel_ID),
  FOREIGN KEY (Lieferant_ID) REFERENCES LIEFERANT(Lieferant_ID),
  FOREIGN KEY (Artikel_ID) REFERENCES ARTIKEL(Artikel_ID)
);
```
