
## Inhalt

> [!cite] Inhalt
> 
> - ﻿﻿Relationale und nicht-relationale Datenbanken, NoSQL Datenbanken
> - ﻿﻿Datentypen: Boolesche Werte, Ganzzahl, Gleitkom-mawerte, Währung, Datumswerte, Texte fester und variabler Länge, BLO, Geokoordinaten
> - ﻿﻿Normalisieren, 1. bis 3. Normalform
> - ﻿﻿ER-Diagramm, Attribute, Beziehungen, Kardinali-täten, referenzielle Integrität, Aktualisierungsweiter-gabe, Löschweitergabe, Primärschlüssel, Fremd-schlüssel
> - ﻿﻿Datenbankabfrage, Datenpflege
> - ﻿﻿Tabellenstruktur (CREATE TABLE, ALTER TABLE), Index (CREATE INDEX), Manipulation (INSERT, UP-DATE, DELETE), Projektion (SELECT FROM) Selektion (SELECT FROM ... WHERE) und (SELECT ... (SELECT ...)), Sortieren (ORDER BY), Gruppieren (GROUP BY, HAVING)
> - ﻿﻿Abfrage über mehrere Tabellen (JOIN)
> - ﻿﻿Ausdrücke und Bedingungen
> - ﻿﻿Aggregat-Funktionen, z. B. SUM
> - ﻿﻿OpenData, API-Schnittstellen
### **Relationale und nicht-relationale Datenbanken, NoSQL Datenbanken:**
    
