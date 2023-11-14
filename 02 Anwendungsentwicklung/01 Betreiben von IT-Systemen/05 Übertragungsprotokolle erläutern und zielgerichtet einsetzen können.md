
> [!cite] Inhalt
> 05 Übertragungsprotokolle erläutern und zielgerichtet einsetzen können.
> 
> - ﻿﻿TCP/UDP
> - ﻿﻿HTTPS

### TCP/UDP

TCP (Transmission Control Protocol) und UDP (User Datagram Protocol) sind zwei Kernprotokolle der Transportschicht im Internetprotokoll-Stack. Sie sind für den Versand von Datenpaketen von einem Host zum anderen zuständig, unterscheiden sich jedoch in ihrer Funktionsweise und ihren Einsatzgebieten.

**TCP:**
- **Verbindungsorientiert:** TCP stellt eine zuverlässige Verbindung zwischen Client und Server her, bevor Daten übertragen werden.
- **Zuverlässigkeit:** Es garantiert die Integrität der Datenübertragung durch Bestätigungsmechanismen und Neuübertragung verlorener oder beschädigter Pakete.
- **Kontrolle der Übertragungsqualität:** TCP verwendet Flusskontrolle und Staukontrolle, um die Datenübertragung an die Netzwerkbedingungen anzupassen.
- **Reihenfolge:** TCP sorgt dafür, dass die Pakete in der richtigen Reihenfolge beim Empfänger ankommen.

**UDP:**
- **Verbindungslos:** UDP sendet Daten, ohne vorher eine Verbindung aufzubauen, und ohne zu garantieren, dass sie ankommen.
- **Schnelligkeit:** Es gibt keine Überlastkontrolle, was es schneller macht, da der Overhead durch Bestätigungen entfällt.
- **Eingeschränkte Integrität:** UDP hat einen sehr einfachen Fehlerprüfungsmechanismus und korrigiert oder wiederholt keine verlorenen Pakete.
- **Flexibilität:** Es eignet sich für Anwendungen, bei denen es auf Geschwindigkeit ankommt und gelegentliche Fehler tolerierbar sind, wie z.B. bei Live-Video- oder Audio-Streams.

**Zielgerichteter Einsatz:**
- TCP wird in Anwendungen eingesetzt, bei denen Zuverlässigkeit und Reihenfolge der Daten entscheidend sind, wie z.B. Webseitenabruf (HTTP/HTTPS), Dateiübertragung (FTP) und E-Mail (SMTP, POP3, IMAP).
- UDP wird für Dienste verwendet, bei denen Geschwindigkeit wichtiger ist als Zuverlässigkeit, wie z.B. Streaming-Dienste (Video, Audio), Online-Spiele und VoIP (Voice over IP).

### HTTP

HTTP (Hypertext Transfer Protocol) ist ein Protokoll der Anwendungsschicht, das als Grundlage für die Datenkommunikation im World Wide Web dient. Es ermöglicht die Übertragung von Hypermedia-Dokumenten, wie zum Beispiel HTML. Es ist das Protokoll, das verwendet wird, um Seiten von einem Webserver zu einem Browser zu laden, sowie um Daten von einem Browser an einen Webserver zu senden, beispielsweise beim Ausfüllen eines Formulars.

**Grundfunktionen von HTTP:**

- **Stateless Protocol:** HTTP ist ein zustandsloses Protokoll, was bedeutet, dass jeder Befehl unabhängig von anderen Befehlen ausgeführt wird. Jedoch können HTTP-Cookies verwendet werden, um den Zustand und die Benutzersitzungen zu speichern.
- **Client-Server-Modell:** In einer typischen HTTP-Transaktion sendet ein Webbrowser (der Client) eine HTTP-Anforderung an den Webserver, auf dem die angeforderte Webseite gehostet wird. Der Server antwortet dann mit einer HTTP-Antwort.
- **Methoden:** HTTP definiert eine Reihe von Anforderungsmethoden, um die gewünschte Aktion des Servers anzugeben. Die am häufigsten verwendeten Methoden sind GET, um Ressourcen (wie Webseiten) abzurufen, und POST, um Daten zum Server zu senden, z. B. Formulardaten.
- **Statuscodes:** Jede HTTP-Antwort enthält einen Statuscode, der das Ergebnis der Anfrage angibt. Diese Codes sind in verschiedene Klassen eingeteilt, wie 2xx für Erfolg, 3xx für Umleitung, 4xx für Client-Fehler und 5xx für Server-Fehler.
- **Versionen:** HTTP/1.1 ist eine sehr verbreitete Version, die Verbindungs-Persistent bietet, wobei mehrere Anfragen über eine einzige TCP-Verbindung gesendet werden können. ~~HTTP/2 ist die neueste Version~~**Lüge: es gibt schon HTTP/3**, die die Leistung verbessert, indem es Features wie Stream-Priorisierung und Header-Kompression einführt.

### HTTPS

HTTPS (Hypertext Transfer Protocol Secure) ist eine Erweiterung des HTTP-Protokolls, das für die sichere Kommunikation über ein Computernetzwerk, insbesondere das Internet, verwendet wird. HTTPS verschlüsselt die Sitzung mit Transport Layer Security (TLS) oder, in älteren Anwendungen, mit Secure Sockets Layer (SSL), was die Sicherheit der Datenübertragung verbessert.

**Merkmale von HTTPS:**
- **Verschlüsselung:** Um die Sicherheit der Daten zu gewährleisten, werden diese zwischen dem Browser des Benutzers und dem Webserver verschlüsselt übertragen.
- **Authentifizierung:** HTTPS ermöglicht die Überprüfung der Identität der Gegenstelle mittels Zertifikaten, die von Zertifizierungsstellen ausgestellt werden.
- **Schutz vor Man-in-the-Middle-Angriffen:** Durch die Verschlüsselung und Authentifizierung wird es für Angreifer deutlich schwieriger, sich zwischen die Kommunikationspartner zu schalten und Daten auszuspähen oder zu manipulieren.

**Zielgerichteter Einsatz:**
- HTTPS wird vor allem für Transaktionen im Internet eingesetzt, bei denen Sicherheit und Datenschutz wichtig sind, wie z.B. Online-Banking, E-Commerce und jegliche Form der Datenerfassung, die sensible Informationen enthält.

Zusammenfassend ist die Wahl des Übertragungsprotokolls entscheidend für die Leistung und Sicherheit der Netzwerkkommunikation. Während TCP für zuverlässige Übertragungen genutzt wird, bietet UDP Vorteile bei Echtzeitanwendungen. HTTPS hingegen ist unverzichtbar für sichere Webanwendungen und den Schutz vertraulicher Daten.

