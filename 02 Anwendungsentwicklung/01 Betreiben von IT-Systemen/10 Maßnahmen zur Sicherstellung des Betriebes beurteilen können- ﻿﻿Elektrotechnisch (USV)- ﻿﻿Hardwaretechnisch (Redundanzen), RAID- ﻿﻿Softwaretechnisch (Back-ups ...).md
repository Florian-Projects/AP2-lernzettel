
> [!cite] Inhalt
> 10 Maßnahmen zur Sicherstellung des Betriebes beurteilen können
> 
> - ﻿﻿Elektrotechnisch (USV)
> - ﻿﻿Hardwaretechnisch (Redundanzen), RAID
> - ﻿﻿Softwaretechnisch (Back-ups ...)

### Elektrotechnisch: USV (Unterbrechungsfreie Stromversorgung)
- **Funktion**: Eine USV schützt vor Stromausfällen und Spannungsschwankungen, indem sie bei Bedarf sofort Energie aus Batterien bereitstellt.
- **Beurteilung**: USVs sind unerlässlich für den Schutz kritischer Systeme. Sie ermöglichen es, im Falle eines Stromausfalls die Systeme ordnungsgemäß herunterzufahren oder den Betrieb aufrechtzuerhalten, bis ein Generator anspringt oder die Stromversorgung wiederhergestellt ist.
- **Wichtigkeit**: Besonders für Server, Netzwerkgeräte und Datenzentren kritisch.

### Hardwaretechnisch: Redundanzen, RAID (Redundant Array of Independent Disks)
- **Redundanzen**: Das Vorhandensein von mehrfacher Ausstattung (z.B. doppelte Netzteile, mehrere Netzwerkpfade).
  - **Beurteilung**: Redundanzen sind entscheidend, um den Ausfall einzelner Komponenten zu kompensieren, ohne dass es zu einem Gesamtsystemausfall kommt.
