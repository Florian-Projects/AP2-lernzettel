
> [!cite] Inhalt
> 03 ﻿﻿﻿Netzwerkkonzepte (-topologien, -infrastruk-turen) benennen und charakterisieren
> - ﻿﻿Ausdehnung
> - ﻿﻿Datenübertragungsrate
> - ﻿﻿Verschlüsselung (preshared key, RADIUS ...)
> - ﻿﻿LAN/WAN/MAN/GAN
> - ﻿﻿Strukturierte Verkabelung
> - ﻿﻿VLAN
> - ﻿﻿Drahtlos: PAN/WLAN
> - ﻿﻿Sicherheitskonzepte und -risiken
> - ﻿﻿Bluetooth

## Netzwerkkonzepte

Netzwerkkonzepte und -topologien sind ein fundamentaler Teil der IT-Infrastruktur und somit auch ein wichtiger Aspekt der Ausbildung im Bereich Fachinformatik für Anwendungsentwicklung. Hier sind einige Grundlagen, die du kennen solltest:

### Netzwerktopologien:

![[Pasted image 20231029182002.png]]
Netzwerktopologien beschreiben die Anordnung verschiedener Netzwerkkomponenten. Zu den gängigsten Topologien gehören:

1. **Bus-Topologie:**
   - Alle Geräte sind an ein gemeinsames Übertragungsmedium angeschlossen, das als Bus bezeichnet wird.
   - Vorteil: Einfach zu implementieren und zu erweitern.
   - Nachteil: Wenn das gemeinsame Medium ausfällt, sind alle Anschlüsse betroffen.

2. **Stern-Topologie:**
   - Alle Geräte sind über eigene Kabel mit einem zentralen Knotenpunkt (z.B. ein Switch) verbunden.
   - Vorteil: Zentrale Verwaltung und einfache Fehlersuche.
   - Nachteil: Wenn der zentrale Knotenpunkt ausfällt, sind alle Verbindungen betroffen.

3. **Ring-Topologie:**
   - Die Geräte sind in einem geschlossenen Ring verbunden, wobei jedes Gerät genau zwei Nachbarn hat.
   - Vorteil: Einfache Datenübertragung in eine Richtung.
   - Nachteil: Ein Bruch der Verbindung kann das gesamte Netzwerk lahmlegen.

4. **Maschen-Topologie (Mesh):**
   - Jedes Gerät ist mit mehreren anderen verbunden, sodass es mehrere Pfade für die Datenübertragung gibt.
   - Vorteil: Hohe Ausfallsicherheit durch redundante Verbindungen.
   - Nachteil: Hoher Verkabelungsaufwand und schwierigere Verwaltung.

5. **Baum-Topologie:**
   - Eine Kombination aus Stern- und Bus-Topologie, bei der Sternpunkte in einer hierarchischen Weise verbunden sind.
   - Vorteil: Erweiterung von Bus- und Stern-Topologien.
   - Nachteil: Hierarchische Struktur kann die Komplexität erhöhen.

### Netzwerkinfrastrukturen:
Die Netzwerkinfrastruktur umfasst die Hardware, Software, Netzwerkdienste und Protokolle, die für die Kommunikation und den Betrieb eines Netzwerks notwendig sind. Wesentliche Elemente sind:

- **Router:** Geräte, die Netzwerkpakete zwischen verschiedenen Netzwerken weiterleiten.
- **Switches:** Geräte, die Netzwerkgeräte innerhalb eines Netzwerks verbinden und Datenpakete gezielt weiterleiten können.
- **Firewalls:** Systeme, die das Netzwerk vor unautorisierten Zugriffen schützen.
- **Gateways:** Verbinden Netzwerke mit unterschiedlichen Protokollen.
- **Kabel und Funktechnologien:** Ethernet-Kabel, Glasfaserkabel, WLAN, etc.
- **Protokolle:** TCP/IP, HTTP, FTP, etc., die die Regeln für die Kommunikation definieren.

### Charakterisierung von Netzwerken:
Beim Charakterisieren von Netzwerken sollten folgende Aspekte berücksichtigt werden:

