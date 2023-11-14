# TOMS
Technisch Organisatorische Maßnahmen beschreiben maßnahmen, die dazu dienen den Schutz und Vertraulichkeit von IT-Systemen und Daten (DSGVO) zu gewährleisten.
Einige maßnahmen sind in § 64 Abs. 3 S.1 [[BDSG]] spezifiziert

## Technische Maßnahmen
### Zutrittskontrolle
Verwährungs des Zugangs zu Daten verarbeitungsnalagen. (Für unbefugte)
#### Maßnahmen
- Einsatz von Sicherheitsschleusen und -schranken. 
- Biometrische Zugangssysteme wie Fingerabdruckscanner oder Gesichtserkennung.
- Schlüsselkarten- oder Token-basierte Zutrittssysteme.

### Zugangskontrolle
Verwehrung des Zugangs zu Verarbeitungsanlagen, mit denen die Verarbeitung durchgeführt wird, für Unbefugte
#### Maßnahmen
- Starke Authentifizierungsmethoden für Benutzer, z.B. Multi-Faktor-Authentifizierung. 
- Virtuelle private Netzwerke (VPNs) für sicheren Fernzugriff. 
- Automatische Sperre von Benutzerkonten nach mehreren fehlgeschlagenen Zugriffsversuchen.

### Zugriffskontrolle
Gewährleistung, dass die zur Benutzung eines automatisierten Verarbeitungssystems Berechtigten ausschließlich zu den von ihrer Zugangsberechtigung umfassten personenbezogenen Daten Zugang haben
#### Maßnahmen
- Berechtigungsmanagement und Zugriffsrechtevergabe auf das Prinzip der geringsten Privilegien basierend. 
- Dateisystem-Sicherheit mit verschlüsselten Dateiablagen.
- Protokollierung des Zugriffs auf Systeme und Daten.

### Transportkontrolle
Gewährleistung, dass bei der Übermittlung personenbezogener Daten sowie beim Transport von Datenträgern die Vertraulichkeit und Integrität der Daten geschützt werden
#### Maßnahmen
- Verschlüsselung von Daten bei der Übertragung über öffentliche Netzwerke. 
- Gesicherte und verschlüsselte Kommunikationskanäle wie HTTPS. 
- Sichere Transportbehälter und -verfahren für physische Datenträger.

### Weitergabekontrolle
Daten sind auf dem Transportweg geschützt. Können also von unbefugten nicht gelesen, modifiziert, gelöscht oder oder kopiert werden.
#### Maßnahmen
- Einsatz von End-to-End-Verschlüsselung für Daten, die zwischen Systemen übertragen werden.
- DLP-Lösungen (Data Loss Prevention) zur Überwachung und Verhinderung von ungewollten Datenübertragungen. 
- Strikte Konfiguration von Firewall- und Routing-Regeln, um Datenflüsse zu kontrollieren.

### Eingabekontrolle
Gewährleistung, dass nachträglich überprüft und festgestellt werden kann, welche personenbezogenen Daten zu welcher Zeit und von wem in automatisierte Verarbeitungssysteme eingegeben oder verändert worden sind
#### Maßnahmen
- Protokollierung von Systemeingriffen in Audit-Logs.
- Regelmäßige Überprüfungen der Protokolle auf unautorisierte Eingaben.
- Benutzerschnittstellen, die detaillierte Informationen über Eingabevorgänge anzeigen.

### Auftragskontrolle
Gewährleistung, dass personenbezogene Daten, die im Auftrag verarbeitet werden, nur entsprechend den Weisungen des Auftraggebers verarbeitet werden können
#### Maßnahmen
- Vertragliche Vereinbarungen mit Dienstleistern, die die Datenverarbeitung im Auftrag regeln. 
- Regelmäßige Überprüfungen der Einhaltung dieser Vereinbarungen durch die Dienstleister. 
- Technische und organisatorische Maßnahmen bei den Dienstleistern zur Sicherung der Weisungstreue.

### Verfügbarkeitskontrolle
Gewährleistung, dass personenbezogene Daten gegen Zerstörung oder Verlust geschützt sind
#### Maßnahmen
- Redundante Systemauslegung und regelmäßige Backups.
- Einsatz von Hochverfügbarkeitslösungen und Failover-Systemen.
- Anti-DDoS-Strategien und -Lösungen zur Sicherstellung der Dienstverfügbarkeit.

### Wiederherstellbarkeit
Gewährleistung, dass eingesetzte Systeme im Störungsfall wiederhergestellt werden können
#### Maßnahmen
- Disaster-Recovery-Pläne und Business-Continuity-Management.
- Regelmäßige Tests von Backup- und Wiederherstellungsprozeduren.
- Dokumentation der Wiederherstellungsprozeduren.

