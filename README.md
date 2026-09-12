# examination-frontend-grupp1

Osama: Navigation footer
Dan: Hero
Zachery: Grid


På min eventsida använder jag till exempel:

<nav> för navigationen
<header> för Hero-sektionen
<main> för sidans huvudinnehåll
<section> för About, Artists, Schedule och Tickets
<article> för de olika artisterna
<footer> för sidfoten


Jag har använt semantisk HTML eftersom det gör koden tydligare och mer strukturerad. Det hjälper också webbläsare, sökmotorer och hjälpmedel som skärmläsare att förstå sidans struktur.

2. Hur fungerar arv i CSS? Ge ett exempel från er egen kod.

Arv i CSS betyder att vissa CSS-egenskaper automatiskt förs vidare från ett föräldraelement till dess barn.

body {
    font-family: sans-serif;
    font-size: 1rem;
}

Eftersom font-family och font-size är egenskaper som kan ärvas, får texten i elementen inne i <body> normalt samma typsnitt och storlek om jag inte anger något annat.

Både <h1> och <p> ligger inuti <body> och kan därför ärva font-family: sans-serif.

Jag använder alltså arv för att slippa skriva samma CSS på varje element.

3. Vad är den största skillnaden mellan Flexbox och CSS Grid, och när ska man använda vilket verktyg?

Den största skillnaden är att Flexbox främst är till för layout i en dimension, medan CSS Grid är till för layout i två dimensioner.

.artist-cards {
    display: flex;
    gap: 2rem;
    justify-content: center;
    flex-wrap: wrap;
}


Här vill jag placera flera artistkort bredvid varandra och låta dem flytta till nästa rad när skärmen blir mindre. Därför passar Flexbox bra.

CSS Grid passar bättre när man vill kontrollera både rader och kolumner

.main {
    display: grid;
    grid-template-columns: 1fr 3fr;

    grid-template-areas:
        "about artists"
        "schedule tickets";
}

Här bestämmer jag både kolumner och rader, så Grid passar bättre.

Jag använder också Grid för schemat eftersom en timetable naturligt kan organiseras i rader och kolumn