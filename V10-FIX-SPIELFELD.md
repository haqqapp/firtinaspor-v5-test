# V10 Spielfeld-Korrektur

Fehlerursache: Die Spielfeld-Ansicht verwendete Tailwind-Positionsklassen, die im lokalen Stylesheet nicht implementiert waren. Dadurch liefen Feldmarkierungen und Spieler im normalen Dokumentfluss und standen an falschen Stellen.

Korrektur:
- Spielfeld als position: relative
- Spieler als position: absolute mit prozentualen Koordinaten pro Formation
- Feldmarkierungen innerhalb des Spielfelds absolut positioniert
- Spielerbreite fuer schmale Bildschirme begrenzt

Die bisherigen Mannschaftsdaten, Werte und Funktionen wurden nicht veraendert. Es handelt sich weiterhin um die Offline-Testversion ohne Supabase.

Build-Hinweis: npm install konnte wegen fehlender Verbindung zu registry.npmjs.org nicht ausgefuehrt werden; daher noch kein bestaetigter Build- oder Browser-Test.