### Trennbarkeit
ewährleistung, dass zu unterschiedlichen Zwecken erhobene personenbezogene Daten getrennt verarbeitet werden können
#### Maßnahmen
- Datenspeicherung in getrennten Datenbanken oder Schemas. 
- Implementierung von Softwarelösungen, die eine Mandantentrennung ermöglichen. 
- Physikalische Trennung von Netzwerken und Speichersystemen für unterschiedliche Datensätze.

### Datenintegrität
Gewährleistung, dass gespeicherte personenbezogene Daten nicht durch Fehlfunktionen des Systems beschädigt werden können
#### Maßnahmen
- Einsatz von Checksummen und Hash-Funktionen zur Sicherung der Datenintegrität.
- Versionierungssysteme zur Nachverfolgung von Änderungen an Daten. 
- Regelmäßige Integritätsprüfungen der Datenbestände.

## Organisatorische Maßnahmen
- **Dokumentenmanagement:** Richtlinien für die sichere Speicherung und Vernichtung von Dokumenten. Implementierung von Versionierungssystemen, um die Verwendung aktueller und genehmigter Dokumentversionen sicherzustellen.
- **Notfallplanung:** Etablierung und regelmäßige Tests von Notfallplänen für den Umgang mit Datenpannen oder Sicherheitsverletzungen. Durchführung einer Business Impact Analysis zur Bewertung der Auswirkungen von Betriebsstörungen. 
- **Auditierung und Compliance:** Organisation regelmäßiger interner und externer Audits zur Überwachung der Datenschutzrichtlinien und Sicherstellung der Einhaltung relevanter Gesetze und Branchennormen.

## Personelle Maßnahmen
- **Einstellungsverfahren:** Sicherheitsüberprüfungen bei neuen Mitarbeitern und Durchführung von Datenschutzschulungen bereits im Rahmen des Onboarding-Prozesses. 
- **Rollen- und Verantwortungsdefinition:** Klare Zuordnung von Verantwortlichkeiten im Bereich Datenschutz und Informationssicherheit und Bestellung spezifischer Beauftragter für diese Bereiche. 
- **Sicherheitskultur:** Aufbau einer Sicherheitskultur, die das Sicherheitsbewusstsein der Mitarbeiter schärft. Regelmäßige Veranstaltungen und Schulungen zur Informationssicherheit.

# Log Management 
Log-Management ist der Prozess des Sammelns, Konsolidierens, Analysierens und Speicherns von Log-Daten von verschiedenen Systemen innerhalb einer Organisation. Ziel ist es, einen Überblick über die Sicherheitslage zu erhalten, Vorfälle zu erkennen und darauf reagieren zu können. Wichtig ist hierbei die Sicherstellung der Integrität und die Nachvollziehbarkeit der Log-Daten, um zum Beispiel im Falle einer Sicherheitsverletzung die Ursache ermitteln und die Verantwortlichen identifizieren zu können. 
# Compliance Reports 
Compliance-Reports dienen dazu, den Nachweis zu erbringen, dass eine Organisation den relevanten gesetzlichen Bestimmungen, Standards und Richtlinien, die auf sie zutreffen, entspricht. Dazu gehören zum Beispiel Datenschutzgesetze wie die DSGVO oder Industrienormen wie ISO-Standards. Compliance-Reports sind oft Bestandteil von Auditierungen und helfen, Transparenz gegenüber Regulierungsbehörden und Partnern zu schaffen. 

# Vorgehen 
## Privacy by Design 
Privacy by Design ist ein Ansatz in der Systementwicklung, bei dem Datenschutz und Datensicherheit von Anfang an in die Produkt- und Systementwicklung integriert werden. Das bedeutet, dass Datenschutzmaßnahmen nicht nachträglich als Add-on implementiert, sondern als Grundprinzip in der Architektur und im Designprozess berücksichtigt werden. Dies soll sicherstellen, dass der Datenschutz systematisch und umfassend in die technische und organisatorische Struktur eines Unternehmens eingebettet ist. 
## Privacy by Default 
Privacy by Default bedeutet, dass die Standardeinstellungen eines Produktes oder Systems so gestaltet sind, dass sie von Anfang an den höchstmöglichen Datenschutz bieten. Der Nutzer soll nicht erst Einstellungen ändern müssen, um seine Privatsphäre zu schützen. Stattdessen sollen die Datenschutzeinstellungen bereits in der Voreinstellung so gewählt sein, dass sie nur minimale Daten erfassen und verarbeiten.


# Zutrittskontrolle
## Alarmanlage
## Videoüberwachung
## Besucherausweise
# Zugangskontrolle
## Bildschirmschoner mit Passwortschutz
## Biometrische Verfahren
## Magnet oder Chipkarten
# Zugriffskontrolle
## Verschlüsselung
## Löschung von Datenträgern
## User/ Rollenkonzept