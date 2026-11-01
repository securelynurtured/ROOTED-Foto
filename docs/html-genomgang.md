# HTML-struktur – ROOTED Foto

HTML beskriver innehållets struktur och betydelse. Samma grundstruktur
används på webbplatsens tre sidor för att ge en enhetlig navigation.

## Dokumentets början

- `<!doctype html>` anger att dokumentet använder modern HTML.
- `<html lang="sv">` anger svenska som sidans språk.
- `<head>` innehåller information om dokumentet, exempelvis teckenkodning,
  sidtitel och beskrivning.
- `charset="utf-8"` gör att bland annat å, ä och ö kan visas korrekt.
- `viewport` anpassar sidans visningsyta till enhetens bredd. Den responsiva
  layouten byggs sedan med CSS.
- `<body>` innehåller det som visas och används på sidan.

## Gemensamma delar

| Del | Funktion |
| --- | --- |
| Länken Hoppa till innehållet | Gör det möjligt att gå direkt till sidans huvudinnehåll. |
| `<header>` | Samlar verksamhetens namn och huvudnavigationen. |
| `<nav>` | Anger att länkarna används för navigation. |
| `aria-current="page"` | Markerar den aktuella sidan för hjälpmedel. |
| `<main>` | Innehåller det unika huvudinnehållet på respektive sida. |
| `<footer>` | Samlar verksamhetens namn, kontaktlänk och märkningen Studentprojekt. |

## Rubriker, sektioner och länkar

Varje sida har en huvudrubrik, `<h1>`. Underrubrikerna använder `<h2>` och,
för startsidans tjänstekort, `<h3>`. Rubriknivåerna beskriver innehållets
ordning och väljs efter struktur.

`<section>` samlar innehåll med ett gemensamt ämne och en rubrik.
Startsidan använder `<article>` för tjänstekorten, eftersom varje kort
beskriver en egen fotografering.

En länk, `<a href="kontakt.html">`, används för att gå till en annan sida.
En knapp används för en handling, exempelvis att skicka ett formulär.

## Bilder

`src` anger bildens sökväg. `alt` beskriver bildens innehåll när bilden inte
kan ses. `width` och `height` anger bildens visningsmått och proportioner.
CSS används senare för att anpassa bilderna till mindre skärmar.

Mellanslag i bildfilnamn skrivs som `%20` i bildens URL. Bilder längre ned
på sidan använder `loading="lazy"`, vilket låter webbläsaren skjuta upp
inläsningen tills bilden närmar sig visningsytan.

## Kontaktformuläret

- `<label>` ger fältet en synlig benämning. Dess `for` matchar fältets `id`.
- `name` anger vilket namn fältets värde har i formulärdata.
- `type="email"` anger att ett fält ska innehålla en e-postadress.
- `autocomplete` hjälper webbläsaren att föreslå namn och e-postadress.
- `<select>` innehåller val av fotografering.
- `<textarea>` används för ett längre meddelande.
- `required` markerar obligatoriska fält. Uppgiftens JavaScript-validering
  läggs till i ett senare steg och ersätts inte av detta HTML-attribut.
- Skicka-knappen är tillfälligt inaktiverad med `disabled` under HTML-steget.
  Den aktiveras när JavaScript-hanteringen finns på plats.

Formuläret är en demonstration inom studentprojektet. Inga meddelanden
skickas till en mottagare.
