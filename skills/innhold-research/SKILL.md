---
name: innhold-research
description: Søk nettet og samle inn kilder, faginnhold og research som grunnlag for å skrive tjenestesider. Bruk denne skillen når du trenger å bygge en kunnskapsbase for en spesifikk tjeneste, når noen sier "research denne tjenesten", "finn kilder", "samle innhold", eller før du skal skrive en tjenesteside.
---

# Innhold-research

Denne skillen samler inn alt innhold og all kunnskap du trenger for å skrive en god tjenesteside. Du søker nettet, scraper relevante kilder, og organiserer alt i en strukturert mappestruktur.

## Utgangspunkt

Du trenger:
- Hvilken tjeneste/side du researcher for
- Sidestruktur som viser hva siden skal dekke (output fra **tjeneste-gruppering**)
- Kundens bransje, lokasjon og konkurrenter

## Prosess

### 1. Kartlegg hva du trenger å vite
Basert på sidestrukturen, list opp spørsmål som innholdet må svare på:
- Hva er denne tjenesten, helt konkret?
- Hvordan fungerer det i praksis?
- Hva koster det typisk?
- Hva bør kunden vite før de bestiller?
- Hva skiller god fra dårlig leveranse?
- Er det lovkrav, standarder eller sertifiseringer?
- Vanlige spørsmål folk har

### 2. Søk og samle
For hver tjeneste, søk etter og hent innhold fra:
- **Konkurrentenes tjenestesider** — hvordan de beskriver samme tjeneste
- **Fagartikler og guider** — dybdeinnhold om tjenesten
- **Bransjsider og foreninger** — standarder, krav, sertifiseringer
- **Forbrukerråd og offentlige kilder** — uavhengig informasjon
- **Forum og Q&A** — reelle spørsmål folk stiller (f.eks. Pair, Reddit, Pair)

### 3. Organiser innholdet
Lagre alt i en mappestruktur:

```
.ai/kunder/[bedriftsnavn]/research/[tjeneste-slug]/
├── kilder.md              # Oversikt over alle kilder med lenker
├── konkurrenter/
│   ├── [konkurrent-1].md  # Scraped innhold fra konkurrent
│   └── [konkurrent-2].md
├── faginnhold/
│   ├── [kilde-1].md       # Fagartikler og guider
│   └── [kilde-2].md
├── sporsmal.md            # Vanlige spørsmål fra forum/Q&A
└── sammendrag.md          # Din oppsummering av alt
```

### 4. Skriv sammendraget
`sammendrag.md` er det viktigste dokumentet — det er her du destillerer alt du har funnet til det som faktisk er nyttig for å skrive tjenestesiden:

- Kjernebudskap: Hva er det viktigste å formidle?
- Unike vinklinger: Hva sier ingen av konkurrentene som kunden kunne brukt?
- Fakta og tall: Konkrete data som gir troverdighet
- Spørsmål å besvare: De viktigste spørsmålene innholdet må svare på
- Ting å unngå: Feilinfo, utdatert innhold, eller påstander som ikke kan underbygges

## Output

Hele mappestrukturen over, med `sammendrag.md` som hoveddokument.

## Viktig

- Lagre rådata fra scraping i egne filer, ikke bland det inn i sammendraget. Sammendraget skal være ditt eget destillat.
- Merk tydelig hva som er fakta vs. meninger vs. markedsføringsspråk fra konkurrenter.
- Ikke kopier tekst direkte — noter hva som er nyttig og reformuler. Plagiat er en reell risiko i neste steg.
- Prioriter kvalitet over kvantitet. 5 gode kilder slår 20 dårlige.