- **Relationale Datenbanken:** Diese speichern Daten in tabellenähnlichen Strukturen, wobei Beziehungen zwischen Tabellen durch Schlüssel hergestellt werden. Sie folgen einem festen Schema und verwenden SQL (Structured Query Language) für Abfragen und Manipulationen.
- **Nicht-relationale Datenbanken (NoSQL - non-SQL, manchmal auch [not only SQL](https://en.wikipedia.org/wiki/NoSQL#cite_note-3)):** Im Gegensatz dazu ==speichern sie Daten auf flexible Weise, oft ohne ein festes Schema==. Sie sind besser für unstrukturierte Daten oder schnelle Änderungen geeignet und verwenden unterschiedliche Modelle, z.B. Dokumenten-, Spaltenfamilien- oder Graphendatenbanken.
1. **Dokumentenbasierte Datenbanken:**
	
	- Speichern Daten in Dokumenten, typischerweise im JSON- oder XML-Format.
	- Jedes Dokument enthält alle relevanten Informationen und kann in der Struktur variieren.
	- Beispiele: MongoDB, Couchbase.
2. **Spaltenorientierte Datenbanken:**
	
	- Speichern Daten in Spaltenfamilien oder Spaltengruppen statt in Zeilen.
	- Optimal für Lesevorgänge, Analytik und Big Data-Szenarien.
	- Beispiele: Apache Cassandra, HBase.
3. **Graphdatenbanken:**
	
	- Modellieren Daten als Knoten und Kanten, um Beziehungen zwischen Datenpunkten effizient darzustellen.
	- Geeignet für komplexe Abfragen, soziale Netzwerke und Wissensgraphen.
	- Beispiele: Neo4j, Amazon Neptune.
4. **Schlüssel-Wert-Datenbanken (Key Value Datenbanken):**
	
	- Speichern Daten als Schlüssel-Wert-Paare, wobei der Schlüssel einen eindeutigen Identifier für den Wert darstellt.
	- Effizient für schnelle Lese- und Schreibvorgänge.
	- Beispiele: Redis, Riak.
5. **Objekt-orientierte Datenbanken:**
	
	- Speichern Daten als Objekte, wobei die Struktur und die Beziehungen zwischen den Objekten erhalten bleiben.
	- Geeignet für Anwendungen, die auf objektorientierten Paradigmen basieren.
	- Beispiele: db4o.
6. **Multi-Modell-Datenbanken:**
	
	- Kombinieren verschiedene NoSQL-Modelle in einer einzigen Datenbank, um vielseitige Anforderungen zu erfüllen.
	- Ermöglicht die Verwendung mehrerer Modelle in einem einzigen System.
	- Beispiele: ArangoDB, OrientDB.
7. **Zeitreihendatenbanken (Timeseries Databases):**
	
	- Speichern und verwalten Zeitreihendaten, die sich im Laufe der Zeit ändern, wie Sensordaten und Protokolle.
	- Optimiert für das Speichern und Abfragen von zeitbasierten Daten.
	- Beispiele: InfluxDB, OpenTSDB.

### **Datentypen:**

- **Boolesche Werte:** Wahr/Falsch (True/False) Werte.
- **Ganzzahl:** Ganze Zahlen ohne Dezimalstellen.
- **Gleitkommawerte:** Zahlen mit Dezimalstellen.
- **Währung:** Werte zur Darstellung von Geldbeträgen.
- **Datumswerte:** Datums- und Zeitinformationen.
- **Texte fester und variabler Länge:** Zeichenketten, wobei feste Länge eine festgelegte Anzahl von Zeichen hat und variable Länge sich anpasst.
	- `CHAR(20)` muss immer 20 Chars lang sein
	- `VARCHAR(20)` kann max 20 Chars lang sein
	- `TEXT` egal wie lang
- **BLOB:** Binary Large Object, um binäre Daten wie Bilder oder Dokumente zu speichern.
- **Geokoordinaten:** Breiten- und Längengrade zur Darstellung von Ortsinformationen.

### **Normalisieren, 1. bis 3. Normalform:**

- **Normalisieren:** Ein Prozess in der Datenbankgestaltung, um Daten in tabellarischen Beziehungen effizienter zu organisieren und Redundanz zu reduzieren.
- Beispiel: [[#Normalisierung]]
- **1. Normalform:** Jede Spalte in einer Tabelle enthält atomare (unteilbare) Werte.
- **2. Normalform:** Eine Tabelle in 1. Normalform, und alle Nicht-Schlüsselattribute sind funktional abhängig vom gesamten Primärschlüssel.
	- Nur anwendbar wenn man einen zusammengesetzten Primärschlüssel benutzt
	- Erklär in Tristan Worten: Man kann keine nicht-Schlüsselspalte eindeutig von einem einzigen der Primarschlüsseln ableiten
- **3. Normalform:** Eine Tabelle in 2. Normalform, und es besteht keine transitive Abhängigkeit zwischen Nicht-Schlüsselattributen.

### **ER-Diagramm, Attribute, Beziehungen, Kardinalitäten, referenzielle Integrität, Aktualisierungsweitergabe, Löschweitergabe, Primärschlüssel, Fremdschlüssel:**
    
- **ER-Diagramm:** Ein grafisches Modell zur Darstellung von Entitäten (Objekten), Attributen (Eigenschaften), Beziehungen zwischen Entitäten und anderen Konzepten in einer Datenbank.
- **Attribute:** Eigenschaften oder Merkmale von Entitäten in einer Datenbank.
- **Beziehungen:** Darstellen, wie Entitäten miteinander in Verbindung stehen.
- **Kardinalitäten:** Definieren, wie viele Entitäten in einer Beziehung beteiligt sein können (z.B., 1:1, 1:N, N:M).
- **Referenzielle Integrität:** Sicherstellung, dass Beziehungen zwischen Tabellen konsistent sind.
	- Sagt das ein FK auch wirklich auf eine existierende Zeile zeigen muss
	- Wird durch FK-Constraints umgesetzt
- **Aktualisierungsweitergabe und Löschweitergabe:** Festlegen, wie Änderungen an Beziehungselementen auf verbundene Elemente übertragen werden.
	- Löschweitergabe: löscht sie die mit dem zu löschenden Datensatz verknüpften Datensätze ebenfalls
		- `on_delete=models.CASCADE`
	- Aktualisierungsweitergabe: wenn man den PK einer Zeile ändert werden alle FKs die auf ihn zeigen geändert
- **Primärschlüssel und Fremdschlüssel:** Primärschlüssel identifiziert eindeutig Datensätze, während der Fremdschlüssel Beziehungen zwischen Tabellen herstellt.

### **Datenbankabfrage, Datenpflege:**
    
- **Datenbankabfrage:** Ein Prozess, bei dem Daten aus einer Datenbank extrahiert werden, normalerweise unter Verwendung von SQL.
- **Datenpflege:** Das Hinzufügen, Aktualisieren und Löschen von Daten in einer Datenbank, um deren Genauigkeit und Vollständigkeit sicherzustellen.

### **Tabellenstruktur, Index, Manipulation, Projektion, Selektion, Sortieren, Gruppieren:**

[[#IHK Belegsatz SQL]]

1. **Tabellenstruktur**
    - **CREATE TABLE**: Dient zum Erstellen einer neuen Tabelle.
        ```sql
        CREATE TABLE Studenten (
            StudentenID INT PRIMARY KEY,
            Name VARCHAR(100),
            Alter INT
        );
        ```
    - **ALTER TABLE**: Modifiziert die Struktur einer bestehenden Tabelle, z.B. um eine Spalte hinzuzufügen.
        ```sql
        ALTER TABLE Studenten ADD Email VARCHAR(100);
        ```

2. **Index**
    - **CREATE INDEX**: Erstellt einen Index auf einer oder mehreren Spalten, um die Abfrageleistung zu verbessern.
        ```sql
        CREATE INDEX idx_Name ON Studenten (Name);
        ```

3. **Manipulation**
    - **INSERT**: Fügt einen neuen Datensatz in eine Tabelle ein.
        ```sql
        INSERT INTO Studenten (StudentenID, Name, Alter) VALUES (1, 'Anna', 20);
        ```
    - **UPDATE**: Ändert existierende Datensätze in einer Tabelle.
        ```sql
        UPDATE Studenten SET Alter = 21 WHERE StudentenID = 1;
        ```
    - **DELETE**: Löscht Datensätze aus einer Tabelle.
        ```sql
        DELETE FROM Studenten WHERE StudentenID = 1;
        ```

4. **Projektion**
    - **SELECT FROM**: Wählt bestimmte Spalten aus einer Tabelle aus.
        ```sql
        SELECT Name, Alter FROM Studenten;
        ```

5. **Selektion**
    - **SELECT FROM ... WHERE**: Filtert Datensätze basierend auf einer Bedingung.
        ```sql
        SELECT Name, Alter FROM Studenten WHERE Alter > 20;
        ```
    - **Subquery (SELECT ... (SELECT ...))**: Eine Abfrage innerhalb einer anderen Abfrage.
        ```sql
        SELECT Name FROM Studenten WHERE Alter > (SELECT AVG(Alter) FROM Studenten);
        ```

6. **Sortieren**
    - **ORDER BY**: Sortiert die Ergebnisse einer Abfrage.
        ```sql
        SELECT Name, Alter FROM Studenten ORDER BY Alter DESC;
        ```

7. **Gruppieren**
    - **GROUP BY**: Gruppiert Ergebnisse nach einer oder mehreren Spalten.
    - **HAVING**: Filtert Gruppierungsergebnisse basierend auf einer Bedingung.
        ```sql
        SELECT Alter, COUNT(*) FROM Studenten GROUP BY Alter HAVING COUNT(*) > 1;
        ```

8. **Abfrage über mehrere Tabellen**
    - **JOIN**: Verknüpft Zeilen aus zwei oder mehr Tabellen basierend auf einer verwandten Spalte.
        ```sql
        SELECT s.Name, k.Kursname FROM Studenten s JOIN Kurse k ON s.StudentenID = k.StudentenID;
        ```

9. **Ausdrücke und Bedingungen**
    - Mathematische und logische Operationen, Vergleichsoperatoren usw.
        ```sql
        SELECT Name, Alter*12 AS Monate FROM Studenten WHERE Name LIKE 'A%';
        ```

10. **Aggregat-Funktionen**
    - **SUM**: Summiert die Werte einer Spalte.
        ```sql
        SELECT SUM(Alter) FROM Studenten;
        ```

### **OpenData, API-Schnittstellen:**
    
- **OpenData:** Daten, die frei verfügbar und ohne Einschränkungen genutzt werden können. - [wiki](https://en.wikipedia.org/wiki/Open_data)
- **API-Schnittstellen:** Erlauben den Zugriff auf und die Interaktion mit Diensten oder Daten über vordefinierte Schnittstellen (Application Programming Interfaces).


## Normalisierung

https://it-berufe-podcast.de/normalisierung-einer-datenbank-am-konkreten-beispiel-anwendungsentwickler-podcast-144/

### 0 NF - nicht normalisiert

![[Pasted image 20231029154612.png]]

### 1 NF

> Es gibt 1) nur atomare Attribute und 2) keine Wiederholungsgruppen
> Alle Datensätze sind eindeutig über einen Primärschlüssel identifizierbar

Primärschlüssel Teile sind Rot

![[Pasted image 20231029154624.png]]

### 2 NF

> Alle Attribute hängen vom gesamten Schlüssel ab (und nicht nur von seinen Teilen).

Eklärung nur für Entity Kunde: Es wurde eine extra Tabelle erstellt weil man Nachname, Vorname, Straße, ... eindeutig anhand von der Kundennummer erkennen konnte. In der Bestellungs Tabelle steht jetzt nur noch der FK: Kundennummer

![[Pasted image 20231029154656.png]]

### 3 NF

> Kein Nicht-Schlüssel-Attribut hängt von einem anderen Nicht-Schlüssel-Attribut ab

`Artikel.Rabatt` hing von `Artikel.Artikelgruppe`ab -> immer wenn es Artikelgruppe `Elektronik` war gab es auch 10% Rabatt. Das ist jetzt in einer eigenen Tabelle

![[Pasted image 20231029154931.png]]

## IHK Belegsatz SQL

![[SQL_Belegsatz_IHK.pdf]]