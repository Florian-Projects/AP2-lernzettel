> [!cite] Inhalt
> 1. Prüfverfahren 
> 	1. Parität
> 	2. Redundanz 
> 	3. Prüfsummen
> 2. Softwaretest
> 	1. Voraussetzungen für das Testen
> 	2. Systematisches Testen: Prozessschritte
> 	3. Teststufen
> 	4. Arten von Tests
> 3. Testverfahren
> 	1. Verifizierende Testverfahren
> 	2. Analysierende Testverfahren
> 	3. Statische Testverfahren
> 	4. Dynamische Testverfahren
> 		1. Funktionalität dynamischer Verfahren
> 		2. Spezifikationsorientierte Verfahren (Black-Box-Tests)
> 		3. Strukturorientierte Verfahren (White-Box-Tests)
> 			1. Kontrollflussorientierte Verfahren
> 			2. Datenflussorientierte Tests

# Prüfverfahren
Bei Prüfverfahren geht es in der Regel darum, in der Lage zu sein Fehler zu erkennen und zu Korrigieren. Mögliche verfahren dafür sind:

## Parität
Paritätsprüfungen dienen dazu, auftretende Fehler zu erkennen. Ein einfaches **Beispiel** ist das Paritätsbit: Bei 7 Datenbits wird das achte Bit so gesetzt, dass die Anzahl der "1" im Byte gerade ist.

- Daten: `1001101`
- Anzahl `1`: 4
- Paritätsbit: 0
- Resultat: `01001101`

Ein Fehler kann erkannt werden, wenn die Anzahl der `1` durch eine Bitänderung ungerade wird. Eine Erweiterung ist der **Hamming-Code**, der durch mehrere Prüfbits eine Fehlerkorrektur ermöglicht, wie z.B. in RAID-5-Systemen.

## Redundanz
Redundanz bezeichnet das mehrfache Vorhalten von Informationen zur Sicherung. Beispiele:

- RAID 1: Daten werden auf zwei Festplatten gespiegelt.
- Mehrere Server, die bei Ausfall die Last übernehmen können.
- Clusterservices wie Kubernetes, Docker Swarm, Redis Cluster usw.

## Prüfsummen
Prüfsummen sind Berechnungen, die die Integrität von Daten sicherstellen sollen. Sie werden erzeugt und mit gesendeten Daten verglichen, um auf Fehler zu prüfen. Beispiele:
### Hashwerte
**MD5, SHA-1, SHA-256, BLAKE-256**
>[!important] Ein guter Hashalgorithmus zeichnet sich durch Folgendes aus:
>1. **Kollisionssicherheit**: Es sollte extrem unwahrscheinlich sein, zwei unterschiedliche Eingaben zu finden, die denselben Hashwert ergeben.
>2. **Pre-Image-Resistance**: Aus dem Hashwert sollte es nicht möglich sein, die ursprünglichen Daten zurückzugewinnen.
>3. **Schnelligkeit**: Er muss in der Lage sein, schnell einen Hashwert für beliebige Daten zu berechnen.
>4. **Determinismus**: Gleiche Eingabedaten führen stets zum identischen Hashwert.
>5. **Fehlerempfindlichkeit**: Selbst minimale Änderungen der Eingabe sollten den Hashwert drastisch ändern.

#### CRC (Cyclic Redundancy Check)
wird z.B. von Ethernet, USB und IEEE 802.x (Wi-Fi) verwendet.

#### weitere Arten von Prüfsummen:
- **Personalausweis**: Die Ziffern werden mit 7,3,1 fortlaufend gewichtet. Jede Ziffer wird mit dem Gewicht multipliziert. Die resultierenden Werte werden addiert. Die letzte Ziffer dieser Summe ist die Prüfziffer.
- **ISBN**: Jede Ziffer wird fortlaufend mit 1-9 multipliziert. Alle Ergebnisse werden addiert und durch 11 geteilt. Der Rest dieser Division ist die Prüfziffer. Wenn der Rest 0 ist, ist die Prüfziffer "X".
- **EAN-Nummern** (Barcode): Die 12 Ziffern werden abwechselnd mit 1 und 3 multipliziert, die Ergebnisse addiert. Die Differenz zum nächsten Vielfachen von 10 ist die Prüfziffer.

