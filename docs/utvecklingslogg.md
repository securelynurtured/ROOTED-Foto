# Utvecklingslogg – ROOTED Foto

## Steg 01 – HTML-grundstruktur

Datum: 2026-11-01.

### Genomförande

Tre sammanlänkade HTML-sidor skapades: startsida, fotograferingar och kontakt.
Startsidan följer innehållsordningen i Figma-underlaget. Fotograferingssidan
beskriver tjänsterna och arbetsgången. Kontaktsidan innehåller adressen
Glädjens Gränd 2, 903 63 Umeå, klickbara länkar för telefon och e-post,
samt ett formulär.

### Val och motivering

- Semantiska element används för att beskriva sidornas struktur.
- Samma navigation och sidfot används på alla sidor för att skapa igenkänning.
- Sidornas språk anges som svenska och varje sida har en egen titel.
- Bilder har beskrivande alt-texter och formulärfält har synliga etiketter.
- HTML-strukturen byggs först. Utseende och interaktivitet utvecklas i
  efterföljande steg för att kunna kontrolleras var för sig.

### Kontroller

Samtliga sidor kontrollerades med W3C Nu Html Checker, version 26.11.1.

| Sida | Fel | Varningar |
| --- | --- | --- |
| index.html | 0 | 0 |
| fotograferingar.html | 0 | 0 |
| kontakt.html | 0 | 0 |

De fullständiga svaren, kontrolltidpunkterna och filernas SHA-256-värden
finns i [valideringsresultatet](validation/01-html-validation.json).
Resultaten gäller HTML-filerna i detta utvecklingssteg och behöver
kontrolleras igen när innehållet förändras.

Navigationen från startsida till fotograferingar, vidare till kontakt och
tillbaka till startsidan kontrollerades i Chrome. Bilder och sidfötter
granskades visuellt. Kontaktuppgifternas länkar kontrollerades i
webbläsarens tillgänglighetsträd. Ett klick på Namn-etiketten fokuserade
motsvarande formulärfält. Skicka-knappen var inaktiverad enligt planen.

Tre [skärmbilder](screenshots/README.md) sparades från den lokala
webbläsarvyn med bredden 1440 CSS-px. Bilderna visar HTML-steget och
kan användas för att beskriva genomförandet i rapporten.

### Kvar i detta skede

CSS, responsiv layout, mobilmeny och JavaScript-validering återstår.
Formulärets skicka-knapp är därför tillfälligt inaktiverad. Formuläret
skickar inga meddelanden.

### Nästa steg

Utforma webbplatsen med färger, typografi och layout enligt Figma-underlaget.

## Steg 02 – Gemensam sidstruktur

Datum: 2026-11-01.

### Genomförande och motivering

Fotograferings- och kontaktsidans huvudrubrik och introduktion placerades
i en inledande `<section>`, enligt samma mönster som startsidan.
Innehållet på respektive sida behölls.

De gemensamma delarna följer startsidans kodstruktur: dokumentets början,
skipplänk, header, navigation, main-element och sidfot. Sidtitel,
metabeskrivning och `aria-current="page"` anpassas till den aktuella sidan.
Det sidspecifika huvudinnehållet ligger inom `<main>`.

### Kontroller

Koden utanför huvudinnehållet jämfördes mellan alla tre sidor. Efter att
sidtitel, metabeskrivning och aktuell sidmarkering undantagits var koden
identisk. Varje sida hade exakt en aktuell sidmarkering.

De två ändrade sidorna kontrollerades med W3C Nu Html Checker. Båda gav
0 fel och 0 varningar. Resultaten finns i
[valideringen för steg 02](validation/02-shared-structure-validation.json).
