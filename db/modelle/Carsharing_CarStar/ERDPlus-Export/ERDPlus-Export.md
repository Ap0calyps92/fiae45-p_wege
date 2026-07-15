# ERDPlus-Export

Nachfolgender code kommt direkt von ERDPlus und sollte nicht ausgeführt werden.

#Meine Version

```sql
CREATE TABLE KUNDE
(
  Kunden_Nr VARCHAR(100) NOT NULL,
  Name VARCHAR(100) NOT NULL,
  Strasse VARCHAR(100) NOT NULL,
  PLZ VARCHAR(5) NOT NULL,
  Ort VARCHAR(100) NOT NULL,
  PRIMARY KEY (Kunden_Nr)
);

CREATE TABLE NUTZER
(
  Nutzer_ID VARCHAR(100) NOT NULL,
  Kunden_Nr VARCHAR(100) NOT NULL,
  PRIMARY KEY (Nutzer_ID),
  FOREIGN KEY (Kunden_Nr) REFERENCES KUNDE(Kunden_Nr)
);

CREATE TABLE RECHNUNG
(
  Rechnungs_Nr VARCHAR(100) NOT NULL,
  Rechnungsdatum DATE NOT NULL,
  Zeitraum_von DATE NOT NULL,
  Zeitraum_bis DATE NOT NULL,
  Monatspauschale NUMERIC(9,2) NOT NULL,
  Kunden_Nr VARCHAR(100) NOT NULL,
  PRIMARY KEY (Rechnungs_Nr),
  FOREIGN KEY (Kunden_Nr) REFERENCES KUNDE(Kunden_Nr)
);

CREATE TABLE FAHRZEUGTYP
(
  Fahrzeugtyp_ID INT NOT NULL,
  Bezeichnung VARCHAR(100) NOT NULL,
  EUR_Std NUMERIC(9,2) NOT NULL,
  EUR_km NUMERIC(9,2) NOT NULL,
  PRIMARY KEY (Fahrzeugtyp_ID)
);

CREATE TABLE FAHRZEUG
(
  Fahrzeug_ID INT NOT NULL,
  Kennzeichen VARCHAR(100) NOT NULL,
  Fahrzeugtyp_ID INT NOT NULL,
  PRIMARY KEY (Fahrzeug_ID),
  FOREIGN KEY (Fahrzeugtyp_ID) REFERENCES FAHRZEUGTYP(Fahrzeugtyp_ID)
);

CREATE TABLE FAHRT
(
  Fahrt_ID INT NOT NULL,
  Abholung_Datum DATE NOT NULL,
  Abholung_Zeit TIME NOT NULL,
  Rueckgabe_Datum DATE NOT NULL,
  Rueckgabe_Zeit TIME NOT NULL,
  Dauer_Std FLOAT NOT NULL,
  Start_km INT NOT NULL,
  Ende_km INT NOT NULL,
  Strecke_km INT NOT NULL,
  Rechnungs_Nr VARCHAR(100) NOT NULL,
  Nutzer_ID VARCHAR(100) NOT NULL,
  Fahrzeug_ID INT NOT NULL,
  PRIMARY KEY (Fahrt_ID),
  FOREIGN KEY (Rechnungs_Nr) REFERENCES RECHNUNG(Rechnungs_Nr),
  FOREIGN KEY (Nutzer_ID) REFERENCES NUTZER(Nutzer_ID),
  FOREIGN KEY (Fahrzeug_ID) REFERENCES FAHRZEUG(Fahrzeug_ID)
);
```

# Alternativ Version

```sql
CREATE TABLE KUNDE
(
  Kunden_Nr VARCHAR(100) NOT NULL,
  Name VARCHAR(100) NOT NULL,
  Strasse VARCHAR(100) NOT NULL,
  PLZ VARCHAR(5) NOT NULL,
  Ort VARCHAR(100) NOT NULL,
  PRIMARY KEY (Kunden_Nr)
);

CREATE TABLE RECHNUNG
(
  Rechnungs_Nr VARCHAR(100) NOT NULL,
  Rechnungsdatum DATE NOT NULL,
  Zeitraum_von DATE NOT NULL,
  Zeitraum_bis DATE NOT NULL,
  Monatspauschale NUMERIC(9,2) NOT NULL,
  Kunden_Nr VARCHAR(100) NOT NULL,
  PRIMARY KEY (Rechnungs_Nr),
  FOREIGN KEY (Kunden_Nr) REFERENCES KUNDE(Kunden_Nr)
);

CREATE TABLE NUTZER
(
  Nutzer_ID VARCHAR(100) NOT NULL,
  Kunden_Nr VARCHAR(100) NOT NULL,
  PRIMARY KEY (Nutzer_ID),
  FOREIGN KEY (Kunden_Nr) REFERENCES KUNDE(Kunden_Nr)
);

CREATE TABLE FAHRZEUGTYP
(
  Fahrzeugtyp_ID INT NOT NULL,
  Bezeichnung VARCHAR(100) NOT NULL,
  EUR_Std NUMERIC(9,2) NOT NULL,
  EUR_km NUMERIC(9,2) NOT NULL,
  PRIMARY KEY (Fahrzeugtyp_ID)
);

CREATE TABLE FAHRZEUG
(
  Fahrzeug_ID INT NOT NULL,
  Kennzeichen VARCHAR(100) NOT NULL,
  Fahrzeugtyp_ID INT NOT NULL,
  PRIMARY KEY (Fahrzeug_ID),
  FOREIGN KEY (Fahrzeugtyp_ID) REFERENCES FAHRZEUGTYP(Fahrzeugtyp_ID)
);

CREATE TABLE FAHRT
(
  Fahrt_ID INT NOT NULL,
  Abholung DATETIME NOT NULL,
  Rueckgabe DATETIME,
  Dauer_Std FLOAT,
  Start_km INT NOT NULL,
  Ende_km INT,
  Strecke_km INT,
  EUR_Std NUMERIC(9,2) NOT NULL,
  EUR_km NUMERIC(9,2) NOT NULL,
  Nutzer_ID VARCHAR(100) NOT NULL,
  Fahrzeug_ID INT NOT NULL,
  PRIMARY KEY (Fahrt_ID),
  FOREIGN KEY (Nutzer_ID) REFERENCES NUTZER(Nutzer_ID),
  FOREIGN KEY (Fahrzeug_ID) REFERENCES FAHRZEUG(Fahrzeug_ID)
);
```
