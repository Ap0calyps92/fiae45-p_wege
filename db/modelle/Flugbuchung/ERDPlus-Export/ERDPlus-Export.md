# ERDPlus-Export

Hier der generierte ERDPlus Code, der nicht ausgeführt werden sollte... Dieser basiert auf der version von HG_Roeder und nicht auf meiner auf den Bildern!

```sql
CREATE TABLE PERSON
(
  Person_ID INT NOT NULL,
  Vorname VARCHAR(100) NOT NULL,
  Nachname VARCHAR(100) NOT NULL,
  Geburtsdatum DATE NOT NULL,
  PRIMARY KEY (Person_ID)
);

CREATE TABLE KUNDE
(
  Kundennummer CHAR(5) NOT NULL,
  Strasse VARCHAR(100) NOT NULL,
  PLZ VARCHAR(100) NOT NULL,
  Ort VARCHAR(100) NOT NULL,
  Person_ID INT NOT NULL,
  PRIMARY KEY (Kundennummer),
  FOREIGN KEY (Person_ID) REFERENCES PERSON(Person_ID)
);

CREATE TABLE FLUGHAFEN
(
  Flughafen_Code CHAR(3) NOT NULL,
  Flughafen_Name VARCHAR(100) NOT NULL,
  PRIMARY KEY (Flughafen_Code)
);

CREATE TABLE FLUGVERBINDUNG
(
  Flugnummer CHAR(10) NOT NULL,
  Abflugzeit TIME NOT NULL,
  Ankunftzeit TIME NOT NULL,
  Preis NUMERIC(9,2) NOT NULL,
  Abflughafen_Code CHAR(3) NOT NULL,
  Zielflughafen_Code CHAR(3) NOT NULL,
  PRIMARY KEY (Flugnummer),
  FOREIGN KEY (Abflughafen_Code) REFERENCES FLUGHAFEN(Flughafen_Code),
  FOREIGN KEY (Zielflughafen_Code) REFERENCES FLUGHAFEN(Flughafen_Code)
);

CREATE TABLE VERKEHRSTAG
(
  Datum DATE NOT NULL,
  PRIMARY KEY (Datum)
);

CREATE TABLE FLUG
(
  Flugnummer CHAR(10) NOT NULL,
  Datum DATE NOT NULL,
  PRIMARY KEY (Flugnummer, Datum),
  FOREIGN KEY (Flugnummer) REFERENCES FLUGVERBINDUNG(Flugnummer),
  FOREIGN KEY (Datum) REFERENCES VERKEHRSTAG(Datum)
);

CREATE TABLE BUCHUNG
(
  Buchung_ID BIGINT NOT NULL,
  Buchungsdatum DATE NOT NULL,
  Kundennummer CHAR(5) NOT NULL,
  PRIMARY KEY (Buchung_ID),
  FOREIGN KEY (Kundennummer) REFERENCES KUNDE(Kundennummer)
);

CREATE TABLE BUCHUNGSPOSTEN
(
  Buchung_ID BIGINT NOT NULL,
  Person_ID INT NOT NULL,
  Flugnummer CHAR(10) NOT NULL,
  Datum DATE NOT NULL,
  PRIMARY KEY (Buchung_ID, Person_ID, Flugnummer, Datum),
  FOREIGN KEY (Buchung_ID) REFERENCES BUCHUNG(Buchung_ID),
  FOREIGN KEY (Person_ID) REFERENCES PERSON(Person_ID),
  FOREIGN KEY (Flugnummer, Datum) REFERENCES FLUG(Flugnummer, Datum)
);
```
