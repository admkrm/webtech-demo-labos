# Labo 2 - Wie wint? Selectors, cascade en je eerste nabouw: modeloplossing

Niet voor studenten.

Bij `opgaven/labo-02.md`. De startbestanden staan in `startbestanden/labo-02/` (voor studenten: `dist/labo-02-starter.zip`). Deze map bevat per oefening de uitgewerkte versie; de HTML-bestanden zijn identiek aan de starter (de student wijzigt ze niet). `nabouw/css/stijl.css` is de referentie-CSS: modeloplossing, bron van het screenshot én bron voor de meetpunten van de feedback-tooling.

## Overzicht

| Oefening | Bestand(en) | Kern |
|---|---|---|
| 1. Commit & Sync | repo `webtech`, gekloond in VS Code | van upload naar de wekelijkse routine; pushen is inleveren |
| 2. Selectors | `selectors/css/stijl.css` | acht selectors precies raak; vijf selectors lezen |
| 3. Voorspel, dan kijk | `cascade/`, tabel in README | tien cascade-vragen, eerst op papier, dan Styles-paneel |
| 4. Nabouw | `nabouw/css/stijl.css` | toetsvorm: HTML vergrendeld, tokens, rem, geen id's/!important |
| 5. Commit | push | eerste push waar de feedback-tooling naar kijkt |
| 6. Site | `site/css/stijl.css` in de repo van de student | B2.1: één stylesheet voor vier pagina's, tokens, nav met hover en focus |

Timing (richtpunt): 1 = 15 min, 2 = 15 min, 3 = 25 min, 4 = 45 min, 5 = 5 min, 6 = 15 min + thuis.

## 1. Van uploaden naar Commit & Sync

Kern: Git geïnstalleerd en `git config` gezet (Voor je begint), map `webtech` op de schijf hernoemd naar `webtech-oud`, repo gekloond via *Clone Git Repository...*, `labo-02` erin gesleept, eerste commit en sync vanuit VS Code.

Typische problemen:

- Windows zonder Git: *Clone* doet niets of geeft "git not found" -> git-scm.com, VS Code herstarten
- Mac zonder Git: `git --version` in Terminal start de installatie van de command line developer tools (10 min); VS Code herstarten
- *Commit* faalt op `user.name`/`user.email` (vooral Windows; Git raadt op een Mac meestal zelf iets): de twee `git config --global`-regels uit *Voor je begint*, stap 3
- aanmeldvenster bij de eerste *Sync* komt van VS Code óf van Git Credential Manager (Windows): beide via browser, *Authorize*
- niet aangemeld bij GitHub: clone van een publieke repo lukt wel, sync niet -> account-icoon linksonder
- gekloond ín `webtech-oud` of in OneDrive -> opnieuw, op een gewone plek
- "stagen"-vraag met *No* beantwoord: commit is leeg -> *Always* kiezen of de bestanden met + stagen
- student wil labo-01 uit `webtech-oud` "ook nog eens" kopiëren: niet nodig, hij staat al in de kloon

Wie hier na 20 minuten nog vastzit, gaat verder met oefening 2 tot 4 in de kloon en doet de sync met een begeleider bij oefening 5.

## 2. Selectors schrijven en lezen

Antwoordmodel: `selectors/css/stijl.css`, met per opdracht de selector en in commentaar de typische fout. Het antwoordmodel voor de vijf leesselectors staat onderaan dat bestand.

Beoordeel op precisie, niet op uitzicht: `nav a` en `header nav ul li a` geven hetzelfde beeld, maar het tweede is F-materiaal voor volgende week (overspecifiek, AI-kader). Bij 3 is `.rassen li` de klassieker: het verschil is alleen in de binnenlijsten te zien. Bij 8 vergeet de helft `:focus`; laat ze met de tab-toets door de pagina gaan (F2.11).

## 3. Voorspel, dan kijk

Antwoordmodel:

| vraag | kleur | trede | toelichting |
|---|---|---|---|
| 1 | groen | herkomst | auteursstijl verslaat de blauwe link van de user agent stylesheet |
| 2 | blauw | volgorde | zelfde selector twee keer; de laatste wint |
| 3 | rood | specificiteit | class (0,1,0) verslaat element (0,0,1), ook al staat het element later |
| 4 | rood | selector raakt niet | `.v4 > a` raakt niets: de a is geen direct kind van de section; alleen `.v4 a` raakt |
| 5 | blauw | specificiteit | één id verslaat drie classes |
| 6 | blauw | overerving verliest | `.v6-tekst` raakt de p zelf; de rode kleur op de section is alleen geërfd |
| 7 | rood | overerving | geen enkele regel raakt blockquote; hij erft van `.v7` |
| 8 | blauw | inline style | het style-attribuut wint van elke selector in de stylesheet (2.3) |
| 9 | rood | !important | springt boven de normale orde uit; de class verliest (2.7) |
| 10 | groen, normale grootte | vergeten puntkomma (F2.3) | `font-size: 1.5rem color: blue` is één onbegrijpelijke declaratie; de browser laat ze vallen, `color: green` blijft |

Vraag 4, 8 en 10 zijn de leerzaamste. Bij 4 zeggen studenten "groen, want `>` is specifieker": nee, `>` verandert niets aan de specificiteit, en de regel raakt gewoon niet (F2.4). Bij 10 toont het Styles-paneel het waarschuwingsteken; laat het zien.

