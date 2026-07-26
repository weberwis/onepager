# Weber Industrial Services One-Pager

Zweisprachiger, statischer Unternehmensauftritt für
[weber-wis.com](https://weber-wis.com).

## Inhalt

- deutsche Website unter `/de/`
- englische Website unter `/en/`
- Impressum und Datenschutzhinweise in beiden Sprachen
- responsive Gestaltung ohne externe Schriftarten
- keine Cookies, Analyse- oder Marketingdienste
- Sitemap, strukturierte Unternehmensdaten und `hreflang`

## Lokale Vorschau

```powershell
python -m http.server 8000
```

Danach `http://localhost:8000/de/` oder `http://localhost:8000/en/`
aufrufen.

## Vertrauliche Unterlagen

Der Ordner `input/` enthält ausschließlich lokale Ausgangsmaterialien und wird
über `.gitignore` nicht veröffentlicht.

## Rechtliche Prüfung

Impressum und Datenschutz sind auf Basis der vorliegenden Angaben erstellt.
Unternehmensform, Pflichtangaben und Datenschutztext sollen vor der endgültigen
Domain-Freigabe fachlich beziehungsweise rechtlich geprüft werden.

## MTA-STS

Die Richtlinie unter `mta-sts-policy/` ist die Quelle für einen separaten Host
`mta-sts.weber-wis.com`. Sie darf erst nach Prüfung des aktiven
Microsoft-365-MX-Ziels im Modus `enforce` veröffentlicht werden.
