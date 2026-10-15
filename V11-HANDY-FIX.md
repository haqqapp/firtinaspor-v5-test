# V11 Handy-Fix – Spielerverschieben

- Verhindert einen Absturz, wenn React einen verzögerten Drag-Zustand nach Loslassen des Fingers verarbeitet.
- Der Spielerindex wird vor der asynchronen Statusaktualisierung festgehalten.
- Drag-Bewegungen werden auf maximal etwa 22 sichtbare Updates pro Sekunde begrenzt.
- Andere App-Daten und Speicher-Schlüssel bleiben unverändert.

Bitte zunächst im getrennten GitHub-/Vercel-Testprojekt prüfen. Ein tatsächlicher Mobilbrowser-Test steht noch aus.
