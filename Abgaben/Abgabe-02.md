# Blatt 02: Git Branches, JUnit Basics; CI-Pipeline

## Aufgaben

### Git-Spiel

1. Shopkeeper in Master verändert. Danach habe ich die changes commited und end in master gemerged. Es hat ohne Konflikte funktioniert
2. Diesmal habe ich stats in der stats.md verändert und diese commited. Beim Mergen von end in master kamm es dann zu keinem konflikten, da die Änderungen an unterschiedlichen Stellen waren.
3. Im Unterschied zu 2 kann git hier nicht automatisch mergen, da eine Datei in beiden Branches an derselben Stelle verändert wurde. Die Konflikte musste ich Manuel mit Nano lösen, bevor ich erneut commiten konnte
4. Dadurch das ich erst gerebased habe wurden dabei schon die Konflikte beseitigt, weshalb das Mergen danach reibungslos ablief.

### Katzen-Café
Link zu meier Fork: https://github.com/Marva919/Marvin_prog2_ybel_catcafe

Diskussion  zu JUnit:
1. Die Testfälle sind relevant, weil sie die wichtigsten Funktionen des Programms überprüfen. Dabei wird getestet, ob Katzen korrekt hinzugefügt, gezählt und gesucht werden können und wie das Programm auf ungültige Eingaben reagiert. 
2. Die Testfälle sind unterschiedlich, weil sie verschiedene Situationen abdecken. Manche testen normale Abläufe, andere Fehlerfälle oder Sonderfälle wie leere Listen, doppelte Namen oder ungültige Gewichtsbereiche.