# Firtinaspor V11 – Testkandidat (kein Produktionsrelease)

## Umgesetzt
- Neue Formation 3-5-2 mit zwei Spitzen, drei Verteidigern und fünf Mittelfeldspielern.
- Spieler auf dem Spielfeld durch Ziehen mit Maus oder Finger verschieben. Kurz antippen öffnet die Alternativen.
- Positionskorrekturen werden je Spiel und Formation in der lokalen Testdatenspeicherung gesichert.
- Manuelle Spielerauswahl pro Spiel und Formation. Bereits bestehende V9-Vorgaben bleiben erhalten.
- PNG-Aufstellungsexport verwendet die angepassten Positionen.
- Gemeinsame optische Verbesserungen an Schrift, Formularen, Buttons und Feld.
- PWA-Cache-Version erhöht. Kein globaler Offline-Reset-Button.

## Einschränkungen
- Offline-Testversion: keine Supabase-Synchronisierung. NICHT als Live-App einsetzen.
- Vollständiger Vite-Build/Browsertest war hier nicht möglich (npm-Paketinstallation blockiert).
- React/JSX-Syntaxprüfung mit TypeScript-Parser war fehlerfrei.
- Dieses Paket ist kein umfassend getestetes Redesign aller App-Seiten; gezielte weitere UI-/Mobiltests sind erforderlich.
- Aufstellungsauswahl/Positionsverschiebung pro Spiel erfordert einen Praxistest auf iOS und Android.
- Der Export kann auf manchen Browsern als Download statt Share-Sheet erscheinen.

## Vor Live-Einsatz erforderlich
1. Aktuellen Supabase-Live-Code und Datenbank vollständig sichern (Excel ist kein vollständiger Datenbank-Backup).
2. Testprojekt und separate Testdaten verwenden.
3. `npm install` und `npm run build` erfolgreich ausführen, anschließend mobil alle sechs Formationen, manuelle Spielerwechsel und PNG-Export testen.
4. App-Oberflächen auf kleinen Bildschirmen prüfen; Spieler/Training/Spiele/Statistik inklusive vorhandener Daten und Löschbestätigungen durchtesten.
5. Änderungen in die aktuelle Supabase-Live-Version portieren, Realtime und Berechtigungen prüfen; zuerst Preview-Deployment und erst nach Freigabe Produktion.
