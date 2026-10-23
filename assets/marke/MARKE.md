# Marke Pixxelbeast – Kurzfassung

Quelle: Logokoffer (`_Logokoffer.zip`, Ordner `Pantone/`, `RGB/`, `SW/`, Stand 2020–2022).
Wichtig: Im Logokoffer gibt es **keinen Styleguide** (kein PDF, kein Text).
Alle Angaben unten stammen aus den Logodateien selbst:
Farbfelder in den EPS-Dateien und exakt gezählte Pixelfarben der PNG-Logos.
Rollen der Farben sind daraus abgeleitet, nicht offiziell festgelegt.

## Farben

| Name | HEX | RGB | CMYK (aus EPS) | Druck | Rolle (abgeleitet) |
|---|---|---|---|---|---|
| Pixxel-Pink | `#FF3EB3` | 255 / 62 / 179 | 0 / 80 / 0 / 0 | PANTONE 806 C (Sonderfarbe) | Primärfarbe: Monster, „BEAST“, Einfarb-Logo |
| Schwarz | `#000000` | 0 / 0 / 0 | 91 / 79 / 62 / 97 (Tiefschwarz) | – | Text, „PIXXEL“ auf hellem Grund |
| Weiß | `#FFFFFF` | 255 / 255 / 255 | 0 / 0 / 0 / 0 | – | Hintergrund, „PIXXEL“ auf dunklem Grund |
| Pixel-Grün | `#78D900` | 120 / 217 / 0 | 55 / 0 / 100 / 0 | – | Akzent (kleine Pixel-Balken) |
| Pixel-Violett | `#7E15FD` | 126 / 21 / 253 | 80 / 80 / 0 / 0 | – | Akzent (i-Punkt-Pixel) |
| Monster-Lila | `#82008C` | 130 / 0 / 140 | 65 / 100 / 0 / 0 | – | Sekundär/Detail (Augenbraue des Monsters) |

Die Farbnamen sind beschreibend vergeben; offizielle Namen gibt es nicht (unklar).

## Schriften

- **Unklar.** Im Logokoffer sind keine Schriftdateien und keine Schriftnamen enthalten.
  Die Wortmarke „PIXXELBEAST“ ist in Pfade umgewandelt; die Schrift lässt sich nicht sicher bestimmen.
- Bis zur Klärung: neutrale Systemschrift verwenden (siehe CSS unten). Die Wortmarke nie mit einer Schrift nachsetzen, immer die Logodatei nehmen.

## Logo-Varianten

Alle Dateien liegen in `assets/marke/logos/` (PNG mit transparentem Hintergrund).

| Variante | Für | Datei |
|---|---|---|
| Logo komplett (Monster + Wortmarke), farbig | heller Grund | `logos/logo-farbig-heller-grund.png` (601 px), `logos/logo-farbig-heller-grund-gross.png` (1801 px) |
| Logo komplett, farbig | dunkler Grund | `logos/logo-farbig-dunkler-grund.png` (601 px), `logos/logo-farbig-dunkler-grund-gross.png` (1801 px) |
| Logo komplett, einfarbig schwarz (Strichversion) | heller Grund | `logos/logo-schwarz.png` (601 px), `logos/logo-schwarz-gross.png` (2501 px) |
| Logo komplett, einfarbig weiß (Strichversion) | dunkler Grund | `logos/logo-weiss-gross.png` (1251 px) |
| Wortmarke „PIXXELBEAST“, farbig | heller Grund | `logos/wortmarke-farbig-heller-grund.png` |
| Wortmarke, farbig | dunkler Grund | `logos/wortmarke-farbig-dunkler-grund.png` |
| Wortmarke, schwarz | heller Grund | `logos/wortmarke-schwarz.png` |
| Monogramm „PB“, farbig | heller Grund | `logos/monogramm-pb-farbig-heller-grund.png` |
| Monogramm „PB“, farbig | dunkler Grund | `logos/monogramm-pb-farbig-dunkler-grund.png` |
| Monogramm „PB“, schwarz | heller Grund | `logos/monogramm-pb-schwarz.png` |
| Bildmarke Monster, farbig | beliebig | `logos/monster-farbig.png` (105 px), `logos/monster-farbig-gross.png` (313 px) |
| Bildmarke Monster, schwarz | heller Grund | `logos/monster-schwarz.png` |

Hinweise:
- Es gibt **keine SVG-Dateien** im Logokoffer. Die Vektor-Originale (EPS in RGB, CMYK und PANTONE 806 C)
  liegen nur im Logokoffer, nicht in diesem öffentlichen Repository.
- Für große Darstellungen (z. B. Startseite, Retina) die `-gross`-Dateien nehmen.
- Kleine PNGs nicht hochskalieren.

## Regeln

- **Schutzzone:** unklar (nicht angegeben). Empfehlung bis zur Klärung: rundum frei lassen, mindestens die Höhe des „P“ der Wortmarke.
- **Mindestgröße:** unklar (nicht angegeben). Ist das Logo zu klein für die Wortmarke, das Monogramm „PB“ oder das Monster verwenden.
- **Verbote:** keine offiziellen Angaben. Grundsätzlich: Logo nicht verzerren, nicht umfärben, keine Effekte (Schatten, Konturen), keine Teile entfernen.
- **Heller/dunkler Grund:** Auf hellem Grund die Varianten mit schwarzer Schrift, auf dunklem Grund die Varianten mit weißer Schrift.
- **Tonalität / Claims:** unklar (keine Angaben im Logokoffer).

## CSS-Variablen

```css
:root {
  /* Markenfarben Pixxelbeast (aus Logodateien ermittelt) */
  --pb-pink: #FF3EB3;         /* Primärfarbe, PANTONE 806 C */
  --pb-gruen: #78D900;        /* Akzent */
  --pb-violett: #7E15FD;      /* Akzent */
  --pb-lila: #82008C;         /* Sekundär/Detail */
  --pb-schwarz: #000000;      /* Text */
  --pb-weiss: #FFFFFF;        /* Hintergrund */

  /* Rollen */
  --pb-farbe-primaer: var(--pb-pink);
  --pb-farbe-akzent: var(--pb-gruen);
  --pb-farbe-akzent-2: var(--pb-violett);
  --pb-farbe-text: var(--pb-schwarz);
  --pb-farbe-hintergrund: var(--pb-weiss);

  /* Schriften: Markenschrift unklar, daher Systemschriften als Platzhalter */
  --pb-font-headline: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  --pb-font-text: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
}
```
