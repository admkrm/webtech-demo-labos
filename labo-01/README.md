# Labo 1 - Je werkplek en je eerste pagina's: modeloplossing

Niet voor studenten.

Bij `opgaven/labo-01.md`. Er zijn geen startbestanden: het labo begint van nul. De map `labo-01/` hier is wat een student op het einde in zijn repository `webtech` heeft staan, met precies de bestandsnamen die de feedback-tooling vanaf labo 2 verwacht. De foto is een placeholder (`afbeeldingen/schelde.jpg`); de alt-tekst is het antwoordmodel, niet de foto. Open de map met Live Server om de links te controleren.

## Overzicht

| Oefening | Bestand(en) | Kern |
|---|---|---|
| 1. Werkplek | `index.html` | map als workspace, skelet uit het hoofd, werklus bewerk-bewaar-kijk |
| 2. Kijken naar de pagina | geen | Elements-tab toont de herstelde boom, niet het bestand |
| 3. Over mij | `over-mij.html` | h1, drie p, h2 + ul, h2 + ol, één em en één strong |
| 4. Tags opzoeken | commentaar bovenaan `over-mij.html` | acht elementen in één zin per element, eigen woorden |
| 5. Structuur | `hobby.html` + header/footer in alle pagina's | grondplan header-main-footer, nav met ul, img met echte alt, absolute link |
| 6. Boodschappenlijst | `boodschappen.html` | ul met li's, links in li's, opgenomen in elke nav |
| 7. Online | repo `webtech`, GitHub Pages | map uploaden in de browser, Pages aanzetten, adres op telefoon openen |

## 1. Je werkplek

Kern: de map `webtech` als workspace (*File - Open Folder*), submap `labo-01`, skelet getypt (syllabus 1.5), Live Server, werklus. Bestandsnamen in kleine letters zonder spaties.

Typische fouten:

- los bestand geopend in plaats van de map; Live Server doet dan niets of opent de verkeerde map -> *File - Open Folder*
- map in OneDrive of iCloud; werkt vandaag, geeft later synchronisatieproblemen met de repository
- skelet gekopieerd in plaats van getypt; merk je aan wie in oefening 3 het skelet niet meer uit het hoofd kan

## 2. Kijken naar de pagina

Kern: na het verwijderen van `</p>` staat de sluittag in de Elements-tab toch; de browser herstelt stil (syllabus 1.6 en het motorkap-kader). Het punt: de Elements-tab is de waarheid over de boom, het bestand niet.

Verwacht inzicht bij navraag: "de browser klaagt niet, maar wat hij bouwde is niet wat ik schreef". Wie zegt "de pagina werkt dus het is goed" heeft het punt gemist; verwijs naar F1.10.

## 3. Over mij

Antwoordmodel: zie `over-mij.html`. Eén `h1` (de naam), twee tot drie `p`, `h2` "Wat ik graag doe" met `ul`, `h2` "Mijn ochtend" met `ol`, één `em` en één `strong` in een paragraaf.

Let op: in de modeloplossing staan de twee tussenkoppen als `h3`, omdat de site-`h1` in de header staat en de naam de `h2` van de pagina is (oefening 5 voegt die header toe). Beide zijn correct zolang de niveaus niet springen; een `h4` pal onder een `h2` is F1.2.

Typische fouten:

- tekst rechtstreeks in `body` of `main`, zonder `p` (F1.1)
- `ul` met tekst of `p` als rechtstreeks kind (F1.4); zichtbaar in de Elements-tab als tekstknoop vóór het eerste `li`
- `em` en `strong` gekozen om het uitzicht ("ik wil dit vet"); vraag naar de reden, niet naar het antwoord: klemtoon is `em`, belang of waarschuwing is `strong`
- `<br>` als witruimte tussen paragrafen

## 4. Tags opzoeken

