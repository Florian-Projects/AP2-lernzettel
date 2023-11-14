# Richtschnur für Entwickler
Dies bezieht sich auf die Leitlinien oder Standards, die Entwicklerteams befolgen sollten, um die Sicherheit während des gesamten Lebenszyklus der Anwendungsentwicklung zu gewährleisten. Dies umfasst sichere Codierungsstandards, regelmäßige Sicherheitsüberprüfungen, Penetrationstests und die Integration von Sicherheitsüberlegungen in die frühen Phasen des Entwicklungsprozesses.

# Objektive Bewertung der Systeme 
Dies beinhaltet die Verwendung von standardisierten, unvoreingenommenen Methoden zur Bewertung der Sicherheit von IT-Systemen. Es könnte die Anwendung von Frameworks wie ISO 27001, Penetrationstests, Sicherheitsaudits und Vulnerability Assessments umfassen, um eine gründliche Analyse zu gewährleisten.

## IT-Grundschutz Modellierung
Dieser Ansatz, entwickelt vom Bundesamt für Sicherheit in der Informationstechnik (BSI) in Deutschland, zielt darauf ab, Unternehmen dabei zu unterstützen, die erforderlichen Sicherheitsmaßnahmen in einer strukturierten und gründlichen Weise zu identifizieren. Der Prozess umfasst:

1. Strukturanalyse: Identifizierung aller kritischen Ressourcen und Prozesse.
2. Schutzbedarfsfeststellung: Bestimmung des notwendigen Schutzniveaus für jede Identifizierte Information und jedes System basierend auf Vertraulichkeit, Integrität und Verfügbarkeit.
3. Modellierung: Zuordnung zu den Standard-Sicherheitsbausteinen des BSI-Grundschutz-Kompendiums.
4. Basis-Sicherheitscheck: Vergleich des aktuellen Sicherheitsstatus mit den Grundschutz-Standards.
5. Risikoanalyse: Identifizierung und Bewertung von Risiken, die nicht durch die Basis-Sicherheitsmaßnahmen abgedeckt sind.
6. Ergänzende Sicherheitsanalyse und Umsetzung: Anwendung zusätzlicher Sicherheitsmaßnahmen, wo das Risikoniveau dies erfordert.

# Anwender/ Benutzer bei der Auswahl eines geeigneten IT-Sicherheitsprodukts unterstutzen
## Security by design


# IT Grundschutz
Eine vom BSI entwickelte vorgehensweise zum Identifizieren und Umsetzen von Sicherheitsmaßnahmen der unternehmenseigenen Informationstechnik.
Das Ziel des Grundschutzes ist das Erreichen eines mittleren, angemessenen und ausreichenden Schutzniveaus für IT-Systeme.

## Sicherheitsziele
1. **Vertraulichkeit:**
    - Hierbei geht es um die Frage, wer Zugriff auf bestimmte Informationen haben darf. Vertrauliche Daten sollen vor unbefugtem Zugriff geschützt werden. Die Einstufung des Schutzbedarfs hängt davon ab, welche Auswirkungen ein unbefugter Informationszugriff hätte.
2. **Integrität:**
    - Dieses Kriterium befasst sich mit der Korrektheit und Vollständigkeit der Daten und Informationen. Ein hoher Schutzbedarf besteht, wenn Veränderungen an Daten, die unbemerkt bleiben, zu schweren Schäden führen könnten, beispielsweise bei Finanztransaktionen oder Patientendaten im Gesundheitswesen.
3. **Verfügbarkeit:**
    - Hier steht die Verfügbarkeit der IT-Systeme und Informationen im Vordergrund. Ein hoher Schutzbedarf ist gegeben, wenn Ausfallzeiten zu erheblichen Beeinträchtigungen oder Schäden führen würden, wie es zum Beispiel bei Notfalldiensten oder kritischen Produktionsanlagen der Fall sein könnte.

## Schutzbedarfskategorien
- **normal:** Die Schadensauswirkungen sind begrenzt und überschaubar.
- **hoch**: Die Schadensauswirkungen können beträchtlich sein.
- **sehr hoch**: Die Schadensauswirkungen können ein existentiell bedrohliches, katastrophales Ausmaß erreichen.


## IT Grunschutz modellierung beispiel:
1. **Definition des Untersuchungsbereichs**
    - Das Unternehmen "Beispiel AG" hat entschieden, seine IT nach IT-Grundschutz zu zertifizieren. Als ersten Schritt definiert das IT-Sicherheitsteam die Untersuchungsbereiche, welche die IT-Infrastruktur, Anwendungen und Geschäftsprozesse umfassen.

1. **Strukturanalyse**
    - Das Team erstellt eine Liste aller IT-Systeme, Netzwerkkomponenten, Anwendungen und Prozesse. Zum Beispiel:
        - Server (Mail, Datenbank, Web, Anwendungsserver etc.)
        - Client-Systeme (Arbeitsplatzrechner, Laptops, mobile Endgeräte)
        - Netzwerkgeräte (Router, Switches, Firewalls)
        - Spezielle Systeme (Telefonanlagen, Sicherheitssysteme)
        - Geschäftsprozesse (Kundenmanagement, Rechnungswesen, Personalwesen)
2. **Schutzbedarfsfeststellung**
    - Für jedes Element wird der Schutzbedarf in den Kategorien "hoch", "mittel" und "niedrig" für die Aspekte der Verfügbarkeit, Integrität und Vertraulichkeit festgelegt. Zum Beispiel könnte der Mail-Server eine hohe Verfügbarkeit erfordern, während die Integrität der Datenbankdaten als kritisch eingestuft wird.
