
## Inhalt

> [!cite] Inhalt
> 01 Schichtenmodelle, z. B. OSI, TCP/IP benennen und zuordnen können
> 
> - ﻿﻿IPv4/IPv6
> - ﻿﻿МАС
> - ﻿﻿Routing
> - ﻿﻿Switching
> - ﻿﻿ARP

### OSI Modell


![[Pasted image 20231029174357.png]]
![[Pasted image 20231029170337.png]]
#### Kurzbeschreibung des OSI-Schichtenmodells

7. Schicht / **Anwendung**: Funktionen für Anwendungen, sowie die Dateneingabe und -ausgabe.  
6. Schicht / **Darstellung**: Umwandlung der systemabhängigen Daten in ein unabhängiges Format.  
5. Schicht / **Kommunikation**: Steuerung der Verbindungen und des Datenaustauschs.  
4. Schicht / **Transport**: Zuordnung der Datenpakete zu einer Anwendung.  
3. Schicht / **Vermittlung**: Routing der Datenpakete zum nächsten Knoten.  
2. Schicht / **Sicherung**: Segmentierung der Pakete in Frames und Hinzufügen von Prüfsummen.  
1. Schicht / **Bitübertragung**: Umwandlung der Bits in ein zum Medium passendes Signal und physikalische Übertragung.
### TCP/IP

https://www.ionos.de/digitalguide/server/knowhow/tcpip-vorgestellt/

- **Netzzugangsschicht**: Diese Schicht ist im Referenzmodell zwar vorgesehen, es wird aber kein bestimmtes Protokoll definiert. In der Praxis kommen vor allem Ethernet (Kabel) und IEEE 802.11 (Funk) zum Einsatz. Die Netzzugangsschicht sorgt für die Verknüpfung von verschiedenen Subnetzen und verbindet so beispielsweise das heimische WLAN per Router mit dem Internet.
- **Internetschicht**: Auf dieser Schicht arbeitet das Internet Protocol und sorgt dafür, dass die transportierten Daten auch das richtige Ziel erreichen. Über die IP-Adresse werden die Datenpakete durch das Netzwerk geroutet.
- **[Transportschicht](https://www.ionos.de/digitalguide/server/knowhow/transportschicht/ "Transportschicht")**: Für den Transport sorgt im Referenzmodell TCP. Das Protokoll ermöglicht die Ende-zu-Ende-Kommunikation, ist also verantwortlich für die Verbindung zwischen zwei Geräten. Neben TCP gehört auch UDP in diese Ebene.
- **[Anwendungsschicht](https://www.ionos.de/digitalguide/server/knowhow/anwendungsschicht/ "Anwendungsschicht")**: Die Kommunikation der Programme über das Netzwerk wird in der obersten Schicht geregelt. Maßgeblich sind hier z. B. HTTP und FTP. Aber auch die E-Mail-Kommunikation (mit POP oder SMTP) funktioniert auf dieser Ebene.
### **IPv4/IPv6**:

**Internet Protocol** (**IP**)
 
- Ebene: Netzwerkebene (Schicht 3)
- Beschreibung: Diese beiden sind Internet-Protokolle, die dazu dienen, Datenpakete von einem Netzwerkgerät zu einem anderen zu leiten. Sie sind verantwortlich für die Adressierung und das Routing von Datenpaketen im Internet.

IP steht für "Internet Protocol". Es ist ein Satz von Regeln, die die Kommunikation zwischen Computern in einem Netzwerk regeln. IP-Adressen sind ein zentraler Bestandteil des IP-Protokolls, da sie die Identifikation und Lokalisierung von Geräten im Netzwerk ermöglichen. Es gibt zwei Hauptversionen des Internet-Protokolls: IP Version 4 (IPv4) und IP Version 6 (IPv6).

1. **IPv4**:
    
    - **Adressierung**: IPv4 verwendet 32-Bit-Adressen, was zu etwa 4,3 Milliarden einzigartigen Adressen führt. Diese Adressen werden normalerweise in dezimaler Punktnotation geschrieben, zum Beispiel 192.168.1.1.
    - **Adressraum**: Der begrenzte Adressraum von IPv4 führt zu einer Adressknappheit, da immer mehr Geräte mit dem Internet verbunden werden.
    - **NAT (Network Address Translation)**: Aufgrund der Adressknappheit ist es häufig notwendig, NAT zu verwenden, um mehrere Geräte hinter einer einzigen öffentlichen IP-Adresse zu verbergen.
2. **IPv6**:
    
    - **Adressierung**: IPv6 verwendet 128-Bit-Adressen, was zu einer nahezu unbegrenzten Anzahl von einzigartigen Adressen führt (etwa 340 Undezillionen). Diese Adressen werden in hexadezimaler Notation geschrieben, zum Beispiel 2001:db8::ff00:42:8329.
    - **Erweiterter Adressraum**: Der größere Adressraum ermöglicht eine einfachere Adressierung und bessere Skalierbarkeit, um dem Wachstum des Internets gerecht zu werden.
    - **Verbesserte Funktionen**: IPv6 bietet verbesserte Routing- und Netzwerkkonfigurationsfunktionen im Vergleich zu IPv4, sowie eingebaute Sicherheitsfunktionen und bessere Mobilitätsunterstützung.

IPv6 wurde entwickelt, um die Einschränkungen von IPv4 zu überwinden, insbesondere die begrenzte Anzahl von verfügbaren IP-Adressen. Die Umstellung von IPv4 auf IPv6 ist jedoch ein langwieriger Prozess, da viele Netzwerke und Geräte nach wie vor IPv4 verwenden und eine Rückwärtskompatibilität erforderlich ist.

### **MAC (Media Access Control) Adresse**:

- Ebene: Verbindungsschicht (Schicht 2)
- Beschreibung: Die MAC-Adresse ist eine eindeutige Hardware-Identifikationsnummer, die einem Netzwerkgerät zugeordnet ist. Sie wird verwendet, um Datenpakete auf der Verbindungsschicht an das richtige Gerät zu leiten.

### **Routing**:

- Ebene: Netzwerkebene (Schicht 3)
- Beschreibung: Routing bezieht sich auf den Prozess, durch den Datenpakete durch ein Netzwerk geleitet werden, um ihr Ziel zu erreichen. Router arbeiten auf dieser Ebene, indem sie Routing-Tabellen verwenden, um zu entscheiden, über welchen Weg ein Paket weitergeleitet werden soll.

### **Switching**:

- Ebene: Verbindungsschicht (Schicht 2)
- Beschreibung: Switching bezieht sich auf den Prozess, durch den Datenpakete innerhalb eines lokalen Netzwerks (z. B. einem LAN) basierend auf den MAC-Adressen weitergeleitet werden. Switches arbeiten auf dieser Ebene.

### **ARP (Address Resolution Protocol)**:
    
- Ebene: Verbindungsschicht (Schicht 2)
- Beschreibung: ARP wird verwendet, um eine IP-Adresse (Schicht 3) in eine MAC-Adresse (Schicht 2) aufzulösen. Wenn ein Gerät den physischen Hardware-Adresse eines anderen Geräts in einem lokalen Netzwerk kennen muss, sendet es eine ARP-Anfrage, um diese Information zu erhalten.

