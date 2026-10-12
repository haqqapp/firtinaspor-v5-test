# V7 Offline-Test – Änderungen

- Fussball.de: direkter Link exakt mit `#!/`.
- Spielplan-Filter: Alle Spiele (inkl. Freundschaft) oder Nur Liga.
- Liga-Saisonstatistik und Torjägerliste schließen Freundschaftsspiele aus.
- Spielerprofile, Formkurven, Score, Minutenkennzahlen und die Spielerbewertung beziehen sich nur auf Ligaspiele. Freundschaftsspiele bleiben mit Ergebnissen, Minuten und Toren weiterhin im Spielplan dokumentierbar, werden jedoch nicht für die Bewertung angeboten.
- Bereits vorhandene Daten bleiben gespeichert. Ältere Spiele lassen sich bearbeiten (Gegner, Datum, Uhrzeit, Wettbewerb, Heim/Auswärts, Ergebnisse, Tore, Assists und Minuten).
- Trainingstage können nachträglich im Datum bearbeitet werden; Anwesenheiten lassen sich weiterhin ändern.
- Reset-Knopf bleibt entfernt.

**Hinweis:** Diese ZIP ist eine getrennte Offline-Testversion. GitHub/Vercel-Testprojekt verwenden, nicht die Supabase-Live-App überschreiben. Bei lokal gespeicherten Daten vor dem Test eine Sicherung machen. Bestehende lokale Daten haben Vorrang vor eingebauten Startdaten.