4. **Modellierung**
    - Basierend auf der Schutzbedarfsfeststellung werden den identifizierten IT-Systemen und Prozessen geeignete Bausteine aus dem IT-Grundschutz-Kompendium zugeordnet. Jeder Baustein beschreibt Standard-Sicherheitsmaßnahmen für typische IT-Konstellationen. Die Zuordnung orientiert sich an den Anforderungen, die sich aus der Schutzbedarfsfeststellung ergeben.
    - **Beipiel: B 3.101 Webserver**:
	    -  Implementierung einer Firewall und eines Intrusion-Detection-System
	    - Regelmäßige Updates und Patches für das Webserver-System
	    - Verschlüsselung der Datenübertragung mittels TLS
	    - Zugriffskontrolle und Authentifizierung für administrative Zugänge
	    - Protokollierung und Monitoring der Webserver-Aktivitäten
1. **Basis-Sicherheitscheck**
    - Die gegenwärtige Umsetzung der IT-Sicherheitsmaßnahmen wird mit den Vorgaben aus den zugeordneten Grundschutz-Bausteinen verglichen. Hierzu könnte das Team eine Liste von Maßnahmen erstellen und überprüfen, welche bereits umgesetzt sind und welche noch angegangen werden müssen.
6. **Risikoanalyse**
    - Für Bereiche, die über den Basis-Schutz hinausgehen oder bei denen ein erhöhtes Risiko besteht, führt das Team eine detaillierte Risikoanalyse durch. Hier werden Bedrohungen und Schwachstellen spezifisch analysiert und das Risiko bewertet.
7. **Umsetzungsplanung**
    - Auf Basis der Risikoanalyse wird ein Umsetzungsplan entwickelt, der Maßnahmen zur Behandlung der identifizierten Risiken beinhaltet. Dies kann beispielsweise das Implementieren neuer Sicherheitssoftware, das Verstärken physischer Sicherheitsmaßnahmen oder das Durchführen von Schulungen für Mitarbeiter umfassen.
8. **Realisierung und Überprüfung**
    - Die Maßnahmen werden umgesetzt und in einem regelmäßigen Turnus überprüft, um sicherzustellen, dass sie effektiv sind und der Schutzbedarf gedeckt bleibt.
9. **Dokumentation und Verbesserung**
    - Alle Schritte, Maßnahmen und Änderungen werden dokumentiert. Die Dokumentation dient als Grundlage für die kontinuierliche Verbesserung des Sicherheitsniveaus und für Audits.
10. **Zertifizierung**
    - Nach Durchführung und Dokumentation der erforderlichen Maßnahmen kann die "Beispiel AG" bei einer akkreditierten Zertifizierungsstelle ein Audit zur Erlangung des IT-Grundschutz-Zertifikats beantragen.

# Beispielhaftes erstellen von Ziele
1. **Gewährleistung der Vertraulichkeit:**
    
    - Sicherstellen, dass Informationen nur für autorisierte Personen zugänglich sind.
    - Entwicklung von Zugriffskontrollsystemen, die den Zugriff auf sensible Daten regulieren.
2. **Integrität von Daten und Systemen bewahren:**
    
    - Schutz vor unbefugten Änderungen an Daten oder Software.
    - Implementierung von Maßnahmen zur Erkennung und Behebung von Datenkorruption.
3. **Aufrechterhaltung der Verfügbarkeit:**
    
    - Sicherstellen, dass IT-Systeme und Informationen immer dann verfügbar sind, wenn sie benötigt werden.
    - Entwicklung von Redundanz und Failover-Strategien zur Minimierung von Ausfallzeiten.
4. **Unterstützung der Authentizität:**
    
    - Verifikation der Identität von Benutzern, Systemen und Daten.
    - Einsatz von Authentifizierungstechnologien wie Multi-Faktor-Authentifizierung.
5. **Sicherstellung der Nachvollziehbarkeit (Accountability):**
    
    - Dokumentation und Überwachung von Aktivitäten in IT-Systemen zur Sicherstellung, dass Handlungen einzelnen Benutzern zugeordnet werden können.
6. **Gewährleistung der Compliance:**
    
    - Einhaltung relevanter Gesetze, Vorschriften und Standards (wie DSGVO, ISO/IEC 27001, BSI IT-Grundschutz).
    - Regelmäßige Überprüfungen und Anpassungen der Sicherheitsrichtlinien und -verfahren.
7. **Risikomanagement:**
    
    - Identifikation, Bewertung und Steuerung von Risiken für IT-Systeme.
    - Entwicklung eines Prozesses für Risikoanalysen und -bewertungen.
8. **Prävention und Reaktion auf Sicherheitsvorfälle:**
    
    - Entwicklung und Implementierung von Incident-Response-Plänen.
    - Schulung der Mitarbeiter in Sicherheitsbest practices und im Umgang mit Vorfällen.
9. **Sicherheitsbewusstsein und Schulung:**
    
    - Schaffung eines Bewusstseins für Sicherheitsrisiken und die Wichtigkeit von Sicherheitsmaßnahmen bei allen Mitarbeitern.
    - Regelmäßige Schulungen und Kampagnen zur Sicherheitsaufklärung.
10. **Business Continuity und Disaster Recovery:**
    
    - Sicherstellung, dass das Unternehmen nach einem Sicherheitsvorfall oder einer Katastrophe seine kritischen Funktionen schnell wieder aufnehmen kann.
    - Erstellung und Testung von Notfallwiederherstellungsplänen.