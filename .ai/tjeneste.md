Tanken her er at vi skal lage ulike skills/ferdigheter for AI til hvordan vi kan utvikle tjenestesider til våre kunder (tenk bedrifter som leverer tjenester). For å lage gode tjenesider, menneske eller AI, så trenger man en SOLID prosess. Denne prosessen tar for seg stegene som gir mening for å skape gode tjenestesider og artikler rundt det bedriften leverer.

Krav:

1. Hver skill må være separert og kan kjøres alene
2. Vi har en totalskill som kan trigges av kommand som kjører helle prosessen start til slutt med minimalt input.
3. Må kunne jobbe med helt nye tjenester vi ikke har utarbeidet tidligere, og vi må også kunne håndtere artikler som allerede eksisterer men som trenger en forbedring.

---

Så hva skal til for å lage godt innhold?

## Forstå kunde og leveranse

I møte med kunden kan vi spørre kort om tjenester de leverer og hvilke andre bedrifter de ser som konkurrenter, både lokalt og nasjonalt. Er det noen som utmerker seg ekstra sterke i bransjen og er kanskje norgesledene?

Ut fra denne feedbacken bør vi kunne ha nok til å gjennomføre mest mulig uten for mye involvering av kunden.

## Tjenestelister

Vi må ha en skill som tar utgangspunktet i konkurrenter og tjenester kunden har nevnt. Så får vi Claude eller AI til å søke på nett på konkurrentene, tjenestene og andre aktører i samme bransje. Målet er å ha en forholdsvis komplett oversikt over tjenesteomfanget i bransjen og hvordan disse ofte beskrives. 

Ofte vil tjenester bestå av hovedtjenester med underleveranser, eller tjenester som ofte inkluderer andre tjenester. Tenk f.eks. rørlegger som leverer vannbåren varme ofte leverer også varmekilder, energiberegninger osv. Vi må ha gode lister på tjenester, hva som ofte inngår og gjerne sortert i en liste ut fra “ofte nevnt” eller de fleste leverer til mer unike tjenester.

Målet er at vi har en komplett oversikt over tjenesteleveransen i korte stikkord og liste som vi kan gi til våre kunder. De må gi feedback om de leverer disse tjenestene, om de leverer noe mer som bør inn og hva som eventuelt ikke leveres.

Det er ofte ønskelig å si noe om priser, enten konkret eller sammenligne. Det kan være fint å få feedback på hva virksomheten tar betalt, eller ser på det med prisbilde på tjenesten.

## Gruppering av tjenester

Ofte er tjenester i grupper med underleveranser, eller at virksomheten har mange tjenester og at vi må derfor gruppere de på en solid måte. Vi må forstå strukturen og omfanget av leveransen og hva som hører sammen. På den måten kan vi definere **hvilke sider** vi skal bygge, hvordan de skal struktureres. Hva som er tjeneste og hva som kanskje bare er et notat i en tjeneste eller en egen artikkel.

Målet er at vi kan lage en liste over artikler som skal utarbeides og hva de i hovedtrekk bør inneholde. Listen må kunne kopieres til Fjellvarden OS oppgaveliste (SOP) på kunden. Slik at vi kan spore utviklingen og prioritere.

---

<aside>
⚠️

Herfra kan vi starte full automatikk pipeline på utvikling av tjenestesider

</aside>

## Innhenting av kilder, innhold og research

Nå som vi vet hva vi skal skrive og hvordan det skal struktureres trenger vi innhold og kunnskap slik at vi har et godt grunnlag for å skrive en god artikkel. Vi får claude/ai til å søke nettet og finne kilder og scrape nettsidene for data som vi kan lagre til markdown filer i en mappe. Her må også underleveranser og detaljer i egne mapper slik at vi har godt organisert innhold for tjenesten.

Hensikten er å ha all innhold og kontekst til å kunne skrive ferdige tjenestesider som er omfattende og treffer godt!

## SEO data

Vi må vite hva folk søker på. Hva er det konkurrentene får mest trafikk på? Hvilke spørsmål er det ofte folk lurer på i forbindelse med tjenesten? Vi må bruke tjenester som DataForSEO, SerpApi, Google Trends osv for å innhente så mye data som mulig.

Dette lagres i egen markdown, og skal være endel av utformingen av innholdet.

# Outline review

Mellom gruppering og research bør det finnes et steg der strukturen på selve artikkelen godkjennes (overskrifter, vinkling, CTA). Det er mye billigere å justere en outline enn å omskrive en hel side.

## First draft - Tjenestesiden

