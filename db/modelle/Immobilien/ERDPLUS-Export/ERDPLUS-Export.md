# ERDPLUS-Export

Nachfolgender SQL-Code wurde von ERDPlus generiert und darf so nicht ausgeführt werden, weil die Angabe fehlt, in welche Datenbank geschrieben wird:

```sql
CREATE TABLE EIGENTUEMER
(
  Eigentuemer_ID INT NOT NULL,
  Name VARCHAR(100) NOT NULL,
  Strasse VARCHAR(100) NOT NULL,
  PLZ VARCHAR(5) NOT NULL,
  Ort VARCHAR(100) NOT NULL,
  PRIMARY KEY (Eigentuemer_ID)
);

CREATE TABLE IMMOBILIE
(
  Immobilie_ID INT NOT NULL,
  Name VARCHAR(100) NOT NULL,
  Strasse VARCHAR(100) NOT NULL,
  PLZ VARCHAR(5) NOT NULL,
  Ort VARCHAR(100) NOT NULL,
  Eigentuemer_ID INT NOT NULL,
  PRIMARY KEY (Immobilie_ID),
  FOREIGN KEY (Eigentuemer_ID) REFERENCES EIGENTUEMER(Eigentuemer_ID)
);

CREATE TABLE MAKLER
(
  Makler_ID INT NOT NULL,
  Name VARCHAR(100) NOT NULL,
  Telefon VARCHAR(100) NOT NULL,
  PRIMARY KEY (Makler_ID)
);

CREATE TABLE KUNDE
(
  Kunde_ID INT NOT NULL,
  Name VARCHAR(100) NOT NULL,
  Strasse VARCHAR(100) NOT NULL,
  PLZ VARCHAR(5) NOT NULL,
  Ort VARCHAR(100) NOT NULL,
  PRIMARY KEY (Kunde_ID)
);

CREATE TABLE BESICHTIGUNG
(
  Besichtigung_ID INT NOT NULL,
  Besuchstermin DATE NOT NULL,
  Immobilie_ID INT NOT NULL,
  Makler_ID INT NOT NULL,
  Kunde_ID INT NOT NULL,
  PRIMARY KEY (Besichtigung_ID),
  FOREIGN KEY (Immobilie_ID) REFERENCES IMMOBILIE(Immobilie_ID),
  FOREIGN KEY (Makler_ID) REFERENCES MAKLER(Makler_ID),
  FOREIGN KEY (Kunde_ID) REFERENCES KUNDE(Kunde_ID)
);
```