# Softwaretest
Testen ist der Prozess indem ein Programm auf Fehler überprüft wird.
Softwaretest ermöglichen es den erforderlichen (geforderten) Zustand mit dem tatsächlichen Zustand zu vergleichen.
>[!quote] Edsger W. Dijkstra
>Das Testen von Software kann lediglich das Vorhandensein von Fehlern nachweisen, nicht deren Abwesenheit


Wenn ein Programm soegfältig getestet und alle gefundenen Fehler korrigiert, so steigt die Wahrschienlichkeit, dass das Programm sich auch in nicht getesteten Fällen korrekt verhält.
Die Korrektheit eines programms kann durch Tests nicht bewiesen werden.

Testen setzt vorraus, dass die erwarteten Ergebnisse bekannt sind. D.h. es muss gegen eine Spzifikation oder gegen vorhandene Testergebnisse (Regressionstest) getestet werden.

**Systematisches Testen beinhaltet mehrere Prozessschritte**
1. Testplanung
	1. Testorganisation (Terminplanung, Personal etc.)
	2. Teststrategie (Testumfang/ Abdeckung)
	3. Testziele (Kriterien für Testbeginn/ Ende/ Abruch)
	4. Testarten (z.B. Statisch oder Dynamisch)
	5. Testumgebung (Simulation, Zielsystem)
	6. Testdaten
	7. Dokumentation
	8. Metriken (z.B. Fehlerraten)
2. Testvorbereitung
	1. Werkzeuge Konfigurieren
	2. Testumgebung aufbauen und einrichten (Systeme, Daten)
	3. Testobjekte in die Umgebung integrieren
3. Testfallspezifikation
	1. Spezifische Testfälle finden (Testfallfindungen, Testfalloptimierung)
	2. Exakte Testbeschreibung
	3. Abhänigkeiten zu anderen Tests feststellen
	4. Testreihenfolge, Soll-Ergebniss für Testdurchführung festlegen
4. Testfalldurchführung
	1. Testdaten, Testergebnisse, Umgebungsdaten Dokumentieren und archivieren
5. Testauswertung
	1. (pro Testfall) Vergleich soll-ist Ergebniss
	2. Entscheidung: Ist Testfall in Ordnung oder Fehlerhaft
	3. Fehlerklassifiezierung, Fehlerbeschreibung -> Weitergabe an Fehlermanagement.
	4. (eventuell Testfall wiederholung nach Softwareänderung)
6. Testabschluss
	1. Testdaten archivieren
	2. Entschiedung über nicht erreichte Soll-Ergebnissse treffen

**Tests können in mehreren Stufen erfolgen z.B.**
Dabei werden die vorher genannten Prozess jedes mal von vorne durchlaufen
1. Unit Tests
	1. Ein unit test ist ein Test das die kleinzmöglichste einheit von Code testet. z.B. eine funktion, methode, eigenschaft etc.
2. Komponenten/ Module tests
	1. Testen von unterteilen von code. z.B. ein Modul, Klasse, Unterprogramm etc.
3. Integrationstest
	1. Testen von Anhänigkeiten von Komponenten. z.B. Testen von Mehreren Klassen/ Modulen in Kombination.
4. Systemtest
	1. Testen des gesamten Systems gegen die gegebenen Anforderungen.
5. Abnahmetest
	1. Endgültiger Test vor der Auslieferung der software. Kann z.B. nach dem Pflichtenheft erfolgen

Tests können unterschiedliche Test Arten enthalten wie z.B.
1. Ende zu ende tests
	- API Test
	- Automatisierte Frontend tests
2. Last test/ Performance Tests
	1. z.B. viele Anfragen an einen Webserver schicken
	2. große Textdateien in einem Texteditor testen
	3. große csv importieren