Nå som vi vet hva siden skal omhandle og vi har alt innholdet vi trenger og hvordan det søkes etter så har vi i grunn nok til å lage en solid tjenesteside.

Her må vi ha en solid AI Skill/ferdighet som forstår hvordan den skal lese kodebase, forstå design oppsett, hvilken kundereise vi forventer at en tjeneste har, hvilke ord og retningen den skal bygge innhold på. Det må være veldig tydelig hva vi ønsker å få ut av tjenestesiden. 

Det er mange detaljer å ta stilling til, som f.eks. om tjenestesiden skal ha bilder eller ikke, hvilke design den skal se etter osv. Nok data til å ta gode valg.

Kort oppsummert så er dette en viktig og kompleks skill. Som danner grunnlaget for hvor god siden blir.

**"They Ask, You Answer" (Marcus Sheridan)**

Hele premisset er at de beste tjenestesidene svarer direkte på spørsmålene kundene faktisk stiller. Dere har SEO-steget, men vurder å gjøre det mer eksplisitt: bygg innholdsstrukturen rundt reelle spørsmål, ikke bare søkeord. "Hva koster vannbåren varme?" er bedre enn en generisk tjenestebeskrivelse.

**Inverted Pyramid (journalistikk)**

Det viktigste først. Tjenestesider bør åpne med kjernesvaret, ikke bygge opp til det. Mange bedriftssider feiler her fordi de skriver "om oss" når de burde skrive "dette løser vi for deg".

**Jobs To Be Done-perspektivet**

Folk kjøper ikke en tjeneste, de "ansetter" den for å løse et problem. Skriv fra brukerens jobb, ikke leverandørens leveranse. Dette bør inn som en eksplisitt del av skrivepromptet i "First draft"-skillen.

**Hemingway-prinsippet for revisjon**
"Write drunk, edit sober." Første utkast skal være rikt og omfattende (det dere kaller First Draft). Deretter kutte brutalt. Dere har Content Review og Content Polish som separate steg, og det er smart. Men vurder å legge inn et eksplisitt **kuttesteg** mellom review og polish. Spør: "Hva kan fjernes uten å tape verdi?"

**"One reader"-teknikken**

Gode forfattere skriver til én konkret person. For tjenestesider: definer en primærpersona per side. Er dette en boligeier som vurderer varmepumpe, eller en utbygger som trenger 50 enheter? Det endrer alt fra ordvalg til detaljeringsnivå.

**Tone of voice / stilguide mangler som eget steg.** Dere nevner det under Content Polish, men det bør defineres *før* First Draft. Skillen som skriver trenger klare retningslinjer, ikke bare "vær menneskelig".

## Content review

Nå som tjenestesiden er bygget så må vi sjekke at tjenestetekstene ikke er plagiat av innholdet vi har hentet inn. At kundereisen er fulgt og gir den mening. Vi bør kvalitetsjekke påstander. Er f.eks. innholdet evergreen eller blir det fort utdatert? AI må ta på seg ulike roller, f.eks, kritisk kunde, kvinne, mann osv og sørge for at innholdet treffer bredt og godt. 

## Content polish

Det blir fort mye AI skriveri. Det vil si bruk av emdash, setninger i tilsvarende lengder og annet som får en til å “grine på nesa” når man leser. Vi ønsker at språket vårt er varmt, mest mulig menneskelig, bruker normale ord og uttrykk, er tydelig osv. 

"Fjern AI-skriveri" er vagt. Lag en sjekkliste: unngå emdash, variér setningslengde, maks X adjektiver per avsnitt, unngå "i en verden der..." osv. Jo mer konkret reglene er, jo bedre kan AI-en følge dem.

Språket må også passe tjenestesider. Tekst må være tydelig. SEO rettet, men mest rettet mennesker.

## Design review

Kan vi få Claude til å bruke Chrome eller Playwright til å analysere designet og sørge for at layout er god? I såfall bør vi få noen øyne på siden og sørge for at det visuelt sett er korrekt.

## Simplify

Vi bør etter dette sørge for at kildekode er god. Er f.eks. korrekte styles gode. Er det duplikater av andre sider som burde mer inn i en global css kode osv.

## SEO Metadata

Vi bør sørge for at vi har en siste SEO sjekk. Schema data, title, descriptions etc. 

## Intern linking

Andre nettsider som omhandler tjenesten bør linke til den nye siden.

## Epost til kunde

Vi bør ha en klar e-post til kunde med god forklaring på hva de må se etter og hvordan de skal forholde seg til endringene. 

---

Etter dette er det bare å publisere til en none-public Netlify build som kunden kan kjøre godkjenningsprosess på.
