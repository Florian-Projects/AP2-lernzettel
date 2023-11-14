# Begriffsklärung:
## Qualität
> [!cite] Nach ISO 9000
>" Grad, in dem ein Satz inhärente Merkmale von Anforderungen erfüllt."
>Dies bedeutet das Qualität nicht nur an der Abwesenheit von Fehlern gemessen wird sondern auch wie gut ein Produkt die spezifizierten Anforderungen erfüllt.

Qualität beschreibt ob ein Produkt/ Dienstleitung den festgelegten  und implizierten Anforderungen entspricht. sie kann sowohl Subjektiv als auch Objektiv sein.

> [!example]
> 1. Ein Qualitatives Auto ist nicht nur frei von Fehlern sondern bietet auch hohen Komfort, Sicherheit und Effizienz.
> 2. Eine software ist nicht nur frei von Fehlern/ Bugs sondern auch benutzerfreundlich und effizient. Die anzahl gemeldeter Bugs, Reaktionszeiten und grad an Barrierefreiheit könnten als Qualitätsindikatoren dienen.

## Qualitätsprüfung
Ist der Prozess bei dem der Grad der Qualität geprüft wird. Dabei wird der soll-Zustand mit dem Ist-Zustand verglichen. Dies erfolgt in der Regel anhand von Fakten wie ==Messdaten (Anzahl reporteter Bugs, Reaktionszeit, Anzahl fehlgeschlagen tests, Testgrad etc.)== und/ oder anhand von ==subjektiven Empfindungen (Kundenzufriedenheit, Benutzerfeedback, Interne Diskussionen und Umfragen)==

## Qualitätssicherung
Bezeichnet alle geplanten Maßnahmen die zur Aufrechterhaltung der gewünschten Qualität dienen. (Prüfaspekt des Qualitätsmanagement).

