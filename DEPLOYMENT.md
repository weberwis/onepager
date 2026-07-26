# Veröffentlichung und DNS

Stand: 26. Juli 2026

## Öffentliche Vorschau

GitHub Pages ist aktiv:

- Basis: `https://weberwis.github.io/onepager/`
- Deutsch: `https://weberwis.github.io/onepager/de/`
- Englisch: `https://weberwis.github.io/onepager/en/`

Der Build des Commits `1d971ae` wurde erfolgreich abgeschlossen. Alle drei
Adressen liefern HTTP 200.

## Aktueller DNS-Status

Vor der Domainumstellung wurden folgende Einträge ermittelt:

- `weber-wis.com` besitzt noch keinen A-Record für eine Website.
- `www.weber-wis.com` besitzt noch keinen CNAME.
- Microsoft-365-MX:
  `weberwis-com01c.mail.protection.outlook.com`
- SPF:
  `v=spf1 include:spf.protection.outlook.com -all`
- Autodiscover:
  `autodiscover.outlook.com`
- MTA-STS-Ankündigung:
  `v=STSv1; id=2026072601`
- `mta-sts.weber-wis.com` besitzt noch kein Webziel.

## DNS-Einträge für die Hauptwebsite

Beim DNS-Anbieter sind für die Apex-Domain vier A-Records einzutragen:

| Typ | Name | Wert |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |

Zusätzlich:

| Typ | Name | Wert |
|---|---|---|
| CNAME | `www` | `weberwis.github.io` |

Erst nachdem diese Einträge gespeichert sind:

1. in GitHub unter **Settings → Pages** `weber-wis.com` als Custom Domain
   eintragen;
2. DNS-Prüfung abwarten;
3. **Enforce HTTPS** aktivieren;
4. `weber-wis.com`, `www.weber-wis.com`, `/de/` und `/en/` testen.

Die Custom Domain wird noch nicht vorab in GitHub gesetzt, weil GitHub die
funktionierende Vorschau sonst auf eine derzeit nicht auflösbare Domain
umleiten könnte.

## Microsoft-365-Einträge nicht verändern

Folgende vorhandene Einträge bleiben unverändert:

- MX für `weberwis-com01c.mail.protection.outlook.com`
- SPF/TXT
- Microsoft-Domainbestätigung
- Autodiscover/CNAME
- vorhandene DKIM- und DMARC-Einträge
- `_mta-sts`-TXT

## MTA-STS

Die angekündigte MTA-STS-Richtlinie benötigt einen separaten HTTPS-Host:

`https://mta-sts.weber-wis.com/.well-known/mta-sts.txt`

Die Quelldatei liegt im Repository unter:

`mta-sts-policy/.well-known/mta-sts.txt`

Der konfigurierte MX
`weberwis-com01c.mail.protection.outlook.com` passt zum vorgesehenen Muster
`*.mail.protection.outlook.com`.

Noch erforderlich:

1. separate statische Veröffentlichung für die MTA-STS-Datei bereitstellen;
2. `mta-sts.weber-wis.com` per CNAME mit diesem Host verbinden;
3. gültiges HTTPS ohne Zertifikatsfehler sicherstellen;
4. Abruf der Richtlinie unter dem exakten Pfad testen;
5. anschließend die Versions-ID des `_mta-sts`-TXT-Eintrags erhöhen.

Da `_mta-sts.weber-wis.com` den Standard bereits ankündigt, sollte dieser
separate Host zeitnah eingerichtet werden.

## Rechtliche Freigabe

Impressum und Datenschutzerklärung sind als veröffentlichungsfähige Entwürfe
implementiert. Vor der endgültigen Freischaltung von `weber-wis.com` sollen
insbesondere Unternehmensform, Pflichtangaben und die Datenschutzerklärung
fachlich beziehungsweise rechtlich geprüft werden.
