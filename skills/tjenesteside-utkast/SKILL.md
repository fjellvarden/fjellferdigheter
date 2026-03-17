---
name: tjenesteside-utkast
description: Skriv første utkast av en tjenesteside basert på godkjent outline, research og SEO-data. Bruk denne skillen når du har en godkjent outline og skal skrive selve tjenestesiden, eller når noen sier "skriv tjenestesiden", "lag utkast", "first draft", "bygg siden".
---

# Tjenesteside — Første utkast

Dette er den viktigste skillen i pipelinen. Her skrives selve tjenestesiden. Første utkast skal være rikt og omfattende — det kuttes og poleres i senere steg.

## Utgangspunkt

Du trenger:
- Godkjent outline (fra **outline-review**)
- Research-mappe med faginnhold (fra **innhold-research**)
- SEO-data med søkeord (fra **seo-research**)
- Tilgang til kundens kodebase for å forstå design og komponenter

Alle fire bør være på plass. Mangler du research eller SEO, flagg det — du skriver dårligere innhold uten grunnlag.

## Før du skriver

### Forstå kodebasen
Les kundens eksisterende kode for å forstå:
- Hvilke komponenter og layouts som brukes
- Designsystem og stilvalg (farger, typografi, spacing)
- Hvordan eksisterende tjenestesider er bygget
- Bildebruk og mediehåndtering
- CMS-struktur hvis relevant

### Forstå kundereisen
En god tjenesteside følger leserens naturlige tankerekke:
1. **Gjenkjennelse** — "Ja, dette er problemet mitt"
2. **Forståelse** — "Slik løses det"
3. **Tillit** — "Disse folkene kan dette"
4. **Handling** — "Jeg tar kontakt"

### Sett tone of voice
Basert på kundens bransje og målgruppe, definer skrivestilen FØR du starter:
- Formelt eller uformelt?
- Teknisk eller folkelig?
- Kort og punchy, eller utfyllende og grundig?
- Hvordan tiltaler vi leseren? (du/dere/De?)

## Skriveprinsipper

### They Ask, You Answer
De beste tjenestesidene svarer direkte på spørsmålene kundene faktisk stiller. Bygg innholdet rundt reelle spørsmål, ikke generiske tjenestebeskrivelser.

Dårlig: "Vi tilbyr profesjonelle rørleggertjenester av høy kvalitet."
Bra: "Lurer du på hva det koster å bytte varmtvannsbereder? Her er det du trenger å vite."

### Inverted Pyramid
Det viktigste først. Åpne med kjernesvaret, ikke bygg opp til det. Leseren skal forstå hva siden handler om innen 5 sekunder.

### Jobs To Be Done
Folk kjøper ikke en tjeneste — de ansetter den for å løse et problem. Skriv fra leserens jobb, ikke leverandørens leveranse.

Dårlig: "Vi leverer vannbåren varme med 20 års erfaring."
Bra: "Vil du ha jevn varme i hele huset uten kalde gulv? Vannbåren varme er løsningen."

### One Reader
Skriv til primærpersonaen fra outlinen. Én konkret person. Er det en boligeier som googler om kvelden, eller en utbygger som sammenligner tilbud? Det endrer alt.

## Prosess

### 1. Følg outlinen
Bruk den godkjente outlinen som skjelett. Du kan avvike hvis det gir bedre flyt, men de store linjene skal stemme.

### 2. Skriv rikt
Første utkast skal være **omfattende**. Ta med alt som kan være relevant:
- Prosessbeskrivelser
- Prisinfo og kostnadsguider
- Vanlige spørsmål med gode svar
- Konkrete eksempler
- Fakta og tall fra researchen

Det er lettere å kutte enn å legge til. "Write drunk, edit sober."

### 3. Integrer SEO naturlig
- Primærsøkeord i H1, intro, og jevnt gjennom teksten
- Sekundærsøkeord i H2-er og naturlige steder
- Spørsmålssøk som faktiske spørsmål i innholdet
- Aldri keyword-stuffing. Hvis det høres unaturlig ut, skriv om.

### 4. Bygg i kodebasen
Skriv siden direkte i kundens kodebase:
- Bruk eksisterende komponenter og layout
- Match designsystemet
- Følg etablerte mønstre fra andre tjenestesider
- Legg inn placeholder for bilder med tydelige instruksjoner om hva som trengs

## Output

Selve filen i kodebasen (den faktiske tjenestesiden), pluss en kort notatfil:

```
# Utkast-notat — [Tjeneste]

## Valg tatt
- [tone of voice-valg]
- [design-valg]
- [innhold som ble prioritert / nedprioritert]

## Åpne spørsmål
- [ting som trenger kundens input]
- [steder der innhold mangler]

## Bilder trengs
- [seksjon]: [beskrivelse av bildebehov]

## SEO-sjekk
- Primærsøkeord: [søkeord] — brukt X ganger
- Sekundære: [liste]
```

Lagre notatet i `.ai/kunder/[bedriftsnavn]/utkast/[tjeneste-slug]-notat.md`.

## Viktig

- Ikke skriv "AI-tekst". Unngå generiske setninger som "I en verden der..." eller "Med vår ekspertise...". Vær konkret og direkte.
- Første utkast er et utkast. Det er OK at det er langt og litt rotete — det finpusses i review og polish.
- Bruk research og fakta. Påstander uten grunnlag svekker troverdigheten.
- Tenk mobil. De fleste leser på telefon — korte avsnitt, tydelige overskrifter, scanbart.
