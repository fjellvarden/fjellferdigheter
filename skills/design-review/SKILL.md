---
name: design-review
description: Visuell gjennomgang av tjenestesidens layout og design ved hjelp av nettleser eller skjermbilder. Bruk denne skillen når en tjenesteside er ferdig kodet og du trenger å sjekke at den ser bra ut visuelt, eller når noen sier "sjekk designet", "hvordan ser det ut", "layout-sjekk", "visuell review".
---

# Design Review

Denne skillen gjennomgår det visuelle uttrykket på en ferdig kodet tjenesteside. Målet er å fange layoutproblemer, designinkonsistenser og UX-svakheter før siden sendes til kunden.

## Utgangspunkt

Du trenger:
- En ferdig kodet tjenesteside som kan vises i nettleser
- Tilgang til kundens designsystem eller eksisterende sider for sammenligning

## Prosess

### 1. Sett opp visning
Bruk Playwright, Chrome, eller et skjermbildeverktøy for å se siden:
- Desktop (1440px bredde)
- Tablet (768px bredde)
- Mobil (375px bredde)

Ta skjermbilder av hele siden på alle tre bredder.

### 2. Sjekk layout
For hvert breakpoint, vurder:
- Er spacing konsistent? (marginer, padding, mellom seksjoner)
- Er tekst lesbar? (fontstørrelse, linjehøyde, kontrastforhold)
- Flyter innholdet naturlig nedover siden?
- Er det nok "luft" — eller er det trangt og klemt?
- Fungerer bilder/media godt i layout?

### 3. Sjekk konsistens
Sammenlign med eksisterende sider på samme nettsted:
- Matcher fargebruk, typografi og spacing?
- Er knapper og CTA-er konsistente med resten av siden?
- Følger komponenter samme mønster som på andre sider?
- Er header og footer intakt?

### 4. Sjekk UX
- Er CTA synlig uten å scrolle (above the fold)?
- Er kontaktinfo lett å finne?
- Fungerer navigasjonen?
- Er scanbarhet god? (kan man forstå sidens innhold ved å skumme overskriftene?)
- Er det nok visuell variasjon, eller ser hele siden lik ut fra topp til bunn?

### 5. Sjekk tilgjengelighet
- Har bilder alt-tekst?
- Er kontrastforholdet tilstrekkelig (WCAG AA)?
- Fungerer siden med tastaturnavigasjon?
- Er overskriftshierarkiet korrekt (H1 → H2 → H3)?

## Output

```
# Design Review — [Tjeneste]

## Overordnet inntrykk
[2-3 setninger om helheten]

## Desktop
- ✅ / ⚠️ [funn]

## Tablet
- ✅ / ⚠️ [funn]

## Mobil
- ✅ / ⚠️ [funn]

## Konsistens med resten av nettsiden
- ✅ / ⚠️ [funn]

## UX
- ✅ / ⚠️ [funn]

## Tilgjengelighet
- ✅ / ⚠️ [funn]

## Konkrete endringer å gjøre
1. [endring med skjermbilde-referanse]
2. ...

## Skjermbilder
[lenker eller referanser til skjermbildene]
```

Lagre i `.ai/kunder/[bedriftsnavn]/review/[tjeneste-slug]-design-review.md`.

## Verktøy

Denne skillen fungerer best med:
- **Playwright** — automatisert skjermbildetaking og interaksjonstesting
- **Chrome DevTools** — manuell inspeksjon av layout og responsivitet
- **Lighthouse** — tilgjengelighets- og ytelsessjekk

Hvis ingen av disse er tilgjengelig, be brukeren om skjermbilder og gjør reviewen basert på de.
