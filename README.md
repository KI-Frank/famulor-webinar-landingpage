# Famulor-Webinar – Landingpage (Vorlage für Famulor)

Entwurf von Frank Wilstermann zur Übernahme in das Famulor-Ökosystem. Die Vorschau zeigt Aufbau, Texte und Gestaltung der Anmeldeseite für das Webinar am **Donnerstag, 10. Dezember 2026, 18:00–19:30 Uhr** (Microsoft Teams). In dieser Fassung werden **keine Anmeldungen gespeichert** (Vorschau-Modus).

## Dateien
- `index.html` – die komplette Seite, Styles und Skript eingebettet, keine externen Dienste, keine Cookies
- `impressum.html`, `datenschutz.html` – Hinweise für die Vorschau; Famulor ergänzt die eigenen Texte
- `assets/` – Famulor-Logo (Brand-Kit, SVG) und Maskottchen (WebP)

## Aufbau der Seite
1. Kopfbereich: Badge mit Termin, Headline, Untertitel, Button „Jetzt kostenlos anmelden“, Kennzahlen, Webinar-Bonus, Terminkarte mit Countdown
2. Problem: drei Kacheln (verpasste Anrufe, abkühlende Leads, Standardanfragen)
3. Leistungen: sechs Karten
4. Agenda „Das nehmen Sie aus dem Webinar mit“: sechs Punkte (Milian live, Telefonie, Squad und Dolmetscher, alle Kanäle und KI-Avatar, Technik mit Browser Use, Preise und kostenloser Start)
5. Referent und Kennzahlen (+30 Mio. Anrufe, +3.000 Workspaces, 270+ Kunden)
6. Anmeldung mit Formular
7. FAQ (acht Fragen)

## Formular
- Felder: Vorname, Nachname, Firmen-E-Mail, Firma (optional), Einwilligung, unsichtbares Bot-Feld
- Freemail-Adressen (gmail, gmx, web.de, t-online, outlook …) werden abgelehnt, weil der Webinar-Bonus nur mit Firmen-E-Mail gilt
- Für den echten Betrieb in `index.html`: `DEMO_MODE = false` und `FORM_ENDPOINT` setzen. Gesendet wird dann JSON: `vorname, nachname, email, firma, einwilligung, quelle, seite, zeit`
- Nach der Anmeldung: Danke-Ansicht und Kalenderdatei (.ics, 10.12.2026, 18:00–19:30 Uhr)

## Webinar-Bonus
Auf der Seite steht nur der Hinweis: 800 Credits für rund 27 Gesprächsminuten für Teilnehmer, die noch keine Famulor-Kunden sind, bei Registrierung mit Firmen-E-Mail. Der Gutscheincode wird bewusst nur im Webinar genannt.

## Offen für die Übernahme
- Impressum und Datenschutz von Famulor
- Ziel für die Anmeldungen und Versand des Teams-Links per E-Mail
- Ob eine Aufzeichnung angeboten wird (FAQ verweist bisher auf „nach der Anmeldung“)
- Schrift: Die Seite nutzt Inter Tight, wenn installiert, sonst eine Systemschrift (bewusst ohne Google Fonts)

## Lokal ansehen
```
python -m http.server 8765
```
dann http://127.0.0.1:8765 öffnen.