Antwoordmodel: de acht commentaarregels bovenaan `over-mij.html`. Beoordeel op eigen woorden en op de kern: `main` is uniek per pagina en er is er één; `header` en `footer` keren terug; `nav` is een blok links; `article` staat op zichzelf; `aside` staat ernaast; `a` heeft `href`; `img` heeft `src` en `alt`. Een gekopieerde MDN-zin is niet fout, maar vraag dan om ze in eigen woorden te herhalen.

## 5. De structuur van een pagina

Antwoordmodel: `hobby.html`. Grondplan `header`, `main`, `footer` als de drie kinderen van `body` (syllabus 1.8); `nav` bevat een `ul`; `img` met relatief pad `afbeeldingen/naam.jpg` en een alt die zegt wat er op de foto staat; externe link met volledig `https://`-adres. Dezelfde header en footer in alle pagina's, en alle navigaties hebben vier links.

Typische fouten:

- `nav` in `main` of `h1` in `footer` (F1.8)
- `alt="foto"` of `alt` weggelaten (F1.5); "een foto van mij" is ook zwak, want het zegt niet wat er te zien is
- bestandsnaam met hoofdletter of spatie (`Schelde 1.JPG`): werkt lokaal, breekt na publicatie (F1.6); nu corrigeren, niet in oefening 7
- foto van 4 MB uit de telefoon: werkt vandaag; benoem dat dit in hoofdstuk 6 terugkomt
- navigatie gekopieerd naar de andere pagina's maar de link naar `hobby.html` vergeten in `index.html` of `over-mij.html`
- `href="#"` als tijdelijke link: niet toestaan, de pagina's bestaan

## 6. Boodschappenlijst

Antwoordmodel: `boodschappen.html`. `ul` met uitsluitend `li`; wat online gekocht wordt, heeft een `a` ín het `li` (niet eromheen). Pagina opgenomen in elke `nav`.

Typische fout: `<a>` rond het `<li>` in plaats van erin; de validator meldt dit, de browser herstelt het stil.

## 7. Je pagina's online

Kern: repo `webtech`, public, met README; de map `labo-01` als geheel geüpload (niet de losse bestanden, anders ontbreekt `afbeeldingen/`); Pages op `main` en `/ (root)`; adres `https://gebruikersnaam.github.io/webtech/labo-01/index.html`.

Typische fouten:

- losse bestanden gesleept: de afbeelding ontbreekt online
- repo privé gezet: Pages werkt niet op een gratis account
- adres met hoofdletters getypt; GitHub-gebruikersnamen zijn in het adres altijd kleine letters
- lokaal werkende afbeelding die online kapot is: bijna altijd F1.6 (hoofdletter of spatie in bestandsnaam of pad)
- Pages nog niet klaar: even wachten en verversen, niet opnieuw uploaden

## Klaar? - controles

Validator: op de vier pagina's van de modeloplossing meldt validator.w3.org niets. Bij studenten meldt hij meestal: ontbrekende `title`, tekst rechtstreeks in `ul`, gekruiste tags, `alt` ontbreekt. Dat zijn de fouten die de browser stil herstelt en die de student dus zelf nooit zag: precies het punt van de oefening.

Boom van `hobby.html` (antwoordmodel voor de tekening):

```
body
  header
    h1
    nav
      ul
        li  a
        li  a
        li  a
        li  a
  main
    h2
    p
    img
    p
      a
  footer
    p
```

Wie `a` als broer van `li` tekent in plaats van als kind, heeft de nesting van de lijst niet begrepen; wie `img` onder `p` hangt terwijl het ernaast staat, heeft de Elements-tab niet vergeleken.

## Wat de feedback-tooling vanaf labo 2 op deze bestanden checkt

Geldige boom (validator-equivalent), precies één `h1` per pagina, geen niveausprongen in hoofdingen, `ul` en `ol` met uitsluitend `li`-kinderen, elk `img` met niet-leeg en niet-generiek `alt` ("foto", "afbeelding", "image"), `lang="nl"`, `header`, `main` en `footer` als kinderen van `body`, `nav` bevat een `ul`, bestandsnamen in kleine letters zonder spaties, alle relatieve paden resolveerbaar.
