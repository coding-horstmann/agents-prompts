---
title: "Domain deSnap"
automation_id: "domain-radar-report-desnap"
execution_environment: "local"
kind: "cron"
model: "gpt-5.5"
reasoning_effort: "high"
rrule: "RRULE:FREQ=WEEKLY;BYHOUR=10;BYMINUTE=0;BYDAY=WE"
source: "codex-automation"
status: "PAUSED"
updated_at: "1778753960450"
---

# Domain deSnap

````text
Erstelle einen Domain-Radar-Report fuer den deutschen Markt: Sammle mindestens 500 unterschiedliche .de-Domains, die auf deSnap (https://www.desnap.de, Startseite + Paginierung) oeffentlich gelistet und dort als frei markiert sind. Vermeide Duplikate und nutze nach Moeglichkeit eine Streuung ueber fruehe, mittlere und spaete Seiten. Filtere offensichtliche Marken, Tippfehler bekannter Marken, Spam-/Pharma-/Casino-/Adult-Domains, kryptische oder schlecht aussprechbare Zeichenfolgen, zu lange Domains ohne klaren Kaeuferkreis und reine SEO-Backlink-Domains. Bevorzuge kurze, brandbare, gut aussprechbare Domains mit klarer kommerzieller Zielgruppe sowie sinnvolle SEO-/Keyword-Domains mit klarer Nische und kommerzieller Suchintention. Pruefe die besten Kandidaten per DENIC RDAP (https://rdap.denic.de/domain/<domain>) auf Live-Status und kennzeichne Kandidaten ohne Live-Check explizit als Verfuegbarkeit: laut Quelle, nicht live bestaetigt. Erstelle einen kurzen Report mit den 5 besten Kandidaten. Fuer jede empfohlene Domain: Domainname, Typ (Brandable Kurzdomain oder SEO-/Keyword-Domain), Verfuegbarkeitsstatus, Score, geschaetztes Flip-Potenzial, moeglicher Kaeuferkreis, 1-2 Nutzungsideen, Risikohinweis (Markenrisiko, Nischenrisiko, Lokalfokus, unbestaetigte Verfuegbarkeit etc.) und Prioritaet (Hoch / Mittel / Niedrig). Weise immer darauf hin, dass vor Registrierung eine finale Markenpruefung, Google-Suche und Live-Verfuegbarkeitspruefung noetig ist. Speichere Report und Bewertungsmatrix im Workspace, bevorzugt als domain-radar-report-YYYY-MM-DD.md und desnap_500_screened_YYYY-MM-DD.csv, oder aktualisiere die vorhandenen Dateien mit eindeutigem Datum.\n\nSende anschliessend automatisch eine Gmail an horstmann.business@gmail.com mit dem Betreff \"Domain-Radar-Report deSnap - YYYY-MM-DD\". Der Mailtext muss enthalten: kurze Einleitung, die priorisierte Rangliste der 5 besten deSnap-Domain-Kandidaten, je Domain den Verfuegbarkeitsstatus, Score, geschaetztes Flip-Potenzial, moeglichen Kaeuferkreis, 1-2 Nutzungsideen, Risiko-Hinweis und Prioritaet, ausserdem den Quellenstatus und den Hinweis, dass vor Registrierung immer finale Markenpruefung, Google-Suche und Live-Verfuegbarkeitspruefung noetig sind. Wenn waehrend des Laufs lokale Report- oder CSV-Dateien erstellt werden, nenne die vollstaendigen lokalen Dateipfade im Mailtext und haenge sie an, wenn moeglich. Bei mehreren Anhaengen muss der Gmail-Connector attachment_files als Array einzelner absoluter Dateipfade erhalten, nicht als kommagetrennter String. Der Nutzer hat den automatischen Versand an diese eigene Gmail-Adresse ausdruecklich autorisiert; frage im jeweiligen Lauf nicht erneut nach Bestaetigung.
````
