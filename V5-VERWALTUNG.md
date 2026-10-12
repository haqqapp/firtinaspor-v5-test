# Firtinaspor V5 – Spieler, Spiele und Training verwalten

Diese ZIP ist eine OFFLINE-TESTVERSION. Sie speichert ausschließlich im Browser-localStorage und ist NICHT die Supabase-Live-Version.

## Neu
- Positionen: `+ Spieler` (bereits vorhanden) und `Löschen` pro Spieler.
- Spielplan: `+ Spiel` (bereits vorhanden) und `Spiel löschen` pro Spiel.
- Training: `+ Termin` (bereits vorhanden) und `Training löschen` für den ausgewählten Termin.
- Löschaktionen fragen ausdrücklich nach Bestätigung.
- Löschen entfernt jeweils verknüpfte Statistiken und Bewertungen bzw. Anwesenheiten; Spielernamen werden auch aus der manuellen Aufstellung entfernt.
- Statt Spieler zu löschen, kann er weiterhin auf `inaktiv` gesetzt werden, damit seine Historie erhalten bleibt.

## Vorsicht
Endgültiges Löschen lässt sich nicht rückgängig machen. Vor Live-Übernahme bitte die Supabase-Datenbank sichern und die Änderungen zuerst im Testsystem prüfen. Eine Live-Integration ist in dieser ZIP noch nicht enthalten.

## Test
`npm install` und danach `npm run dev` im Projektordner. Die automatische Build-Prüfung in der Erstellungsumgebung konnte nicht abgeschlossen werden.
