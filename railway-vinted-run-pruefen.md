---
title: "Railway Vinted Run prüfen"
automation_id: "railway-vinted-run-pr-fen"
kind: "heartbeat"
rrule: "FREQ=DAILY;BYHOUR=8;BYMINUTE=45;BYSECOND=0"
source: "codex-automation"
status: "ACTIVE"
updated_at: "1779113885681"
---

# Railway Vinted Run prüfen

````text
Prüfe gezielt, ob der Railway-Service `vinted-worker` für das Projekt `ebayamz` seit dem letzten geplanten Lauf erfolgreich gelaufen ist. Beachte: Vinted wartet inzwischen auf einen laufenden eBay-Run, damit keine Parallel-Scans stattfinden. Nutze Railway, falls verfügbar, und zusätzlich Supabase-Projekt `vmtryawhjcjbaujfzqmt`: kontrolliere die letzten `vinted_runs`, insbesondere Status, scanned/searches/hits/deals/errors, Start-/Endzeit, Warte-/Abbruchhinweise in error_messages und ob neue Produkte `vinted_last_checked` erhalten haben. Melde knapp: gelaufen ja/nein oder wartet noch, Ergebniszahlen, auffällige Fehler oder Rate-Limits, ob der eBay/Vinted-Overlap sauber vermieden wurde, und ob `VINTED_SCAN_LIMIT=400` sinnvoll/stabil wirkt. Zukunftsnotiz nur als Beobachtung, nicht automatisch umsetzen: Einschätzen, ob die aktuelle Kopplung Keepa -> eBay-Run weiterhin stört und ob ein separater Keepa-Pool-Run sinnvoll wäre, der Amazon/Keepa-Daten unabhängig aktualisiert, während eBay und Vinted nur aus diesem Pool lesen. Wenn Railway-Zugriff fehlt, sage das klar und stütze dich auf Supabase.
````