Typische methoden Der qualiltätsicherungen sind:
1. [[01 Methoden zur  Qualitätssicherung anwenden#Softwaretest | Softwaretests]]
2. Anforderungsanalyse
	1. Funktionale Anforderungen: Was soll das system tun
	2. Nicht-Funktionale Anforderungen: Qualitat/ Performance des Systems (Sicherheit, Zuverlässigkeit, Benutzerfreundlichkeit, Barrierefreiheit, etc.)
	3. Systemanforderungen: Technische Anforderungen an Hardware, Software und Netzwerk
3. [[01 Methoden zur  Qualitätssicherung anwenden#Review | Code Reviews]]
4. Dokumentation
	1. Nutzer Handbücher/ Anleitungen
	2. Dokumentation der Software Fähigkeiten
	3. Dokumentation des Quellcodes (Typing, Kommentare, Docstring, API docs, README etc.)
	4. Dokumentation des Systems (z.B. durch Design Dokumente wie UML diagramme, Mockups)
5. Kontinuierliche Integration (Continuous Integration, CI)
	1. Bei jeder integration (z.B. jeder Mergerequest) werden automatisch Qualitätssicherende maßnahmen ausgelöst. Welche erfolgreich durchlaufen bevor die änderungen Übernommen werden können. Das Ziel ist den Integrationsprozess zu beschleunigen, und die Software durchgehend in einem deploybaren Zustand zu halten.
	2. Automatisierte Build, Tests, Linting etc.
	3. Automatische Bereitstellung durch Continuous Deployment (CD)
	4. Integration mit anderen Tools wie, Bug-Tracking/ Planungs werkzeugen, Versionkontrollsystemen etc.
6. Feedback-Schleifen
	1. Entwickler erhalten schnelles Feedback über en Zustand ihres Code, was dabei hilft Probleme fürhzeitig zu identifizieren und lösen.
	2. z.B. durch regelmäßiges feedback mit den Stakeholdern.
	3. Grundlage der agilen Arbeitsmethode
7. Schulung und Weiterbildungen
	1. Weiterbildung von Entwicklern kann die Qualität von Software erhöhen

> [!important] Weitere Begriffe
> Konformität: Erfüllung einer Anforderung
> Ständige verbesserung: wiederkehrende Tätigkeiten zum Erhöhen der Fähigkeiten, Anforderungen zu erfüllen.

# Qualitätsmanagement nach ISO 9000 Normen
Die ISO 9000, 9001, 9004 enthalten Normen und Standards um Unternehmen dahei zu unterstützen effiziente Qualitätsmanagement systeme zu implementieren und kontinuirlich zu verbessern.

## ISO 9000
Regelt Grundlagen und Begriffe zu Qualitätmanagementsystemen. Sie definiert 7 (seit 2015 davor 8) Grundsätze:
1. Kundenorientiertheit
	1. Das Ziel jedes QMS soll es sein die Anforderungen und Erwartungen des Kundesn zu übertreffen
2. Verantwortlichkeit der Führung
	1. Führungskräfte müssen die Aufrechterhaltung des QMS nachaltig aufrechterhalten. Sie vermitteln Strategien und Prozesse und ünterstüzen mitarbeiter im Sinne der erreichung von Qualitätszielen
3. Einbeziehung der beteiligten Personen
	1. Unternehmen sollten ihre Mitarbeiter wertsschätzen, fördern und in den Entscheidungsprozess einbinden.
4. Prozessorientierter Ansatz
	1. Tätigkeiten, Ressourcen und Aufgaben sollte als zusammenhängende Prozesse verstanden werden. Dadurch können Probleme erkannt, nicht wertschöpfende Tätigkeiten vermieden und Das Managementsystem optimiert werden
5. Kontinuirliche Verbesserung
	1. Unternehmen sollten einen fortlaufendne Fokus auf verbesserungen haben um ihre Leistungsfähigkeit und Reaktionsfähigkeit in einem sich ständig veränderden Umgebung sicherzustellen
	2. z.B. durch Ressourcen für verbesserungsprojekte, Prämien für verbesserungsvorschläge, erschaffen von Innovationsprozessen
6. Sachbezogene Entscheidungsfindungsansatz
	1. Entschiedungen sollte auf Basis Daten bzw. auswertung von Informationen basieren. 
7. Lieferbeziehungen zum gegenseitigen Nutzen
	1. Hat den Nutzgewinn sämtlicher interresierter parteien (z.B. Kunden, Lieferandne, Unternehmen) zum Ziel.  Durch die Pflege solcher beziehungen können alle Parteien gemeinsam wachsen und sich entwickeln

## ISO 9001
Legt mindestanforderungen an QM-Systeme fest, die erfüllt werden müssen um Kundenerwartungen und allfällige behördliche Anforderungen zu erfüllen.
Zugleich soll das QM-System einem stetigen Verbesserungsprozess unterliegen.
Dies Geschieht in der regel mithilfe von [[02 Methoden im QM-Prozess#PDCA-Zyklus | PDCA-Zyklus]] oder [[02 Methoden im QM-Prozess#KVP | KVP]]

Einige der wichtigsten Aspekte sind:
1. **Kontext der Organisation**:
	1. Die Organisation muss ihren internen und externen Kontext verstehen, um die Erwartungen interessierter Parteien zu berücksichtigen und die Anwendungsbereiche des QMS festzulegen.
	2. Durchführung einer SWOT-Analyse (Stärken, Schwächen, Chancen, Risiken) zur Identifizierung interner und externer Themen, die für das QM-System relevant sind.
2. **Führung**: 
	1. Die oberste Leitung der Organisation muss das Qualitätsmanagement unterstützen, die Qualitätsziele festlegen und sicherstellen, dass das QMS in die Unternehmensstrategie integriert ist.
	2. Regelmäßige Management-Meetings, in denen die Qualitätspolitik und -ziele überprüft und, falls notwendig, angepasst werden.
3. **Kundenorientierung**:
	1. Die Organisation muss die Anforderungen und Erwartungen der Kunden verstehen und sicherstellen, dass ihre Produkte oder Dienstleistungen diese Anforderungen erfüllen.
	2. Flexible Vertrags- und Zahlungsmodelle.
4. **Planung**:
	1. Es müssen Ziele festgelegt und Aktionspläne entwickelt werden, um diese Ziele zu erreichen. Risiken und Chancen müssen identifiziert und bewertet werden.
	2. Implementierung eines Risikomanagementsystems, um Risiken und Chancen zu identifizieren, zu bewerten und Maßnahmen zur Risikominderung festzulegen.
5. **Unterstützung**: 
	1. Die Organisation muss sicherstellen, dass sie über die erforderlichen Ressourcen, Infrastruktur, Kompetenzen und Unterstützung verfügt, um das QMS umzusetzen und aufrechtzuerhalten.
	2. Durchführung regelmäßiger Schulungen und Workshops, um sicherzustellen, dass alle Mitarbeiter über die notwendigen Kompetenzen verfügen und sich der Qualitätsziele bewusst sind.
6. **Betriebliche Durchführung**: 
	1. Dieser Abschnitt umfasst die Planung und Steuerung von Prozessen, um Produkte oder Dienstleistungen gemäß den Anforderungen herzustellen oder zu erbringen.
	2. Einführung eines standardisierten Prozesses zur Überprüfung und Genehmigung von Lieferanten, um die Qualität extern bereitgestellter Produkte und Dienstleistungen sicherzustellen.
7. **Leistungsbewertung**: 
	1. Die Organisation muss die Leistung des QMS überwachen, messen, analysieren und bewerten, um Verbesserungsmöglichkeiten zu identifizieren.
	2. einrichtung eines internen Audit-Programms, bei dem unabhängige Auditoren regelmäßig die Einhaltung der ISO 9001 und die Wirksamkeit des QM-Systems überprüfen.
8. **Verbesserung**: 
	1. Die Organisation muss kontinuierlich Verbesserungen umsetzen, um die Effektivität des QMS zu steigern und die Kundenzufriedenheit zu erhöhen.
	2. Implementierung eines Feedback-Systems für Kunden, um Rückmeldungen zu sammeln, und Einrichtung eines Teams, das sich mit der Analyse dieses Feedbacks und der Ableitung von Verbesserungsmaßnahmen befasst.

## ISO 9004
Enthalt eine Anleitung zum berwerten der Effizienz und Wirksamkeit von QM-Systemen.
1. **Einleitung:** Erläuterung des Zwecks der Norm und ihrer Beziehung zur ISO 9001.
2. **Geltungsbereich:** Abgrenzung des Anwendungsbereichs der Norm.
3. **Begriffe und Definitionen:** Erläuterung spezifischer Begriffe, die in der Norm verwendet werden.
4. **Kontext der Organisation:** Betrachtung der internen und externen Faktoren, die die Organisation beeinflussen, sowie das Verständnis der Bedürfnisse und Erwartungen der interessierten Parteien.
5. **Führung:** Anleitung zur Schaffung einer Vision, Mission und Werte für die Organisation. Fokus auf die Rolle der Führung bei der Schaffung einer kundenorientierten Kultur.
6. **Strategie und Politik:** Anleitung zur Entwicklung von Strategien, die auf der Vision und Mission der Organisation basieren, und zur Umsetzung von Politiken zur Erreichung dieser Strategien.
7. **Ressourcenmanagement:** Ratschläge zur effizienten Nutzung und Verwaltung von Ressourcen, einschließlich Personal, Infrastruktur und Arbeitsumgebung.
8. **Prozessmanagement:** Empfehlungen zur Identifizierung, Verwaltung und Verbesserung von Prozessen, um konsistente und effektive Ergebnisse zu erzielen.
9. **Leistungsbewertung und -verbesserung:** Anleitung zur Bewertung der Leistung des Qualitätsmanagementsystems und zur Identifizierung von Verbesserungsmöglichkeiten.
10. **Verbesserung, Innovation und Lernen:** Ratschläge zur Förderung einer Kultur der kontinuierlichen Verbesserung, Innovation und organisatorischen Lernens.

# Software qualität nach ISO 9126/ 25000
s.319 + 304
Die ISO 9126 definiert ein Qualitätsmodell für Softwareprodukte. Sie soll ein standard für die Bewertung der Softwarequalität bieten. Dieser Standard besteht aus 4 Hauptkriterien, die dann weiter in Unterkritieren zerteilt werden.

Die ISO 25000 ist der Nachfolger der ISO 9126 (seit 2005) und stellt eine umfassendes Framework für alle Aspekte der Softwarequalität von Anforderungen über die Bewertung bis hin zur Qualität der Anwendung.

## Qualitätskriterien nach ISO 9126
![[Pasted image 20231021214156.png]]
![[Pasted image 20231021221637.png]]
###  Änderbarkeit/Wartbarkeit
Welchen Aufwand erfordert die Durchführung vorgegebener Änderungen an der Software?
Änderungen können Korrekturen, Verbesserungen oder Anpassungen an Änderungen der Umgebung, der Anforderungen oder der funktionalen Spezifikationen einschließen.
- **Analysierbarkeit**: Aufwand, um Mängel oder Ursachen von Versagen zu diagnostizieren oder um änderungsbedürftige Teile zu bestimmen.
- **Konformität**: Grad, in dem die Software Normen oder Vereinbarungen zur Änderbarkeit erfüllt.
- **Modifizierbarkeit**: Aufwand zur Ausführung von Verbesserungen, zur Fehlerbeseitigung oder Anpassung an Umgebungsänderungen.
- **Stabilität**: Wahrscheinlichkeit des Auftretens unerwarteter Wirkungen von Änderungen.
- **Testbarkei**: Aufwand, der zur Prüfung der geänderten Software notwendig ist.

### Benutzbarkeit
Welchen Aufwand fordert der Einsatz der Software von den Benutzern und wie wird er von diesen beurteilt? [Software-Ergonomie](https://de.wikipedia.org/wiki/Software-Ergonomie "Software-Ergonomie").
- **Attraktivität**: Anziehungskraft der Anwendung gegenüber dem Benutzer.
- **Bedienbarkeit**: Aufwand für den Benutzer, die Anwendung zu bedienen.
- **Erlernbarkeit**: Aufwand für den Benutzer, die Anwendung zu erlernen.
- **Konformität**: Grad, in dem die Software Normen oder Vereinbarungen zur Benutzbarkeit erfüllt.
- **Verständlichkeit**: Aufwand für den Benutzer, das Konzept und die Anwendung zu verstehen.

### Effizienz
Wie liegt das Verhältnis zwischen Leistungsniveau der Software und eingesetzten Betriebsmitteln?
- **Konformität**: Grad, in dem die Software Normen oder Vereinbarungen zur Effizienz erfüllt.
- **Zeitverhalten**: Antwort- und Verarbeitungszeiten sowie Durchsatz bei der Funktionsausführung.
- **Verbrauchsverhalten**: Anzahl und Dauer der benötigten Betriebsmittel bei der Erfüllung der Funktionen. Ressourcenverbrauch, wie CPU-Zeit, Festplattenzugriffe usw.

### Funktionalität
Inwieweit besitzt die Software die geforderten Funktionen? 
Vorhandensein von Funktionen mit festgelegten Eigenschaften. Diese Funktionen erfüllen die definierten Anforderungen.
- **Angemessenheit**: Eignung von Funktionen für spezifizierte Aufgaben, zum Beispiel aufgabenorientierte Zusammensetzung von Funktionen aus Teilfunktionen.
- **Sicherheit**: Fähigkeit, unberechtigten Zugriff, sowohl versehentlich als auch vorsätzlich, auf Programme und Daten zu verhindern.
- **Interoperabilität**: Fähigkeit, mit vorgegebenen Systemen zusammenzuwirken.
- **Konformität**: Fähigkeit des Softwareprodukts, Standards, Konventionen oder gesetzliche Bestimmungen und ähnliche Vorschriften bezogen auf die Funktionalität einzuhalten.
- **Ordnungsmäßigkeit**: Merkmale von Software, die bewirken, dass die Software anwendungsspezifische Normen oder Vereinbarungen oder gesetzliche Bestimmungen und ähnliche Vorschriften erfüllt.
- **Richtigkeit**: Liefern der richtigen oder vereinbarten Ergebnisse oder Wirkungen, zum Beispiel die benötigte Genauigkeit von berechneten Werten.

### Übertragbarkeit
Wie leicht lässt sich die Software in eine andere Umgebung übertragen?
Eignung der Software, von der Umgebung in eine andere übertragen werden zu können. Umgebung kann organisatorische Umgebung, Hardware- oder Software-Umgebung sein.
- **Anpassbarkeit**: Fähigkeit der Software, diese an verschiedene Umgebungen anzupassen.
- **Austauschbarkeit**: Möglichkeit, diese Software anstelle einer spezifizierten anderen in der Umgebung jener Software zu verwenden, sowie der dafür notwendige Aufwand.
- **Installierbarkeit**: Aufwand, der zum Installieren der Software in einer festgelegten Umgebung notwendig ist.
- **Koexistenz**: Fähigkeit der Software neben einer anderen mit ähnlichen oder gleichen Funktionen zu arbeiten.
- **Konformität**: Grad, in dem die Software Normen oder Vereinbarungen zur Übertragbarkeit erfüllt.

### Zuverlässigkeit
Kann die Software ein bestimmtes Leistungsniveau unter bestimmten Bedingungen über einen bestimmten Zeitraum aufrechterhalten?
- **Fehlertoleranz**: Fähigkeit, ein spezifiziertes Leistungsniveau bei Software-Fehlern oder Nicht-Einhaltung ihrer spezifizierten Schnittstelle zu bewahren.
- **Konformität**: Grad, in dem die Software Normen oder Vereinbarungen zur Zuverlässigkeit erfüllt.
- **Reife**: Geringe Versagenshäufigkeit durch Fehlerzustände.
- **Wiederherstellbarkeit**: Fähigkeit, bei einem Versagen das Leistungsniveau wiederherzustellen und die direkt betroffenen Daten wiederzugewinnen. Zu berücksichtigen sind die dafür benötigte Zeit und der benötigte Aufwand.

## Konformitätsbeispiele:
1. **Funktionalitätskonformität:**
    - **Beispiel:** Eine Buchhaltungssoftware könnte die **International Financial Reporting Standards (IFRS)** einhalten, was bedeutet, dass sie Funktionen bietet, die sicherstellen, dass Finanzberichte diesen Standards entsprechen.

1. **Zuverlässigkeitskonformität:**
    - **Beispiel:** Medizinische Software, die in einem Herzschrittmacher verwendet wird, könnte die **IEC 60601** Norm für medizinische elektrische Geräte einhalten, um sicherzustellen, dass sie die für Patientensicherheit erforderliche Zuverlässigkeit aufweist.
    
1. **Benutzbarkeitskonformität:**
    - **Beispiel:** Eine öffentliche Website könnte die **WCAG 2.0 (Web Content Accessibility Guidelines)** einhalten, was bedeutet, dass die Website-Designs und -Funktionen den Anforderungen für Barrierefreiheit entsprechen.
    
1. **Effizienzkonformität:**
    - **Beispiel:** Ein Datenbankmanagementsystem könnte den **SQL:2016** Standard für die Abfrageleistung einhalten, was sicherstellt, dass es effizient mit standardisierten SQL-Abfragen umgehen kann.

1. **Wartbarkeitskonformität:**
    - **Beispiel:** Ein Softwareprodukt könnte den **MISRA C** Richtlinien folgen, einer Norm für die Programmierung in der C-Sprache, die insbesondere in sicherheitskritischen Anwendungen (wie der Automobilindustrie) verwendet wird.

1. **Übertragbarkeitskonformität:**
    - **Beispiel:** Ein Betriebssystem oder eine Anwendung könnte die **POSIX (Portable Operating System Interface)** Standards einhalten, um sicherzustellen, dass sie portabel und kompatibel mit anderen POSIX-konformen Systemen ist.

## ISO 25000 vs ISO 9126
Die ISO 9126 Der Schwerpunkt lag auf der Qualitätsmodellierung und der Fähigkeit, sowohl interne als auch externe Qualitätsmerkmale zu messen.

Die ISO 25000 Normenreihe wurde später entwickelt, um ISO 9126 und einige andere zu ersetzen und zu erweitern, und bietet einen umfassenderen Ansatz für Softwareproduktqualität. Sie umfasst Anforderungen, Bewertungsprozesse und Qualitätsmodelle und berücksichtigt auch Qualitätsmanagement und Qualitätssicherungsprozesse.

Die ISO 25010 ist die Nachfolge-Norm der ISO 9126. Zu den Änderungen zählen auch zwei neue Hauptkategorien, die **IT-Sicherheit** und die **Kompatibilität**, die beide vorher Aspekte der Hauptkategorie „Funktionalität waren“:

## Qualitätskriterien nach ISO 25010
![[Pasted image 20231021221739.png]]


### Funktionalität (Functional Suitability)
- Übereinstimmung mit dem [[Pflichtenheft]]
- Abnahmetest
	- Ende u Ende Test
	- Blackbox Test
### Leistungsfähigkeit (Performance Efficiency)
- Leistungs Effizienz
- Ressourcenverbrauch (z.B. Hardware, Strom etc.)
- Monitoring des Verbrauchs
	- Task Manager
	- Profiler
	- Zeitmessung
		- Wie lange dauert ein Use case
		- Wie lange benötigt die Software zum starten.
### Kompatibilität (Compatibility)
- Backwards Compatibility
- Kompatibilität mit anderer Software und Betriebssystemen
- Platformunabhängigkeit
	- Sprache
	- Container
	- Architektur (z.B. Webanwendung)
- Einhalten von Schnittstellen standards
	- z.B. Protokolle (Httpt)
	- Formate (JSON, YAML, TOML etc.)
	- Einhalten von Hardware standards (USB, SPI etc.)
- Dependencies zu Bibliotheken reduzieren
### Benutzbarkeit (Usability)
- Wie Anwenderfreundlich ist das System?
-  Barrierefreiheit
- Usability-Test
- Auswetungen und Umfragen
- Eyetracking
- Benutzerfreundliches einfaches intuitives GUI Desgin
- Bedienungsanleitung
### Zuverlässigkeit (Reliability)
- Zuverlässigkeit und Ausfallsicherheit
- Zuverlässige Hardware
- Redundanz
- Spiegelung von systemen
### Sicherheit (Security)
- Integrität und Datenschutz
- Verschlüsselung
- Zugriffskontrolle
- [[Penetration Testing]]
- Sanitizing of user input

### Wartbarkeit (Maintainability)
- Wie gut können Anpassungen vorgenommen werden oder Funktionen erweitert werden.
- Grad der Wartbarkeit
- Nutzen von Desingpattern
- Clean Code
- Code Kommentare
- Befolgen von styleguides
- Dokumentation
	- Nutzerdokumentation
	- Softwaredokumnetation
	- Projektdokumentation
- Nutzen von Version Control Software (git)
### Übertragbarkeit (Portability)
- Platformunabhängikeit
- Vermeidung von plattformspezifischer Abhängigkeiten

# Softwareanforderungen
Viele Lasten und Pflichtenhefte unterscheiden zwischen Funktionalen und nicht Funktionalen anforderungen.
## Funktionale Anforderungen
Diese beziehen sich auf die spezifischen Funktionen, die ein System oder Softwareprodukt erfüllen soll. Sie beschreiben, was das System tun soll und beinhalten spezifische Features, Interaktionen und Verhaltensweisen des Systems unter bestimmten Bedingungen. Funktionale Anforderungen machen eine Aussage über eine zu erfüllende Eigenschaft oder zu erbringende Leistung eines Produktes, Systems oder Prozesses

### Beispiele:
1. **Benutzerverwaltung**:
    - Anlegen, Bearbeiten und Löschen von Benutzerprofilen.
    - Rollenbasierte Zugriffssteuerung.
2. **Datenverarbeitung**:
    - Erfassung und Speicherung von Kundendaten.
    - Import und Export von Daten in verschiedenen Formaten (z.B. CSV, XML).
3. **Suchfunktion**:
    - Ermöglichen der Suche nach spezifischen Einträgen in der Datenbank.
    - Bereitstellung von Filter- und Sortieroptionen.
4. **Berichterstellung**:
    - Generierung von Berichten basierend auf den gespeicherten Daten.
    - Möglichkeit, Berichte in verschiedenen Formaten (z.B. PDF, Word) zu exportieren.

## Nicht Funktionale Anforderungen
Diese Anforderungen beziehen sich auf die Qualitätsaspekte des Systems oder der Software. Sie definieren, wie gut das System seine Funktionen ausführt und beinhalten Aspekte wie Benutzerfreundlichkeit, Effektivität, Sicherheit, Skalierbarkeit usw. Nicht-funktionale Anforderungen bestimmen die Leistungsstandards und Qualitätsmerkmale der Software und beschreiben, WIE das System seine Funktionen ausführt

### Beispiele:
1. **Performance**:
    - Antwortzeit des Systems bei Anfragen.
    - Maximale Zeit für die Datenverarbeitung.
2. **Skalierbarkeit**:
    - Fähigkeit des Systems, mit einer steigenden Anzahl von Benutzern oder Datenmengen umzugehen.
    - Möglichkeiten zur Erweiterung des Systems.
3. **Sicherheit**:
    - Datenschutz und Compliance mit relevanten Gesetzen und Standards (z.B. GDPR).
    - Sicherheitsmaßnahmen gegen unautorisierten Zugriff und Datenverlust.
4. **Benutzerfreundlichkeit (Usability)**:
    - Einfachheit der Benutzeroberfläche.
    - Verfügbarkeit von Hilfe und Dokumentation für die Benutzer.