- **RAID**: Ein System zur Datenorganisation auf mehreren Festplatten, das Redundanz und/oder Leistungsverbesserung bietet.
  - Siehe [[#Raid Level]]
  - **Beurteilung**: RAID-Systeme sind wesentlich für die Datensicherheit und Verfügbarkeit. RAID-Level wie RAID 1 (Spiegelung) und RAID 5 (Striping mit Parität) sind gängige Lösungen, um Daten vor dem Verlust durch einzelne Festplattenausfälle zu schützen.

#### Raid Level

RAID steht für "Redundant Array of Independent Disks" und ist eine Technologie, die mehrere Festplatten kombiniert, um die Ausfallsicherheit und/oder die Geschwindigkeit des Speicherzugriffs zu verbessern. Hier sind die gängigsten RAID-Level:

##### RAID 0 – Striping
- **Beschreibung**: Daten werden in Blöcken über mehrere Laufwerke verteilt, was die Lese- und Schreibgeschwindigkeit erhöht, da mehrere Laufwerke gleichzeitig genutzt werden.
- **Redundanz**: Keine; wenn ein Laufwerk ausfällt, gehen alle Daten verloren.
- **Ideal für**: Anwendungen, die hohe Geschwindigkeit erfordern und bei denen Datenverluste tolerierbar sind.

##### RAID 1 – Mirroring
- **Beschreibung**: Jedes Laufwerk hat ein exaktes Duplikat (Spiegel). Wenn Daten auf ein Laufwerk geschrieben werden, werden sie auch auf das andere geschrieben.
- **Redundanz**: Ja; wenn ein Laufwerk ausfällt, bleiben die Daten auf dem Spiegel erhalten.
- **Ideal für**: Kritische Anwendungen, bei denen Redundanz wichtiger ist als die Speichernutzung.

##### RAID 5 – Striping mit Parität
- **Beschreibung**: Daten und Paritätsinformationen werden über alle Laufwerke im Array verteilt. Die Paritätsinformation ermöglicht die Wiederherstellung von Daten im Falle des Ausfalls eines Laufwerks.
- **Redundanz**: Ja; ein Laufwerk kann ausfallen, ohne dass Daten verloren gehen.
- **Ideal für**: Server und Systeme, die eine gute Balance aus Leistung, Speicherplatz und Redundanz benötigen.

##### RAID 10 (1+0) – Mirroring und Striping
- **Beschreibung**: Eine Kombination aus RAID 1 und RAID 0, die die Vorteile von Mirroring und Striping bietet.
- **Redundanz**: Ja; mindestens ein Laufwerk jedes gespiegelten Paares kann ausfallen.
- **Ideal für**: Unternehmenskritische Anwendungen, die sowohl hohe Leistung als auch Redundanz erfordern.

### Softwaretechnisch: Back-ups
- **Funktion**: Regelmäßige Sicherungskopien von Daten und Systemkonfigurationen.
- **Beurteilung**: Back-ups sind ein Muss, um Datenverlust bei Hardwaredefekten, Softwarefehlern, Cyberangriffen oder Katastrophen zu verhindern. Wichtig ist eine Strategie, die berücksichtigt, wie oft Back-ups erstellt werden (Backup-Frequenz) [[#generationenprinzip]], wo sie gespeichert werden (onsite/offsite), und wie schnell sie wiederhergestellt werden können (Recovery Time Objectives (RTO) und Recovery Point Objectives (RPO)).
- **Aspekte**: Zuverlässige Back-up-Software, regelmäßige Tests der Wiederherstellung und Offsite-Back-up-Speicherung (z.B. Cloud-Back-up) sind wichtig, um die Effektivität zu gewährleisten.

#### generationenprinzip

https://de.wikipedia.org/wiki/Generationenprinzip

Das **Generationenprinzip**, auch **Großvater-Vater-Sohn-Prinzip** genannt, stellt in der [EDV](https://de.wikipedia.org/wiki/EDV "EDV") eine Strategie der [Datensicherung](https://de.wikipedia.org/wiki/Datensicherung "Datensicherung") dar. Es stellt sicher, dass immer mehrere Sicherungen in verschiedenen zeitlichen Abstufungen (Großvater, Vater, Sohn) vorhanden sind

### Softwaretechnisch: Patch-Management

- **Beschreibung**: Sicherstellen, dass Software auf dem neuesten Stand ist durch regelmäßige Updates und Patches.
- **Ziel**: Schließen von Sicherheitslücken und Vermeidung von Ausfällen durch Softwarefehler.

### Softwaretechnisch: Disaster Recovery Planung

- **Beschreibung**: Erstellung und Wartung von Plänen für den Fall eines kompletten Systemausfalls.
- **Ziel**: Schnelle Wiederherstellung der IT-Systeme und Minimierung der Downtime.

### Softwaretechnisch: Failover- und Clustering-Lösungen

- **Beschreibung**: Automatisches Umschalten auf ein Redundanzsystem bei Ausfall des primären Systems.
- **Ziel**: Gewährleistung der Hochverfügbarkeit von kritischen Anwendungen und Diensten.

### Softwaretechnisch: Load Balancing

- **Beschreibung**: Verteilung der Arbeitslast über mehrere Server, um Überlastung zu vermeiden.
- **Ziel**: Steigerung der Leistung und Reduzierung von Ausfallrisiken durch Überlastung.

### Softwaretechnisch: Monitoring und Alarmierung

- **Beschreibung**: Überwachung von Systemen und Infrastruktur auf Anomalien und Leistungsprobleme.
- **Ziel**: Frühzeitige Erkennung von potenziellen Problemen und sofortige Benachrichtigung der zuständigen Teams.

### Softwaretechnisch: Antivirus- und Anti-Malware-Software

- **Beschreibung**: Schutz vor Schadsoftware durch regelmäßige Scans und Echtzeit-Überwachung.
- **Ziel**: Verhinderung von Datenverlust oder -beschädigung durch Viren, Würmer, Trojaner und andere Malware.