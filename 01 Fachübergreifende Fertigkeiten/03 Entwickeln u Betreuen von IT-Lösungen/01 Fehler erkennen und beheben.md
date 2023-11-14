
> [!cite] Inhalt
> - ﻿﻿Debugging, Break Point
> - ﻿﻿Software-Test, dynamische und statische Testver-fahren (z. B. Black Box, White Box, Review, Extrem-wertetest)
> - ﻿﻿Testdaten
> - ﻿﻿Komponententest, Funktionstest, Integrationstest
> - ﻿﻿Versionsmanagement des Quellcodes

1. **Debugging, Break Point:**
    
    - **Debugging (Fehlerbehebung)** ist der ==Prozess des Identifizierens und Behebens von Fehlern oder Problemen in einer Softwareanwendung==. Es beinhaltet das Nachverfolgen und Isolieren von Fehlern, um die Software zu verbessern.
    - Ein **Break Point** ist ein spezifischer ==Punkt im Quellcode, an dem der Debugger gestartet wird==, um den Zustand der Anwendung zu überprüfen. Der Debugger stoppt die Ausführung des Codes an diesem Punkt, sodass Entwickler den Zustand der Variablen und den Fluss des Programms überwachen können, um Fehler zu finden.
2. **Software-Test, dynamische und statische Testverfahren:**
    
    - **Software-Test** ist der Prozess, bei dem ==Software auf Fehler überprüft== wird, um sicherzustellen, dass sie wie erwartet funktioniert.
    - **Dynamische Tests** umfassen das ==Ausführen der Software== und das Überprüfen ihres Verhaltens. Beispiel: Das Ausführen einer Anwendung und Überprüfen, ob sie die erwarteten Ergebnisse liefert.
    - **Statische Tests** beinhalten die ==Überprüfung des Quellcodes oder der Dokumentation, ohne die Software auszuführen==. Beispiel: Code-Reviews oder die Überprüfung von Anforderungsdokumenten.

	1. **Black Box Testing (Schwarzkastentest):**
	    - Beim **Black Box Testing** wird die interne Struktur der Software nicht berücksichtigt. Stattdessen wird die Software als "Black Box" betrachtet, und ==Tests basieren auf den spezifizierten Ein- und Ausgabeparametern==. Die Tester kennen die innere Logik der Software nicht, sondern ==konzentrieren sich darauf, ob sie die erwarteten Ergebnisse liefert.==
	    - Beispiel: Ein Tester führt einen Black Box Test auf einer Website durch, indem er Eingaben wie Benutzername und Passwort eingibt und überprüft, ob die Anmeldung erfolgreich ist, ohne die genaue Implementierung der Anmeldefunktion zu kennen.
	2. **White Box Testing (Weißkastentest):**
	    
	    - **White Box Testing** beinhaltet das ==Testen der internen Struktur== und des Codes einer Softwareanwendung. Tester haben Kenntnisse über die Implementierung der Software und erstellen Tests, um sicherzustellen, dass der Code korrekt funktioniert.
	    - Beispiel: Ein Entwickler führt White Box Tests aus, um sicherzustellen, dass alle Pfade im Code abgedeckt sind und dass bestimmte Bedingungen (z. B. Schleifen oder Bedingungen) korrekt funktionieren.
	3. **Review (Überprüfung):**
	    
	    - Eine **Überprüfung** ist ein Prozess, bei dem der Quellcode, die Dokumentation oder andere Artefakte einer ==Software von anderen Teammitgliedern oder Experten überprüft werden==, um Fehler zu identifizieren, die Qualität zu verbessern und sicherzustellen, dass die Anforderungen erfüllt werden.
	    - Beispiel: Ein Team von Entwicklern führt eine Code-Review durch, bei der sie den Code eines Kollegen auf Fehler, Einhaltung von Codierungsstandards und Effizienz überprüfen. Die festgestellten Probleme werden behoben, bevor der Code in die Hauptentwicklungslinie integriert wird.
	4. **Extremwertetest:**
	    
	    - Der **Extremwertetest** ist eine Art von Softwaretest, bei dem die ==Software mit extremen oder ungewöhnlichen Eingabewerten oder -bedingungen getestet wird==. Das Ziel ist es, zu überprüfen, wie die Software in Extremsituationen reagiert und ob sie sich korrekt verhält.
	    - Beispiel: In einem Extremwertetest für eine Wetter-App könnte die Software mit extremen Werten wie -30 Grad Celsius für die Temperatur oder einem Sturm mit starkem Wind getestet werden, um sicherzustellen, dass sie in solchen ungewöhnlichen Situationen keine Fehler aufweist.
1. **Testdaten:**
    
    - **Testdaten** sind **Eingaben, die in Softwaretests verwendet werden**, um sicherzustellen, dass die Anwendung korrekt funktioniert. Diese Daten können sowohl gültige als auch ungültige Werte enthalten, um verschiedene Szenarien abzudecken und Fehler zu identifizieren.
4. **Komponententest, Funktionstest, Integrationstest:**
    
    - **Komponententest** ist der ==Test einzelner Softwarekomponenten, wie Funktionen== oder Module, um sicherzustellen, dass sie in Isolation korrekt funktionieren.
    - **Funktionstest** ==testet die gesamte Funktionalität einer Softwareanwendung==, um sicherzustellen, dass sie die Anforderungen erfüllt.
    - **Integrationstest** ==überprüft, wie die verschiedenen Komponenten== oder Module einer Anwendung ==miteinander interagieren==, um sicherzustellen, dass sie ordnungsgemäß zusammenarbeiten.
5. **Versionsmanagement des Quellcodes:**
    
    - **Versionsmanagement** ist der Prozess, bei dem ==Änderungen im Quellcode einer Software verfolgt, verwaltet und dokumentiert werden==. Dies ermöglicht es Entwicklern, verschiedene Versionen des Codes zu erstellen und Änderungen nachzuverfolgen.
    - Beispiele für Versionsverwaltungssysteme sind ==Git==, Subversion und Mercurial. Entwickler können Änderungen an Dateien dokumentieren, verschiedene Versionen verwalten und zwischen verschiedenen Versionen der Software wechseln, um Fehler zu beheben oder neue Funktionen hinzuzufügen.