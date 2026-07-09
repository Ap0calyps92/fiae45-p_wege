# ERDPLUS-Export

Nachfolgender SQL-Code wurde von ERDPlus generiert und darf so nicht ausgeführt werden, weil die Angabe fehlt, in welche Datenbank geschrieben wird:

```sql
CREATE TABLE KUNDE
(
  KundenNr INT NOT NULL,
  Firma VARCHAR(100),
  Vorname VARCHAR(100) NOT NULL,
  Nachname VARCHAR(100) NOT NULL,
  Straße VARCHAR(100) NOT NULL,
  PLZ VARCHAR(5) NOT NULL,
  Ort VARCHAR(100) NOT NULL,
  PRIMARY KEY (KundenNr)
);

CREATE TABLE MITARBEITER
(
  MitarbeiterID INT NOT NULL,
  Vorname VARCHAR(100) NOT NULL,
  Nachname VARCHAR(100) NOT NULL,
  PRIMARY KEY (MitarbeiterID)
);

CREATE TABLE BESTELLUNG
(
  BestellungID INT NOT NULL,
  Bestelldatum DATE NOT NULL,
  Lieferdatum DATE,
  KundenNr INT NOT NULL,
  MitarbeiterID INT NOT NULL,
  PRIMARY KEY (BestellungID),
  FOREIGN KEY (KundenNr) REFERENCES KUNDE(KundenNr),
  FOREIGN KEY (MitarbeiterID) REFERENCES MITARBEITER(MitarbeiterID)
);

CREATE TABLE PRODUKTKATEGORIE
(
  ProduktkategorieID INT NOT NULL,
  Kategorie VARCHAR(100) NOT NULL,
  PRIMARY KEY (ProduktkategorieID)
);

CREATE TABLE PRODUKT
(
  ProduktID INT NOT NULL,
  Produktname INT NOT NULL,
  Verkaufspreis NUMERIC(9,2) NOT NULL,
  Einkaufspreis NUMERIC(9,2) NOT NULL,
  ProduktkategorieID INT NOT NULL,
  PRIMARY KEY (ProduktID),
  FOREIGN KEY (ProduktkategorieID) REFERENCES PRODUKTKATEGORIE(ProduktkategorieID)
);

CREATE TABLE BESTELLUNG-PRODUKT
(
  Menge INT NOT NULL,
  Einzelpreis NUMERIC(9,2) NOT NULL,
  BestellungID INT NOT NULL,
  ProduktID INT NOT NULL,
  PRIMARY KEY (BestellungID, ProduktID),
  FOREIGN KEY (BestellungID) REFERENCES BESTELLUNG(BestellungID),
  FOREIGN KEY (ProduktID) REFERENCES PRODUKT(ProduktID)
);
```