- **Skalierbarkeit:** Die Fähigkeit des Netzwerks, mit der Anzahl der Benutzer oder des Datenverkehrs zu wachsen.
- **Ausfallsicherheit:** Wie gut das Netzwerk gegen Ausfälle geschützt ist.
- **Performance:** Die Datenübertragungsraten und die Latenz im Netzwerk.
- **Sicherheit:** Maßnahmen zum Schutz vor unerlaubtem Zugriff und Datenverlust.
- **Verwaltbarkeit:** Die Einfachheit, mit der das Netzwerk konfiguriert und gewartet werden kann.

Vergewissere dich, dass du nicht nur die Begriffe kennst, sondern auch verstehst, wie diese in realen Szenarien angewendet werden und welche Vor- und Nachteile sie mit sich bringen.

## Alle Unterpunkte

### Ausdehnung:

Die physische Ausdehnung eines Netzwerks ist ein grundlegendes Klassifizierungsmerkmal und kann variieren von:

- **Personal Area Network (PAN):** Sehr kleine Netzwerke, oft für persönliche Geräte.
- **Local Area Network (LAN):** Netzwerk in einem begrenzten geographischen Bereich wie einem Büro oder Gebäude.
- **Metropolitan Area Network (MAN):** Städtisches Netzwerk, das mehrere Gebäude in einer größeren geographischen Fläche, wie einer Stadt, verbindet.
- **Wide Area Network (WAN):** Netzwerk, das große geographische Gebiete oder sogar ganze Länder und Kontinente umfasst.
- **Global Area Network (GAN):** Ein Netzwerk, das über Satellitenkommunikation oder andere drahtlose Technologien verbindet und weltweite Abdeckung bietet.

### Datenübertragungsrate:

Die Geschwindigkeit, mit der Daten über ein Netzwerk übertragen werden, oft gemessen in Megabit pro Sekunde (Mbit/s) oder Gigabit pro Sekunde (Gbit/s). Diese Rate kann je nach Technologie und Medium stark variieren.

### Verschlüsselung:

Verschlüsselungsprotokolle wie WPA2 mit einem Pre-shared Key (PSK) oder der Einsatz von RADIUS-Servern für die Authentifizierung sind entscheidend für die Sicherheit in Netzwerken. Sie sorgen dafür, dass übertragene Informationen nicht von Unbefugten eingesehen werden können.

### LAN/WAN/MAN/GAN:

Diese Abkürzungen beziehen sich auf die geographische Ausdehnung von Netzwerken, wie oben beschrieben.

### Strukturierte Verkabelung:

Das ist ein standardisierter Ansatz für die Verkabelung von Daten- und Telekommunikationsnetzwerken, der modulare und flexible Lösungen für Gebäude oder Campus-Umgebungen bietet.

### VLAN (Virtual Local Area Network):

Ein VLAN ist ein logisch segmentiertes Netzwerk innerhalb eines physikalischen LANs, das es erlaubt, Gruppen von Endgeräten unabhängig von ihrer physischen Lage zu trennen und zu verwalten, was die Sicherheit und Effizienz verbessert.

### Drahtlos: PAN/WLAN:

- **PAN (Personal Area Network):** Ein Netzwerk für persönliche Geräte, oft basierend auf Technologien wie Bluetooth oder NFC.
- **WLAN (Wireless Local Area Network):** Kabelloses Netzwerk, das typischerweise in einem geographisch begrenzten Bereich wie einem Haus oder Bürogebäude eingesetzt wird.

### Sicherheitskonzepte und -risiken:

Die Implementierung von Sicherheitsrichtlinien, die Nutzung von Firewalls, Anti-Malware-Programmen, Intrusion-Detection-Systemen und regelmäßigen Updates sind entscheidend, um Risiken wie Datenverlust, Cyberangriffe und unbefugten Zugriff zu minimieren.

### Bluetooth:

Eine drahtlose Technologie, die für die Erstellung von PANs verwendet wird und Geräte wie Smartphones, Kopfhörer und Computerperipheriegeräte über kurze Entfernungen verbindet.