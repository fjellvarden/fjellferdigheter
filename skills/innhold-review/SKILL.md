---
name: innhold-review
description: Kvalitetsjekk av tjenestesideinnhold — plagiat, fakta, kundereise, og målgruppetreffsikkerhet. Bruk denne skillen etter at et utkast er skrevet og du trenger å kvalitetssikre innholdet, eller når noen sier "sjekk innholdet", "kvalitetsjekk", "review teksten", "er dette bra nok".
---

# Innhold Review

Denne skillen kvalitetssikrer et tjenestesideutkast ved å sjekke det fra flere vinkler: plagiat, faktasjekk, kundereise, og om innholdet treffer målgruppen bredt nok.

## Utgangspunkt

Du trenger:
- Tjenestesiden (utkastet fra **tjenesteside-utkast**)
- Research-mappen med originalkilder (fra **innhold-research**)
- Godkjent outline med primærpersona og vinkling (fra **outline-review**)

## Prosess

### 1. Plagiatsjekk
Sammenlign tjenestesiden med kildene i research-mappen:
- Er det setninger eller avsnitt som er for like originalkilden?
- Er formuleringer omskrevet nok, eller er det bare synonymbytte?
- Flagg alt som er for tett på en kilde og foreslå omskriving.

### 2. Faktasjekk
Gå gjennom alle påstander i teksten:
- Er priser og tall korrekte og oppdaterte?
- Er tekniske beskrivelser riktige?
- Er det påstander som ikke kan underbygges av kildene?
- Er innholdet evergreen, eller vil det fort bli utdatert? (f.eks. "i 2024" bør erstattes med noe tidløst)
- Flagg usikre påstander med forslag til forbedring.

### 3. Kundereise-sjekk
Vurder om innholdet følger en naturlig kundereise:
- **Gjenkjennelse:** Forstår leseren innen 5 sekunder at dette er relevant for dem?
- **Forståelse:** Er tjenesten forklart tydelig nok til at en ikke-fagperson forstår?
- **Tillit:** Bygger innholdet troverdighet? (fakta, prosess, ekspertise)
- **Handling:** Er CTA tydelig og naturlig plassert?

Er det steder der kundereisen bryter? Hopper teksten fra "hva er dette" rett til "kontakt oss" uten å bygge forståelse?

### 4. Rollebasert gjennomlesning
Les teksten fra perspektivet til ulike lesere og noter hva som mangler eller støter:

**Kritisk kunde:** "Hvorfor skal jeg velge dere? Hva skiller dere fra konkurrentene?"
- Er det nok differensiering?
- Svarer teksten på innvendinger?

**Førstegangskjøper:** "Jeg vet lite om dette — skjønner jeg hva som skjer?"
- Er fagbegreper forklart?
- Er prosessen tydelig?

**Prisbevisst kunde:** "Hva koster dette, og er det verdt det?"
- Er prisinfo tilgjengelig og ærlig?
- Kommuniseres verdien godt nok?

**Hastekunde:** "Jeg trenger dette nå — hvordan kommer jeg i gang?"
- Er kontaktinfo og CTA lett å finne?
- Er viktig info scanbar uten å lese alt?

### 5. Kuttevurdering
Hemingway-prinsippet: "Write drunk, edit sober." Gå gjennom utkastet og spør:
- Hva kan fjernes uten å tape verdi?
- Er det gjentakelser?
- Er det avsnitt som ikke tilfører noe for leseren?

Ikke kutt selv — foreslå hva som kan kuttes og forklar hvorfor.

## Output

```
# Innhold Review — [Tjeneste]

## Plagiatsjekk
- ✅ / ⚠️ [funn per seksjon]

## Faktasjekk
- ✅ / ⚠️ [funn per påstand]

## Kundereise
- Gjenkjennelse: ✅ / ⚠️
- Forståelse: ✅ / ⚠️
- Tillit: ✅ / ⚠️
- Handling: ✅ / ⚠️

## Rollebasert feedback
- **Kritisk kunde:** [funn]
- **Førstegangskjøper:** [funn]
- **Prisbevisst:** [funn]
- **Hastekunde:** [funn]

## Foreslåtte kutt
- [seksjon/avsnitt] — [begrunnelse]

## Konkrete endringer å gjøre
1. [endring med begrunnelse]
2. ...

## Helhetsvurdering
[1-2 setninger om helheten — er dette klart for polish, eller trenger det omskriving?]
```

Lagre i `.ai/kunder/[bedriftsnavn]/review/[tjeneste-slug]-review.md`.
