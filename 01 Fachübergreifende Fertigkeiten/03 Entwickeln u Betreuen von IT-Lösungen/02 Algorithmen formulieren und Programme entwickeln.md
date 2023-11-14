
## Beispiel Aufgaben

https://moodle.mm-bbs.de/moodle/course/view.php?id=2185

## Inhalt

> [!cite] Inhalt
> 02 Algorithmen formulieren und Programme entwickeln
> 
> - ﻿﻿Abbildung der Kontrollstrukturen mittels Strukto-gramm, PAP oder Pseudocode als didaktisches  
>     Hilfsmittel
> - ﻿﻿UML (Use Case, Klassendiagramm)
> - ﻿﻿Entwurf der Bildschirmausgabemasken (Software-ergonomie, Barrierefreiheit)

1. **Abbildung der Kontrollstrukturen mittels [[#Struktogramm]], [[#Programmablaufplan]] oder Pseudocode als didaktisches Hilfsmittel:**
    
    - Die Abbildung von Kontrollstrukturen mithilfe von Struktogrammen, Programmablaufplänen (PAP) oder Pseudocode ist eine Technik, um den Programmablauf visuell zu planen und zu dokumentieren.
       
    - Diese Techniken werden oft in der Programmierung und Softwareentwicklung verwendet, um den Entwicklern und anderen Teammitgliedern einen klaren Überblick über den Ablauf eines Programms zu geben.
    
    Beispiel: Ein Struktogramm kann verwendet werden, um den Ablauf eines Algorithmus zur Sortierung von Zahlen darzustellen. Es zeigt visuell, wie die Zahlen verglichen und verschoben werden, um sie in aufsteigender Reihenfolge anzuordnen.
    
2. **UML ([[#Use Case Diagramm]], [[#Klassendiagramm]]):**
    
    - UML (Unified Modeling Language) ist eine standardisierte Modellierungssprache, die in der Softwareentwicklung verwendet wird, um Software-Architekturen und -Designs darzustellen.
    - Ein **Use Case-Diagramm** wird verwendet, um die ==Interaktionen zwischen einem System und seinen Benutzern oder anderen Systemen zu visualisieren==. Es zeigt, wie verschiedene Akteure (Nutzer, Systeme) mit dem System interagieren.
    - Ein **Klassendiagramm** zeigt die ==Struktur einer Softwareanwendung== durch die Darstellung von Klassen, deren Eigenschaften und Methoden, sowie deren Beziehungen zueinander.
    
    Beispiel: In einem Klassendiagramm für ein E-Mail-Programm würden Klassen wie "E-Mail", "Benutzer" und "Anhang" dargestellt, zusammen mit ihren Attributen und Methoden, sowie den Beziehungen zwischen ihnen.
    
3. **Entwurf der Bildschirmausgabemasken (Software-Ergonomie, Barrierefreiheit):**
    
    - Der Entwurf der Bildschirmausgabemasken bezieht sich auf die Gestaltung der Benutzeroberfläche (UI) von Softwareanwendungen.
    - **Software-Ergonomie** bezieht sich auf die Gestaltung der Benutzeroberfläche, um sicherzustellen, dass sie ==benutzerfreundlich und effizient== ist. Dies umfasst Aspekte wie die Anordnung von Schaltflächen, die Farbgestaltung und die Platzierung von Elementen, um die Benutzererfahrung zu verbessern.
    - **Barrierefreiheit** zielt darauf ab, Software so zu gestalten, dass sie von Menschen mit verschiedenen Fähigkeiten und Bedürfnissen, einschließlich Menschen mit Behinderungen, leicht genutzt werden kann.
    
    Beispiel: Bei der Gestaltung einer Website für einen Online-Shop sollte darauf geachtet werden, dass die Schriftgröße ausreichend groß ist, damit Menschen mit Sehschwächen den Text leicht lesen können. Außerdem sollten alle Funktionen über Tastaturbefehle zugänglich sein, um die Barrierefreiheit sicherzustellen.

## Struktogramm

![[Pasted image 20231023054433.png]]

## Programmablaufplan

Erklärung mit Python: https://informatik.mygymer.ch/m25d/04-programmieren/05-struktur.html

![[Pasted image 20231023055151.png]]

![[Pasted image 20231023055419.png]]

### Unterprogramme

https://informatik.mygymer.ch/m25d/04-programmieren/05-struktur.html#unterprogramm

![[Pasted image 20231023055216.png]]

## Use Case Diagramm

![[Pasted image 20231023060035.png]]

### IHK Belegsatz

![[Anwendungsfalldiagramm.png]]
### Kurzes und bündiges Arbeitsblatt

![[ANPR_UML_Usecasediagramm.pdf]]

## Klassendiagramm

### Beziehungen

- **Assoziation**: Eine Assoziation ist eine Beziehung zwischen Klassen, die eine Verbindung zwischen ihnen darstellt, ohne die Lebensdauer der beteiligten Klassen zu beeinflussen.
	- z. B. Funktionsaufrufe
    
- **Aggregation**: Aggregation ist eine spezielle Form der Assoziation, bei der eine Klasse Teile einer anderen Klasse enthält, wobei die Teile unabhängig vom Ganzen existieren können.
	- Lebenszyklen sind unabhängig
		- z. B. Teile werden als Argument an Konstruktor übergeben
    
- **Komposition**: Bei der Komposition enthält eine Klasse Teile einer anderen Klasse, wobei die Teile direkt von der Hauptklasse abhängen, sodass sie zusammen erstellt und zerstört werden.
	- Die Hauptklasse kontrolliert den Lebenszyklus des Teils
		- z. B. Teil wird **innerhalb** des Konstruktors erstellt
	- Es darum wie es implementiert ist. Nicht ob das Teil außerhalb existieren **könnte**. Glaubt Maxi und Tristan zumindest

### Beispiele

![[Pasted image 20231023060148.png]]
![[Pasted image 20231023060436.png]]

### IHK Belegsatz

![[Klassendiagramm.png]]

