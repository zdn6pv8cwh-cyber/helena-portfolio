# Helena Söll – Portfolio Website

Kontext-Datei, damit Design-/Inhalts-Änderungen ohne Rückfragen konsistent umgesetzt werden.

## Seitenstruktur

- `index.html` – Startseite (Hero, About, Projekt-Übersicht)
- `projekt-fein-wuerzig.html` – Projektunterseite
- `projekt-kolonne-null.html` – Projektunterseite (⚠️ enthält 17 base64-eingebettete Bilder, Datei ist dadurch ~7,4 MB statt wenige KB – sollte irgendwann auf externe Dateien in `/images` umgestellt werden, spart massiv Ladezeit & Bearbeitungsaufwand)
- `projekt-nivea-men.html` – Projektunterseite
- `projekt-research-innovation.html` – Projektunterseite
- `impressum.html` – Impressum
- `portfolio-mockup.html` – vermutlich Entwurf/unbenutzt, vor Änderungen kurz klären ob noch relevant
- `/images` – Bildassets (1,9 MB)
- `/fonts` – Playfair Display, Inter (Regular/Medium/Bold), lokal eingebunden als woff2

## Design-Tokens (aus index.html, gelten projektweit)

Farben (CSS-Variablen):
- `--paper: #F3ECDC` (Hintergrund, warmes Off-White)
- `--ink: #000000` (Haupttext/Kontrast)
- `--ink-soft: #000000` (aktuell identisch zu ink, evtl. für spätere Abstufung gedacht)
- `--blue: #86A9C4`
- `--coral: #E38A5C`
- `--pink: #E9A8C4`
- `--rule: #DBD0B6` (Trennlinien, Borders)

Typografie:
- Headlines/Akzente: `Playfair Display` (italic, serif) – edler, redaktioneller Ton
- Fließtext/UI: `Inter` (Regular/Medium/Bold) – klar, modern
- Durchgängig `letter-spacing: 0.03–0.04em`, viel Uppercase bei Labels/Nav/CTA
- Kein `border-radius` (0) – kantiges, striktes Layout

Stilrichtung: reduziert, editorial, viel Weißraum, dezente Hover-Transitions (font-weight/transform), keine verspielten Effekte.

## Workflow für Änderungen

1. Änderung wird direkt in der jeweiligen HTML-Datei umgesetzt (nur die betroffene Seite/Sektion, kein Rewrite ganzer Dateien).
2. Vor dem Commit: Vorschau/Screenshot zeigen, wenn es eine optische Änderung ist.
3. Commit-Message wird aus `git diff` generiert, Format: `<Art>: <kurze Beschreibung>` (z. B. `Fix: Zoom-Effekt nur noch bei kleinen Bildpaaren`, passend zum bisherigen Stil in der Commit-Historie).
4. Push erst nach Bestätigung durch Helena.
