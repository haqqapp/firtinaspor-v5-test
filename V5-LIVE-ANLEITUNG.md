# Firtinaspor V5 Live – Test-/Deployment-Kandidat

Diese Version erweitert die hochgeladene **V4 Offline-Testversion** um Spieler-, Spiele- und Trainingslöschung und ersetzt den Offline-Speicher durch Supabase Auth + `app_state`/Realtime. Der Code ist nicht nachweislich identisch mit dem derzeit auf Vercel laufenden Stand. Daher vor Veröffentlichung **zuerst getrennt testen**.

## Vor dem Deploy
1. Eine vollständige Sicherung der Zeile `public.app_state` (id=`main`, JSON `data`) aus Supabase erstellen. Excel ist kein vollständiger Ersatz für ein JSON-Backup.
2. GitHub-Branch und **Vercel Preview Deployment** benutzen, nicht gleich `main`/Production überschreiben.
3. In der Preview zuerst **ein separates Supabase-Testprojekt mit Kopie des Zustands** einsetzen. Sonst würde auch eine Preview deine echten Live-Daten ändern.
4. Environment Variables `VITE_SUPABASE_URL` und `VITE_SUPABASE_ANON_KEY` konfigurieren (nur Publishable/anon, niemals Service Role).
5. `npm install` und `npm run build`; Preview mit Anmeldung, Hinzufügen, Löschen und einem zweiten Trainer testen.
6. Danach mit gesicherter Live-Datenbank zur Produktionsversion wechseln.

## Funktionen
- Spieler: Hinzufügen und endgültiges Löschen (inklusive Anwesenheit, Noten, Tore, Vorlagen, manueller Aufstellung). Deaktivierung ist vorzuziehen, wenn die Historie erhalten bleiben soll.
- Spiele: Hinzufügen und Löschen (inklusive spielbezogener Bewertungen/Berichte).
- Trainingstage: Hinzufügen und Löschen (inklusive Anwesenheiten).
- Bestätigungsdialoge bei Löschungen, Änderungsverlauf, Supabase-Auth und Realtime.

## Hinweise
- Bei fehlender `app_state`-Zeile wird **nicht** automatisch ein alter Startdatensatz geschrieben.
- Parallelkonflikte werden bei Speichern gemeldet; bei Konflikt Seite neu laden.
- Es gibt keine serverseitige Löschwiederherstellung – Backup aufbewahren.
