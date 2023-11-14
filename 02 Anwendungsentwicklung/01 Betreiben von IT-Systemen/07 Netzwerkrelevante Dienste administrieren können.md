
> [!cite] Inhalt
> 
> 07 Netzwerkrelevante Dienste administrieren können
> 
> - ﻿﻿DNS
> - ﻿﻿DHCP
> - ﻿﻿Proxy


### 1. DNS (Domain Name System)

**Funktion:**
- Übersetzt benutzerfreundliche Domänennamen (z.B. `www.example.com`) in IP-Adressen (z.B. `192.0.2.1`), die Computer verwenden, um sich im Internet oder im internen Netzwerk zu identifizieren und zu lokalisieren.

**Administration:**
- Einrichtung und Pflege von DNS-Servern, die Anfragen bearbeiten.
- Konfiguration von Zonen, Datensätzen (wie A, AAAA, CNAME, MX, PTR) und Forward/Reverse Lookups.
	- A = IPv4
	- AAAA = IPv6
	- PTR ist für reverse Lookups also IP zu Domain
- Sicherstellung der korrekten DNS-Auflösung und Redundanz durch Sekundärserver oder DNS-Cluster.
- Implementierung von Sicherheitsmaßnahmen wie DNSSEC, um die Integrität der DNS-Antworten zu gewährleisten.
	- Die **Domain Name System Security Extensions** (**DNSSEC**) sind eine Reihe von [Internetstandards](https://de.wikipedia.org/wiki/Internetstandard "Internetstandard"), die das [Domain Name System](https://de.wikipedia.org/wiki/Domain_Name_System "Domain Name System") (DNS) um Sicherheitsmechanismen zur Gewährleistung der [Authentizität](https://de.wikipedia.org/wiki/Authentizit%C3%A4t "Authentizität") und [Integrität](https://de.wikipedia.org/wiki/Integrit%C3%A4t_(Informationssicherheit) "Integrität (Informationssicherheit)") der Daten erweitern

### 2. DHCP (Dynamic Host Configuration Protocol)

**Funktion:**
- Automatisiert die Zuweisung von IP-Adressen, Subnetzmasken, Gateways und weiteren Netzwerkinformationen an Clients im Netzwerk.

**Administration:**
- Einrichtung und Konfiguration von DHCP-Servern.
- Definieren von IP-Adresspools und Leasing-Parametern.
	- Mit Leasing ist das herausgeben von IPs gemeint
- Verwaltung von Reservierungen für Geräte, die feste IP-Adressen benötigen.
- Überwachung von Leasing-Zuweisungen und Adressverbrauch.
- Sicherstellen der Verfügbarkeit durch Failover-Konfigurationen oder Hochverfügbarkeitslösungen.

### 3. Proxy-Server

**Funktion:**
- Handelt als Vermittler für Anfragen von Clients, die Ressourcen von anderen Servern suchen. Kann für die Zwischenspeicherung (Caching), Zugriffskontrolle und Filterung verwendet werden.

**Administration:**
- Einrichtung und Konfiguration des Proxy-Servers und entsprechender Software.
- Konfiguration von Zugriffsregeln und -berechtigungen.
- Einrichtung von Caching-Richtlinien zur Verbesserung der Netzwerkperformance.
- Überwachung und Analyse des Datenverkehrs, um Nutzungsmuster zu verstehen und Sicherheitsverletzungen zu erkennen.
- Implementierung von Benutzerauthentifizierungs- und Protokollierungsfunktionen.

**Sicherheitsaspekte:**
- Überwachung auf Anomalien oder Missbrauch.
- Aktualisierung von Software und Patch-Management, um Sicherheitslücken zu schließen.
- Konfiguration von Firewalls und Intrusion-Detection-Systemen in Verbindung mit dem Proxy.

