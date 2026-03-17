---
name: tjenestelister
description: Research og kartlegg alle tjenester i en bransje ved å analysere konkurrenter og markedet. Bruk denne skillen når du trenger en komplett oversikt over tjenester i en bransje, når noen sier "finn tjenester", "kartlegg bransjen", "hva leverer konkurrentene", eller når du skal bygge en tjenesteliste for en kunde.
---

# Tjenestelister

Denne skillen researcher konkurrenter og bransjen for å bygge en komplett oversikt over tjenester som leveres i kundens marked. Resultatet er en strukturert liste kunden kan godkjenne og gi feedback på.

## Utgangspunkt

Du trenger:
- Kundens bransje og lokasjon
- Tjenester kunden allerede har nevnt
- Konkurrenter (nevnt av kunden eller funnet selv)

Hvis du mangler dette, be brukeren kjøre **kunde-intervju** først, eller samle inn det mest nødvendige selv.

## Prosess

### 1. Kartlegg konkurrenter
Søk på nett etter konkurrentene kunden har nevnt. Utvid listen med andre aktører i samme bransje — søk på bransjebegreper + lokasjon, og nasjonalt for å finne de store aktørene.

For hver konkurrent, besøk nettsiden og noter:
- Hvilke tjenester de tilbyr
- Hvordan de grupperer/navngir tjenestene
- Eventuelle priser eller prisindkasjoner
- Hva de fremhever som sine styrker

### 2. Bygg tjenestelisten
Samle alle tjenester du finner på tvers av konkurrenter i en strukturert liste. Organiser slik:

- **Hovedtjenester** — kjernetjenestene i bransjen (det alle eller de fleste leverer)
- **Undertjenester** — tjenester som ofte inngår i eller følger med hovedtjenester
- **Tilleggstjenester** — mer spesialiserte tjenester som noen aktører tilbyr
- **Relaterte tjenester** — tjenester i tilgrensende områder

For hver tjeneste, noter:
- Kort beskrivelse (1 setning)
- Hvor vanlig den er ("de fleste leverer dette" → "nisje/unik")
- Typisk prisindikasjon hvis tilgjengelig
- Hvilke andre tjenester den ofte henger sammen med

### 3. Prisbilde
Samle prisinformasjon der det er tilgjengelig:
- Konkrete priser fra konkurrenter som viser dette
- Prisområder og "fra-priser"
- Prismodeller (fastpris, timepris, prosjektpris)

## Output

Lagre resultatet som markdown:

```
# Tjenesteliste — [Bransje] i [Område]

## Kilder
- [Liste over konkurrenter/nettsider som ble undersøkt]

## Hovedtjenester
| Tjeneste | Beskrivelse | Utbredelse | Prisindikasjon | Relaterte tjenester |
|----------|-------------|------------|----------------|---------------------|
| ... | ... | ... | ... | ... |

## Undertjenester
[samme format]

## Tilleggstjenester
[samme format]

## Relaterte tjenester
[samme format]

## Prisbilde i bransjen
- [oppsummering av prisinfo]

## Anbefaling til kunden
- [kort oppsummering av hva som bør prioriteres]
```

Lagre i `.ai/kunder/[bedriftsnavn]/tjenesteliste.md`.

## Viktig

- Målet er en liste kunden kan gå gjennom og si "ja, dette leverer vi" / "nei, dette gjør vi ikke" / "dette mangler". Hold det enkelt og oversiktlig.
- Ikke anta at kunden leverer alt — listen er et utgangspunkt for dialog.
- Tenk på tjenester som en rørlegger tenker på rørsystemer: hovedledninger med forgreninger. Noen tjenester er alltid del av noe større, andre står alene.
