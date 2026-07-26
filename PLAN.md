# Projektplan: One-Pager für Weber-Wis

## Ziel

Unter `https://weber-wis.com` entsteht ein schneller, moderner und
mobiloptimierter One-Pager. Der Quellcode wird mit Git verwaltet, auf GitHub
gesichert und über GitHub Pages veröffentlicht.

Die bestehende Microsoft-365-E-Mail-Adresse
`a.weber@weber-wis.com` bleibt vollständig erhalten.

## Technischer Ansatz

- Statische Website aus HTML und CSS
- JavaScript nur dort, wo es einen echten Mehrwert bietet
- Versionsverwaltung mit Git
- Zentrales Repository auf GitHub
- Veröffentlichung über GitHub Pages
- Eigene Domain `weber-wis.com`
- HTTPS über GitHub Pages

Dieser Ansatz benötigt weder WordPress noch einen eigenen Webserver und hält
Einrichtung, Betrieb und Wartung überschaubar.

## Umsetzungsschritte

### 1. Inhalte und Gestaltung festlegen

- Angebot und Leistungen von Weber-Wis
- Zielgruppe
- Zentrales Nutzenversprechen
- Gewünschte Handlung der Besucher
- Logo, Farben, Bilder und gewünschter Stil
- Geschäftsanschrift und gesetzlich erforderliche Angaben

### 2. GitHub-Projekt einrichten

- Lokales Git-Repository initialisieren
- GitHub-Repository `onepager` erstellen
- Lokales Repository mit GitHub verbinden
- Ersten Projektstand übertragen

### 3. Seitenstruktur erstellen

Vorgesehene Abschnitte:

1. Startbereich mit klarem Nutzenversprechen
2. Leistungen
3. Vorteile oder Arbeitsweise
4. Über Weber-Wis
5. Kontakt
6. Impressum
7. Datenschutz

### 4. Kontakt integrieren

Die erste Version verwendet einen gut sichtbaren E-Mail-Link:

`a.weber@weber-wis.com`

Ein Kontaktformular kann später ergänzt werden. Da GitHub Pages ausschließlich
statische Inhalte ausliefert, benötigt ein Formular einen zusätzlichen
Formulardienst oder eine eigene serverseitige Verarbeitung.

### 5. Qualität prüfen

- Darstellung auf Smartphone, Tablet und Desktop
- Lesbarkeit und grundlegende Barrierefreiheit
- Ladezeit und Bildgrößen
- Funktion aller Links
- Seitentitel und Suchmaschinenbeschreibung
- Social-Media-Vorschaubild
- Impressum und Datenschutzerklärung

### 6. Vorschau veröffentlichen

- Website zu GitHub übertragen
- GitHub Pages aktivieren
- Website zunächst über die GitHub-Pages-Adresse prüfen

### 7. Domain verbinden

- `weber-wis.com` in GitHub Pages als eigene Domain eintragen
- Domain in GitHub verifizieren
- Apex-Domain über die erforderlichen A-Records mit GitHub Pages verbinden
- `www.weber-wis.com` über einen CNAME-Eintrag verbinden
- HTTPS aktivieren
- Weiterleitung zwischen Domain und `www` prüfen

### 8. Microsoft-365-Mail schützen

Bei der DNS-Konfiguration werden nur die Einträge für die Website ergänzt oder
angepasst. Folgende Microsoft-365-Einträge werden nicht entfernt oder
überschrieben:

- MX
- SPF/TXT
- Autodiscover/CNAME
- DKIM
- DMARC
- weitere Microsoft-Bestätigungs- und Serviceeinträge

### 9. Abschlussprüfung

- `https://weber-wis.com` erreichbar
- `https://www.weber-wis.com` erreichbar beziehungsweise korrekt umgeleitet
- HTTPS-Zertifikat gültig
- Mobilansicht geprüft
- Kontaktlink funktioniert
- E-Mail-Empfang unter `a.weber@weber-wis.com` funktioniert weiterhin

## Nächster konkreter Schritt

Für den ersten Entwurf werden die Leistungen, die Zielgruppe, ein kurzes
Nutzenversprechen, vorhandene Gestaltungselemente sowie die Pflichtangaben für
Impressum und Datenschutz benötigt.