## 4. De nabouw

Referentie-CSS: `nabouw/css/stijl.css`. Screenshot gerenderd met Chromium (Playwright), venster 1280 px breed, schaalfactor 2, volledige pagina; Georgia en Verdana via Liberation Serif en Liberation Sans, vandaar het lichte verschil in letter met een Mac of Windows.

Wat de student moet halen (de meetlat van de feedback-tooling, computed styles op de gerenderde pagina):

| element | property | waarde |
|---|---|---|
| `body` | background-color / color / font-family / line-height | #fbf7f0 / #2b2b2b / Verdana / 1.6 (computed 25.6px) |
| `h1` | font-family / font-size / color / font-weight | Georgia / 48px / #b5451b / 400 |
| `h2` | font-size | 28px |
| `h3` | font-size / color | 20px / #6b6b6b |
| `.slogan` | font-style / color | italic / #6b6b6b |
| `nav a` | color / text-decoration / font-weight | #b5451b / none / bold |
| `nav a:hover`, `nav a:focus` | color / text-decoration | #2b2b2b / underline |
| `.intro` | font-size | 20px |
| `main a` | color | #b5451b |
| `main a:hover`, `main a:focus` | background-color / color | #b5451b / #fbf7f0 |
| `strong` | color | #b5451b |
| `.kaart li:nth-child(odd)` | background-color | #f1e9dc |
| `.prijs` | color / font-style | #6b6b6b / italic |
| `footer` | color / font-size / text-align | #6b6b6b / 14px / center |
| `footer a` | color | #6b6b6b |

Structuurchecks: `index.html` byte-gelijk aan de starter; `:root` met minstens vijf custom properties; geen kleurwaarde buiten `:root` (alle kleuren via `var()`); geen `px` in `stijl.css`; geen `#`-selector; geen `!important`; `:focus` overal waar `:hover` staat.

Typische fouten:

- `index.html` toch aangepast (class op de nav, style-attribuut): nul voor de nabouw, zoals op de toets; zeg dat vooraf
- `css/stijl.css` niet gevonden: bestand naast index.html gezet in plaats van in `css/` (F2.1)
- kleuren letterlijk in de regels in plaats van via tokens (F2.10); werkt, maar mist het punt
- `font-size: 48px` (F2.9); "16 px basis" in de opgave is de hint, niet de eenheid
- `h1 { font-weight: normal }` vergeten: koppen in Georgia zijn standaard vet, in het screenshot niet
- `a { color }` in plaats van `nav a` en `main a` apart: de footer-links worden dan accentkleur (2.5: selecteer met structuur)
- `.kaart li:nth-child(even)`: verkeerde helft gestreept; kijk naar het screenshot, het eerste item is gekleurd
- `line-height: 1.6rem` in plaats van `1.6` (2.8): de intro op 1.25rem krijgt dan te weinig regelhoogte
- hover zonder focus (F2.11)

Zen-moment: `css/zen.css` uit de starter; gebruikt `text-transform` en `letter-spacing` (hoofdstuk 7) en `list-style: none`; benoem dat als "kijken, niet nadoen".

## 6. Je site

Geen modeloplossing: de site is per student. Beoordeel op: `site/` naast `labo-01/`; één `site/css/stijl.css`, gelinkt vanuit alle vier de pagina's met `css/stijl.css`; tokenblok met rolnamen (`--color-accent`, niet `--color-blauw`); basis op `body`; `nav a` met `:hover` én `:focus`; geen `#`, `!important` of `style=""`; live op `https://USER.github.io/webtech/site/`.

Typische fouten: stylesheet in `labo-01` gezet en `site` vergeten; `href="stijl.css"` zonder `css/`; token gedeclareerd maar nergens gebruikt; `a:hover` zonder `:focus`.

## Klaar? - controles

Styles-paneel zonder waarschuwingsteken op de nabouw; validator op de vier site-pagina's via hun Pages-adres; README ingevuld; alles gepusht.

## Thuis: R2.3

Antwoordmodel bestaat niet (output verschilt per model), wel de meetlat: elke bevinding verwijst naar een sectie of foutnummer. Verwacht: px voor lettergroottes (F2.9), kettingen als `header nav ul li a` (AI-kader), `!important` als het model de user agent-stijl "moest" overschrijven (F2.6), letterlijke kleuren ondanks de meegegeven tokens (F2.10), geneste spelling (2.5). Vijf bevindingen zonder verwijzing is niet voldaan.

## Wat de feedback-tooling op deze push checkt

Repo bevat `labo-02/README.md` met de tabel van oefening 3 ingevuld; `labo-02/selectors/css/stijl.css` bevat de acht selectors (string-check op `nav a`, `footer p`, `.rassen > li`, `h2 + p`, `nth-child(odd)`, `last-child`, `.slogan, .intro` of omgekeerd, `main a:hover` én `main a:focus`); `labo-02/nabouw/index.html` ongewijzigd; `labo-02/nabouw/css/stijl.css` haalt de structuurchecks en de meettabel hierboven (tolerantie: kleuren exact, groottes ±1px); `site/css/stijl.css` bestaat en wordt door de vier pagina's geladen; nergens `style=""`, `#`-selector of `!important` in eigen CSS.