3. Usability-Tests
4. Sicherheitstests
5. Aktzeptanzetests
6. Smoke Tests/ Build verification Test
	1. Gehört zu den Accpetance Tests
	2. Eine Reihe von tests die durchlaufen werden müssen bevor eine Version zum Testen akzeptiert werden kann.
	3. Wie bei einem klempner der erst rauch statt wasser durhc Rohre laufen lässt um Lecks zu finden
	4. passiert oft automatisch (z.B. build pipeline)
7. [[#Regressionstests]]
8. Sanity Tests
	1. Unterart von Regressionstest
	2. z.B. spezifischen Bug testen der durch software änderung gefixed wurde, bevor der Rest des Systems geprüft wird

# Softwaretest Verfahren
Zum identifizieren Testfällen und durchführen von Tests gibt es unterschiedliche Verfahren, die verwendet werden können um Testdaten zu generieren.
![[IMG_20231018_211949447~2.jpg]]

## verifizierende Testverfahren
Stellt die Korrektheit des programms sicher. z.B. kann das Programm ausgeführt werden. Kann man es compilen.

## analysierende Testverfahren
Dienen zu vermessung bzw. Darstellung von Systemkomponenten
z.B.
- Strukturelle Komplexität
- Anzahl Kommentare
- Verschachtelungs level

## Statische Testverfahren
Bei Statischen Test geht es um das Prüfen des Programms **ohne** dass das Programm ausgeführt wird.
z.B. durch:
- Reviews
- Statischer Analyse tools
	- safety, BugScout, App-Ray (Sicherheitslücken, Python, Java, IOS/ Android apps)
	- Checkstyle, pylint (Style checker, java, python)
	- Veracode (Sicherheitslücken in Binärdateien)
- Ablaufverfolgung (z.B. mit Tracetabelle) -> erkennung von unendlichen Schleifen und nicht erreichbaren code

## Dynamische Verfahren
Dynamische Softwaretests zeichnen sich dadurch aus, dass sie zur Laufzeit ausgeführt werden. Sie dienen insbesonder um Programmfehler zu erkennen, die in abhängigkeit von ==Laufzeit parametern== (z.B. Eingabeparameter), ==Laufzeitumgebungen== oder ==Nutzerinteraktion==.

### Funktionalität
Grundlage des dynamischen Verfahrens ist die kontrollierte **ausführung** der Software mit systematisch festgelegten **Testdaten**. Zu den Eingabedaten werden auch die zu erwartenden Ausgabedaten angegeben. Die vom Testlauf erzeugten daten werden mit den erwarteten Daten verglichen. Bei abweichungen liegt ein Fehler vor.
Um diese Testdaten zu generieren gibt es viele verschiedene mögliche Verfahren.

### Mögliche Verfahren
#### Spezifikationsorientierte Verfahren (Black-Box test)
Beim black-box verfahren werden die Anforderungen an das Testobjekt verwendet um Testfälle zu generieren.
Bei einem Black-Box test ist das innenleben der Anwendung nicht bekannt. Es wird lediglich geprüft ob eine gewisse Software den Anforderungen entspricht.
Man sagt auch: "Das Testobjekt wird gegen die Spezifikationen getestet".
Je nach Testobjekt und Testart können die Spezifikationen varriieren.
Bei moduletest wird z.B. gegen die Modulspezifikationen getestet, beim Schnittstellentest gegen die Vorgegebene Schnittstellenspezifikation und beim Abnahmetest gegen die funktionalen Anforderungen des Pflichtenhefts.
Um passende Testdaten zu erstellen könne verschiedene Methoden verwendet werden

##### Äquivalenzklassenbildung
Es werten alle möglichen Eingabewerte (oder auch Ausgabewerte) in Klassen eingeteilt, von denen vermutet werden kann, das eine Fehler auftreten könnte.
Die Grundannahme ist, wenn das Programm für einen wert der Klasse funktioniert, dann funktioniert es auch für alle anderen Werte der Klasse, bzw. umgekehrt: Wenn eine wert nicht funktioniert, funktioniert auch kein anderer Wert. Die werte einer solchen Klasse sind also äquivalent.
>[!important] Beispiel
>Die spezifikation eines Onlinebanking systems besagt, dass nur beträge zwischen 0,01€ - 500€ angenommen werden.
>Es ergeben sich also folgende Äquivalenz klassen:
>1. Werte von 0,01 bis und mit 500,00 € (gültig)
>2. Werte kleiner gleich null (ungültig)
>3. Werte größer als 500,00 € (ungültig)
>Da alle werte der jewiligen klassen als äquivalent betrachtet werden, könnten z.B. die Testwerte 0,001€ 123€ und 560€ Euro gewählt werden.

###### Grenzwertanalyse
Die Grenzwertanalyse ist ein ==spezialfall der der Äquivalensklassenanalyse==.
Fehler treten besonders häufig an systemgrenzen auf. Da
>[!important] Nachfolge Beispiel
>Die Äquivalenzklassen mit Grenzwertanalyse sind in diesem Fall
>1. Werte kleiner als 0,01€ (ungültig)
>2. Der Wert 0,01€ (gültig)
>3. Werte zischen 0,01€ - 500€
>4. Der Wert 500€ (gültig)
>5. Werte größer als 500 (ungültig)
>Die zu testenden werte sind also z.B. 0€ 0,01€ 130€ 500€ 560€ 

##### Pairwise-Method
Ist ein verfahren um die Anzahl von Tests mit mehreren Kombinationen von Eingabewerten zu reduzieren.
Dies wird erreicht indem nicht alle möglichen kombinationen, sondern lediglich alle kombination von paaren von eingabewerten betrachtet. Dies Reduziert die komplexität von

##### Zustandsbasierte Testmethode
Die Testfeller werden z.B. aus einem UML Zustandsdiagramm abgeleitet. Die Vollständigkeit der Testfälle ist gegeben wenn folgenden Kriterien erfüllt sind:
1. Werden alle Zustandsübergänge durchlaufen?
2. Werden alle Ereignisse, die Zustandsübergänge hervorrufen sollen, getestet?
3. Werden alle Ereignisse, die _keine_ Zustandsübergänge hervorrufen dürfen, getestet?

##### Ursache-Wirkung-Analyse
Bei der Ursache-Wirkung Analyse geht es darum von Teilspzifikationen zu identifizieren.
Urscahen sind eizelne Eingabebeingungen wirkungen einzelene Ausgabebdingungen.
Durch die daraus abgeleteiten Abghängigkeiten könne testcases generiert werden.
>[!important] Arten von Abhängigkeiten
>1. Exklusive Abhängigkeit: Die Anwesenheit einer Ursache schließt andere Ursachen aus.
>2. Inklusive Beziehung: Mindestens eine von mehreren Ursachen liegt vor (z. B. ist eine Ampel immer grün, gelb oder rot – oder rot und gelb zusammen. Wenn sie funktioniert und eingeschaltet ist).
>3. One-and-only-one-Beziehung: Es liegt genau eine von mehreren Ursachen vor (z. B. männlich oder weiblich).
>4. Requires-Abhängigkeit: Die Anwesenheit einer Ursache ist Voraussetzung für das Vorhandensein einer anderen (z. B. Alter > 21 und Alter > 18).
>5. Maskierungsabhängigkeit: Eine Ursache verhindert, dass eine andere Ursache eintreten kann.

#### Strukturorientierte Verfahren (Whitebox Test)
https://youtu.be/nQQwBsK7YII
Anders als beim Blackbox test ist bei Whitebox tests das innenleben der Anwenung bekannt.
Bei whitebox tests geht es also nicht darum ein und ausgabewerte zu überprüfen, sondern denn Ablauf des Programms zu verfolgen.

##### Kontrollflussorientierte verfahren
1. **Anweisungsüberdeckungstest**: Jede anweisung im Kontrollfluss muss mindestens einmal ausgeführt werden
2. **Kantenüberdeckungstest**: Jeder zweig eines Kontrollflusses muss einmal durchlaufen werden (schliesst Anweisungspberdeckung mit ein)
3. **Bedingungsüberdeckungstest**: Jeder möglichkeit einer Bedingung (Verzweigung) muss mindestens einmal ausgeführt werden
4. **Pfadüberdeckungstest**: Jeder mögliche Pfad muss mindestens einmal durchlaufen sein.

##### Datenflussorientierte Tests
Sehr komplexer graph theorie shit keine ahnung.
Es geht darum, dass die definition und veränderung von variablen innerhalb eines programmablaufs getestet werden.

Whitebox test können Probleme die durch ==Abweichungen== zwischen den tatsäschlichen anforderungen oder Spezifikation entstehen ==NICHT ERKENNEN==. 
Whitebox tests können ==Kontrollflussprobleme== wie, geschlossene oder unendliche Schleifen oder nicht erreichbaren code ==ERKENNEN==.
>[!important] Beispiel
>Eine programm bekommt zweil Zahlen a und b und teilt die größere durch die kleinere von beiden. Selbst wenn alle pfade getestet sind könnte der fall `3 / 0` dennoch einen Fehler auslösen.

## Diversifizierende Testverfahren
### Back-to-Back Test
Das ziel von Back-to-Back tests ist es die Effekte von Softwareveränderung zu erkennen. Dies involviert das vergleichen des Testverhaltens mit einer anderen version der software.

### Mutationen-Test
https://www.johner-institut.de/blog/iec-62304-medizinische-software/regressionstest/
Bei mutationstest, werden absichtlich Fehler in den Programmcode platziert. Das ziel ist, zu erkennen ob die gegebene Testabdeckung in der Lage ist die Mutanten zu erkenen und zu "töten".
Wenn die Testabdeckung nicht ausreichend ist und der Mutation Score entsprechend niedrig können die testfälle so erweitert werden, dass diese Mutationen auch erkannt werden.

### Regressionstest
https://www.johner-institut.de/blog/iec-62304-medizinische-software/regressionstest/
Unter einem regressionstest versteht man die wiederholung von Testfällen nach Programmänderungen. Sie verfolgt mehrer Ziele
1. Alter Code funktioniert noch
2. Code funktioniert zuverlässig
	1. z.B. mehrfach ausführung um Race-Conditions zu finden
	2. bei änderung von Hardware bzw. der Laufzeitungebung
	3. oder bei abhängikeiten von sich ändernden daten.

>[!important] Beispiel
>Bei jedem release werden die gleichen existierenden Testcases jedes mal neu ausgeführt



## Review
Systematische Überprüfung von Softwareartefakten, z.B. Quellcode oder Design-Dokumenten. Oft nach 4 Augen Prinzip.


## Testdaten
Speziell vorbereitete Daten, die verwendet werden, um ein Softwareprogramm zu testen, meist um spezifische Fälle und Reaktionen des Systems zu überprüfen.

# Debugging
Prozess der Identifizierung und Behebung von Defekten oder Problemen innerhalb eines Programmcodes, der eine gezielte Diagnose und Korrektur von Fehlern erfordert.

# Ablaufverfolgung
Techniken zur Überwachung und Protokollierung des Verhaltens von Programmen während ihrer Ausführung, häufig verwendet, um Probleme oder unerwartete Verhaltensweisen zu diagnostizieren.

# Netzwerkanalyse
Methoden zur Untersuchung von Netzwerken, einschließlich der Überwachung des Datenverkehrs, um Leistung und Sicherheit zu bewerten.

# Bandbreite
Maß für die Übertragungskapazität, wichtig für das Verständnis der Datenübertragungsraten und potenzieller Engpässe in Netzwerkumgebungen.

# Reaktionszeiten
Messungen, die zeigen, wie schnell ein System oder eine Komponente auf eine bestimmte Anfrage reagiert, ein kritischer Faktor für die Benutzererfahrung.