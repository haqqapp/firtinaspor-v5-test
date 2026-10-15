# V9 Aufstellungsassistent – Offline-Test

- Formation direkt im Bereich „Aufstellung“ wählen. Die App optimiert die Startelf für jede Formation über Positionsstärke, Score, Form und Momentum.
- Spieler auf dem Spielfeld antippen: Alternativen werden nach positionsbezogenem Empfehlungswert sortiert. Die App zeigt Positionsstärke, Gesamt-Score, Trainingsquote, Form der letzten fünf Spiele und den Vergleich zum aktuellen Spieler.
- Alternative antippen: manueller Slot wird gespeichert. Markierte Spieler behalten Vorrang; dieselbe Person wird nicht zweimal aufgestellt.
- 11 Startelf, 5 Bankspieler und 17. Reserve bleiben erhalten. Der Offline-Reset-Knopf bleibt entfernt.
- Die eingebauten Testdaten werden nicht bei jedem Deployment über vorhandene lokale Daten geschrieben. Bei vorhandenen Browserdaten kann daher ein älterer Teststand angezeigt werden.
- Nicht mit der Supabase-Live-Version verwechseln. Kein produktiver Build-Test möglich: npm-Paketserver in der Testumgebung nicht erreichbar.
