---
name: kunde-epost
description: Skriv en klar og profesjonell e-post til kunden som forklarer hva som er gjort, hva de bør se etter, og hvordan de gir tilbakemelding. Bruk denne skillen når tjenestesider er ferdige og klare for kundens gjennomgang, eller når noen sier "skriv e-post til kunden", "send til godkjenning", "klar for review".
---

# Kunde-epost

Denne skillen skriver en e-post til kunden som forklarer endringene som er gjort og hva kunden trenger å gjøre for å godkjenne.

## Utgangspunkt

Du trenger:
- Oversikt over hvilke sider som er laget/endret
- Eventuelle åpne spørsmål eller steder der kundens input trengs
- URL til Netlify preview (eller tilsvarende staging-miljø)

## Prosess

### 1. Samle informasjon
Gå gjennom alle notatfiler fra prosessen:
- Utkast-notater (åpne spørsmål, bildebehov)
- Review-notater (eventuelle ting kunden bør vurdere)
- Design-review (eventuelle kompromisser)

### 2. Skriv e-posten
E-posten skal være:
- **Kort og tydelig** — kunder har ikke tid til lange e-poster
- **Handlingsorientert** — tydelig hva kunden trenger å gjøre
- **Strukturert** — lett å skumme

### Mal

```
Emne: Nye tjenestesider klare for gjennomgang — [Bedriftsnavn]

Hei [Kontaktperson],

Vi har laget [X] nye tjenestesider for [bedriftsnavn]. Du finner de her:
[Netlify preview-URL]

Her er hva som er nytt:
- [Side 1] — [kort beskrivelse]
- [Side 2] — [kort beskrivelse]
- ...

Ting vi trenger tilbakemelding på:
1. [spørsmål/punkt som trenger kundens input]
2. ...

Slik gir du tilbakemelding:
- Gå gjennom sidene på lenken over
- [Foretrukket måte å gi feedback — e-post, kommentarer, osv.]
- Tenk spesielt på: Er innholdet riktig? Mangler det noe viktig? Er tonen riktig for dere?

Når dere har gitt tilbakemelding, gjør vi de siste justeringene og publiserer.

Gi gjerne lyd om noe er uklart!

Vennlig hilsen
[Avsender]
Fjellvarden
```

### 3. Tilpass
- Tilpass tone etter kundeforholdet (ny kunde = mer formell, eksisterende = mer uformell)
- Legg til spesifikke punkter basert på denne kundens situasjon
- Hvis det er mange sider, vurder å gruppere eller legge ved en separat oversikt

## Output

E-postteksten klar til å sendes, lagret i `.ai/kunder/[bedriftsnavn]/kommunikasjon/epost-review-[dato].md`.
