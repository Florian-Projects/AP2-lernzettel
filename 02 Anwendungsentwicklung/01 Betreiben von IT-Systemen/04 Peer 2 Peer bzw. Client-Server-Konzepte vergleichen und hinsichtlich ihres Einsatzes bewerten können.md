
> [!cite] Inhalt
> 04 Peer 2 Peer bzw. Client-Server-Konzepte vergleichen und hinsichtlich ihres Einsatzes bewerten können
> - ﻿﻿Netzwerktopologie (FI DV/SI)
> - ﻿﻿Netzwerkplan

Die Begriffe „Peer-to-Peer“ (P2P) und „Client-Server“ beschreiben zwei grundlegende Modelle für die Kommunikation und den Datenaustausch innerhalb eines Netzwerks. Hier ein Vergleich der Konzepte und eine Bewertung ihres Einsatzes:

### Peer-to-Peer (P2P):

- **Konzept:** In einem P2P-Netzwerk agieren alle Computer als gleichberechtigte Teilnehmer. Jeder Computer (Peer) kann sowohl als Client als auch als Server fungieren.
- **Vorteile:**
  - Einfache Einrichtung und Konfiguration.
  - Kein zentraler Server notwendig, was Kosten und Verwaltungsaufwand reduziert.
  - Ausfallsicherheit, da der Ausfall eines Peers nicht das gesamte Netzwerk beeinträchtigt.
- **Nachteile:**
  - Skaliert schlechter mit zunehmender Anzahl von Peers, da jede Verbindung Ressourcen des einzelnen Peers beansprucht.
  - Schwieriger zu verwalten und zu sichern, da jeder Peer potenziell verwundbar ist und Angriffsfläche bietet.
  - Ineffiziente Nutzung der Bandbreite, da Daten direkt zwischen den Peers ausgetauscht werden.

- **Einsatzgebiete:**
  - Dateifreigabe und verteilte Systeme, bei denen Daten direkt zwischen Benutzern geteilt werden.
  - Kollaborative Arbeitsumgebungen und Anwendungen, bei denen kein zentraler Datenspeicher erforderlich ist.

### Client-Server:

- **Konzept:** Hier gibt es dedizierte Server, die Dienste und Ressourcen anbieten, und Clients, die diese Dienste und Ressourcen nutzen.
- **Vorteile:**
  - Bessere Skalierbarkeit und Verwaltung, besonders bei einer großen Anzahl von Clients.
  - Zentralisierte Sicherheitskontrollen und Datensicherung.
  - Optimierung von Ressourcen und Bandbreite durch zentralisierte Services.
- **Nachteile:**
  - Single Point of Failure: Wenn der Server ausfällt, sind die darauf basierenden Dienste nicht verfügbar.
  - Höhere Anschaffungs- und Wartungskosten für Server-Hardware und -Software.
  - Kann bei hohem Datenverkehr zu einem Engpass führen.

- **Einsatzgebiete:**
  - Unternehmensanwendungen, bei denen Datenintegrität, Sicherheit und zentrale Administration wichtig sind.
  - Web-Dienste und Anwendungen, bei denen ein Server viele Clients bedient.

### Netzwerktopologie (FI DV/SI):
In Bezug auf die Ausbildung zum Fachinformatiker Systemintegration (SI) oder Datenverarbeitung (DV) sind Kenntnisse über Netzwerktopologien entscheidend, um das geeignete Modell für die jeweilige Anforderung auswählen zu können.

### Netzwerkplan:

> [!important]
> Es scheint kein einheitliches Schema zu geben

Beim Entwerfen eines Netzwerkplans ist es wichtig, das angemessene Modell (P2P oder Client-Server) basierend auf den Anforderungen wie Kosten, Verwaltung, Skalierbarkeit und Sicherheit zu wählen. Der Netzwerkplan sollte sowohl die physische (Hardware, Kabel, etc.) als auch die logische Struktur (IP-Adressierung, Subnetze, etc.) des Netzwerks detailliert darstellen.

Die Wahl zwischen P2P und Client-Server hängt von den spezifischen Bedürfnissen der Organisation oder des Projekts ab. Kleinere Netzwerke oder solche mit begrenzten Ressourcen könnten von einem P2P-Modell profitieren, während größere oder sicherheitsbewusste Unternehmen wahrscheinlich ein Client-Server-Modell bevorzugen.