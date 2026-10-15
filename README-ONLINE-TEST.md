# Firtinaspor V11 – Supabase Online-Testkandidat

**Nicht direkt in die laufende Vercel-Live-App deployen.**

Dieser Quellcode verbindet den V11-Aufstellungseditor mit den Supabase Auth-/app_state-Mechanismen aus einem älteren V5-Live-Projektarchiv. Der aktuelle Produktionsstand konnte nicht bestätigt werden. Für die Nutzung mit dem Co-Trainer zunächst eine **separate Supabase-Testdatenbank oder isolierte Kopie** verwenden, keine Produktivdaten.

- Erwartete Umgebungsvariablen: `VITE_SUPABASE_URL`, `VITE_SUPABASE_ANON_KEY` (niemals Service-Role-Key im Frontend).
- Tabelle: `app_state`, Zeile `id = main`, JSONB-Datenfeld `data`.
- Die App erstellt bei leerem Datenstand **keine** Testdaten automatisch.
- Vor einer Verbindung zur Produktivdatenbank: aktuelle vollständige Sicherung durch Supabase Dashboard/DB-Backup durchführen. Zusätzlich app_state.data exportieren.
- Nur nach erfolgreichen Build-, Browser-, iPhone-/Android- und Zwei-Trainer-Tests sowie Abgleich mit dem **aktuellen** Produktionsrepository freigeben.
- Die Anwesenheit einer Realtime-Verbindung beweist nicht, dass Konflikte und konkurrierende Änderungen in allen Fällen erfolgreich synchronisiert werden. Gleichzeitige Bearbeitung gesondert testen.
- Eine erfolgreiche App-Kompilierung allein ist **keine** Freigabe für den Livegang.
