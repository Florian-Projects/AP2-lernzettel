
> [!cite] Inhalt
> 06 Standortübergreifende und -unabhängige Kommunikation situationsgerecht auswählen und einrichten können
> 
> - ﻿﻿VPN-Modelle
> - ﻿﻿Tunneling
> - ﻿﻿IPsec

Die standortübergreifende und -unabhängige Kommunikation ist ein wesentlicher Bestandteil moderner Netzwerke, vor allem für Unternehmen mit mehreren Standorten oder mobilen Mitarbeitern. Um eine sichere und effiziente Kommunikation zu gewährleisten, werden Technologien wie VPNs (Virtual Private Networks), Tunneling-Protokolle und IPsec eingesetzt. Hier ist ein Überblick über diese Technologien und wie man sie situationsgerecht auswählt und einrichtet:

### VPN-Modelle

**Site-to-Site VPN:**
- Verbindet zwei Standorte über das Internet, indem ein virtuelles Tunnel von einem VPN-Gateway zum anderen erstellt wird.
- Ideal für feste Standortverbindungen, um Netzwerke in verschiedenen geografischen Standorten zu einem einzigen Netzwerk zu verbinden.
- Kann mit statischen Routen oder Routing-Protokollen wie BGP oder OSPF konfiguriert werden.

**Remote-Access VPN:**
- Ermöglicht einzelnen Benutzern den Zugriff auf ein Unternehmensnetzwerk über das Internet.
- Benutzer verwenden VPN-Client-Software, um eine sichere Verbindung zum VPN-Gateway des Unternehmens herzustellen.
- Geeignet für Home-Office-Mitarbeiter oder Mitarbeiter auf Reisen.

**Mobile VPN:**
- Speziell für die Anforderungen von mobilen Benutzern mit ständig wechselnden Netzwerkverbindungen entwickelt.
- Hält die Verbindung beständig, selbst wenn der Netzwerkzugangspunkt, IP-Adresse oder das Gerät wechselt.

### Tunneling

Tunneling ist der Prozess der Verkapselung eines Protokolls oder einer Payload in einem anderen Protokoll, so dass Daten sicher über ein unsicheres Netzwerk, wie das Internet, übertragen werden können. Ein VPN verwendet Tunneling-Protokolle, um private Daten zu übertragen.

**Beispiele für Tunneling-Protokolle:**

- **PPTP (Point-to-Point Tunneling Protocol):** Eines der ältesten VPN-Protokolle, heute aufgrund von Sicherheitsbedenken weniger empfohlen.
- **L2TP (Layer 2 Tunneling Protocol):** Oft in Verbindung mit IPsec verwendet, bietet selbst keine Verschlüsselung, sondern schafft den Tunnel.
- **SSL/TLS:** Wird für sichere Webtransaktionen verwendet und ist die Basis für das VPN-Modell, das als SSL-VPN bekannt ist.
- **OpenVPN:** Ein robustes Open-Source-VPN-Protokoll, das sowohl für Site-to-Site- als auch für Remote-Access-VPN eingesetzt werden kann.

### IPsec

IPsec (Internet Protocol Security) ist ein Set von Protokollen, das Sicherheitsdienste für IP-Kommunikation durch Authentifizierungs- und Verschlüsselungsmechanismen bietet

https://www.elektronik-kompendium.de/sites/net/0906191.htmo

IPsec ist eine Erweiterung des Internet-Protokolls (IP) um Verschlüsselungs- und Authentifizierungsmechanismen. Damit erhält das Internet-Protokoll die Fähigkeit IP-Pakete kryptografisch gesichert über öffentliche und unsichere Netze zu transportieren. IPsec wurde von der Internet Engineering Task Force (IETF) als integraler Bestandteil von IPv6 entwickelt. Weil das Internet-Protokoll der Version 4 ursprünglich keine Sicherheitsmechanismen hatte, wurde IPsec für IPv4 nachträglich spezifiziert.

#### Bestandteile von IPsec-VPNs

- Interoperalitität
- kyptografischer Schutz der übertragenen Daten
- Zugangskontrolle
- Datenintegrität
- Authentisierung des Absenders (Benutzerauthentisierung)
- Verschlüsselung
- Authentifizierung von Schlüsseln
- Verwaltung von Schlüsseln (Schlüsselmanagement)

Hinter diesen Bestandteilen stehen Verfahren, die miteinander kombiniert eine zuverlässige Sicherheit für die Datenübertragung über öffentliche Netze bieten. VPN-Sicherheitslösungen mit hohen Sicherheitsanforderungen setzen generell auf IPsec.

### Einsatz-Szenarien

- Site-to-Site-VPN / LAN-to-LAN-VPN / Gateway-to-Gateway-VPN
- End-to-Site-VPN / Host-to-Gateway-VPN / Remote-Access-VPN
- End-to-End-VPN / Host-to-Host-VPN / Remote-Desktop-VPN / Peer-to-Peer-VPN