# Session-Übergabe

Stand: 26. Juli 2026

## Ziel

Für Weber Industrial Services wurde ein zweisprachiger One-Pager erstellt,
über GitHub Pages veröffentlicht und mit der Domain `weber-wis.com`
verbunden. Zusätzlich wurde MTA-STS für die Microsoft-365-Maildomain
eingerichtet.

## GitHub und lokales Git

- GitHub-Konto: `weberwis`
- Hauptrepository:
  `https://github.com/weberwis/onepager`
- MTA-STS-Repository:
  `https://github.com/weberwis/mta-sts`
- Hauptbranch: `main`
- SSH-Schlüssel:
  `%USERPROFILE%\.ssh\id_ed25519_laptopsshkey`
- Der SSH-Zugriff zu GitHub wurde erfolgreich getestet.
- Das One-Pager-Repository verwendet den Schlüssel über die lokale
  Repository-Konfiguration.
- GitHub CLI und Zugriffstoken sind aktiv. Tokenwerte werden nicht
  dokumentiert.

## One-Pager

Sprachen:

- Deutsch: `https://www.weber-wis.com/de/`
- Englisch: `https://www.weber-wis.com/en/`

GitHub-Pages-Vorschau:

- `https://weberwis.github.io/onepager/`

Umgesetzt:

- responsive statische Website
- deutsche und englische Fachtexte
- SVG-Wortbildmarke auf Basis der Visitenkarte
- Leistungen, Projekterfahrung, Arbeitsweise und Kontakt
- Impressum und Datenschutz in beiden Sprachen
- SEO-Metadaten, `hreflang`, Sitemap und strukturierte Daten
- keine Cookies, Tracker oder extern geladenen Schriftarten
- individuelle 404-Seite

Kontakt:

- E-Mail: `a.weber@weber-wis.com`
- Telefon: `+49 177 577 46 02`
- Standort: Ehringshausen, Deutschland

## Vertrauliche Unterlagen

Der lokale Ordner `input/` enthält:

- Lebenslauf
- Preisliste
- Visitenkartenbild
- Screenshot der E-Mail-Einstellung

Der Ordner ist über `.gitignore` ausgeschlossen und wurde nicht auf GitHub
veröffentlicht.

Nicht veröffentlicht wurden insbesondere:

- Bankverbindung
- Preise
- persönliche Referenzkontakte
- alte Outlook-Adresse
- vollständige Ausgangsdokumente

## Domain und DNS

GitHub Pages verwendet als Custom Domain:

`www.weber-wis.com`

Cloudflare verwaltet die DNS-Zone. Die Website-Einträge müssen für die direkte
GitHub-Pages-Verbindung auf **DNS only** stehen.

Website-DNS:

- `www` CNAME → `weberwis.github.io`
- Apex-A-Records:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`

Die Microsoft-365-Mail-Einträge dürfen nicht verändert werden.

## Microsoft 365

Geprüfte Einträge:

- MX:
  `weberwis-com01c.mail.protection.outlook.com`
- SPF:
  `v=spf1 include:spf.protection.outlook.com -all`
- Autodiscover:
  `autodiscover.outlook.com`
- Microsoft-Domainbestätigung ist vorhanden.
- `_mta-sts`-TXT war zuletzt:
  `v=STSv1; id=2026072601`

## MTA-STS

Öffentliches Repository:

`https://github.com/weberwis/mta-sts`

Aktiver Endpunkt:

`https://mta-sts.weber-wis.com/.well-known/mta-sts.txt`

Status:

- separater GitHub-Pages-Build erfolgreich
- Custom Domain aktiv
- TLS-Zertifikat genehmigt
- HTTPS erzwungen
- HTTP 200 geprüft
- Content-Type `text/plain`

Aktive Richtlinie:

```text
version: STSv1
mode: enforce
mx: *.mail.protection.outlook.com
max_age: 604800
```

Das MX-Ziel passt zum Richtlinienmuster.

Bei jeder künftigen Änderung der Richtlinie muss auch die ID des
`_mta-sts`-TXT-Eintrags erhöht werden.

## Wichtige Projektdateien

- `README.md` – Projektübersicht
- `PLAN.md` – fachliches und gestalterisches Konzept
- `DEPLOYMENT.md` – GitHub-Pages-, DNS- und MTA-STS-Status
- `SETUP_STATUS.md` – lokale Git-, GitHub- und SSH-Einrichtung
- `SESSION_HANDOFF.md` – diese Übergabe
- `de/` – deutsche Website
- `en/` – englische Website
- `assets/` – Logo, Styles und JavaScript
- `mta-sts-policy/` – lokale Referenz der MTA-STS-Richtlinie

## Rechtlicher Hinweis

Impressum und Datenschutzerklärung wurden auf Basis der vorliegenden Angaben
erstellt. Vor einer endgültigen geschäftlichen Freigabe sollten
Unternehmensform, Pflichtangaben und Datenschutztext fachlich beziehungsweise
rechtlich geprüft werden.

## Empfohlene nächste Prüfung

Nach Abschluss aller DNS- und Zertifikatsänderungen kontrollieren:

1. `https://www.weber-wis.com/de/`
2. `https://www.weber-wis.com/en/`
3. Weiterleitung von `https://weber-wis.com`
4. aktiviertes **Enforce HTTPS** im One-Pager-Repository
5. E-Mail-Empfang unter `a.weber@weber-wis.com`
6. MTA-STS-Endpunkt und `_mta-sts`-TXT-ID
