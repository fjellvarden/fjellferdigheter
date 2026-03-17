---
name: tjeneste-gruppering
description: Grupper tjenester i logiske kategorier og definer sidestruktur for nettsiden. Bruk denne skillen når du har en tjenesteliste og trenger å planlegge hvilke sider som skal lages, hvordan tjenester henger sammen, og hva som blir egne sider vs. deler av andre sider. Trigger på "grupper tjenester", "planlegg sider", "sidestruktur", "hvilke sider trenger vi".
---

# Tjeneste-gruppering

Denne skillen tar en godkjent tjenesteliste og organiserer den til en konkret plan for hvilke nettsider som skal bygges, hva hver side skal dekke, og hvordan de henger sammen.

## Utgangspunkt

Du trenger:
- En godkjent tjenesteliste (output fra **tjenestelister**)
- Kundens bekreftelse på hvilke tjenester de leverer

Hvis dette mangler, be om det før du starter.

## Prosess

### 1. Analyser tjenestene
Gå gjennom tjenestelisten og identifiser:
- Hvilke tjenester er store nok til å fortjene en egen side?
- Hvilke tjenester er undertjenester som hører inn under en hovedside?
- Er det tjenester som bare trenger en kort omtale på en overordnet side?
- Finnes det temaer som fortjener en informasjonsartikkel (ikke tjenesteside)?

### 2. Definer sidestrukturen
For hver planlagt side, bestem:
- **Type:** Tjenesteside, kategoriside, eller informasjonsartikkel
- **Hovedtjeneste:** Hva siden primært handler om
- **Inkluderte undertjenester:** Hva som dekkes på samme side
- **Relasjon:** Hvordan denne siden kobler til andre sider

### 3. Prioritering
Sorter sidene etter prioritet:
- **Høy:** Kjernetjenester som driver omsetning og trafikk
- **Medium:** Viktige tjenester, men ikke kjernevirksomhet
- **Lav:** Nisjetjenester eller støtteartikler

## Output

```
# Sidestruktur — [Bedriftsnavn]

## Oversikt
- Antall tjenestesider: X
- Antall kategorisider: X
- Antall informasjonsartikler: X

## Sideplan

### Høy prioritet

#### 1. [Sidetittel]
- **Type:** Tjenesteside
- **URL-forslag:** /tjenester/[slug]
- **Hovedtjeneste:** [tjeneste]
- **Dekker også:** [undertjenester]
- **Hovedinnhold:** [2-3 setninger om hva siden bør formidle]
- **Målgruppe:** [hvem er primærleseren]

[gjenta for hver side]

### Medium prioritet
[samme format]

### Lav prioritet
[samme format]

## Oppgaveliste for Fjellvarden OS
| # | Oppgave | Prioritet | Status |
|---|---------|-----------|--------|
| 1 | Skriv tjenesteside: [tittel] | Høy | Ikke startet |
| 2 | ... | ... | ... |
```

Lagre i `.ai/kunder/[bedriftsnavn]/sidestruktur.md`.

## Oppgavelisten

Oppgavelisten på slutten er viktig — den skal kunne kopieres direkte til Fjellvarden OS (SOP) for å spore arbeidet. Hold den ren og enkel.

## Tips

- En side bør ha ett tydelig fokus. Hvis du er i tvil om noe er én side eller to, tenk på det fra kundens perspektiv: ville de søkt etter dette som én ting eller to separate ting?
- Kategorisider (f.eks. "Rørleggertjenester") er nyttige som navigasjon, men de trenger ikke like dypt innhold som en ren tjenesteside.
- Tenk SEO allerede her — hver side bør ha et tydelig søkeord den sikter mot.
