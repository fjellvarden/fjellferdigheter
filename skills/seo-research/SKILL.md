---
name: seo-research
description: Innhent SEO-data — søkeord, søkevolum, spørsmål folk stiller, og konkurrentenes trafikkdata. Bruk denne skillen når du trenger søkeordanalyse for en tjeneste, når noen sier "finn søkeord", "SEO-analyse", "hva søker folk etter", eller som forberedelse til å skrive tjenestesider.
---

# SEO Research

Denne skillen samler inn SEO-data som brukes til å forme innholdet på tjenestesider. Du finner ut hva folk faktisk søker etter, hvilke spørsmål de stiller, og hva konkurrentene rangerer på.

## Utgangspunkt

Du trenger:
- Tjenesten/temaet du analyserer
- Kundens bransje og lokasjon
- Liste over konkurrenter (fra **tjenestelister**)

## Prosess

### 1. Søkeordanalyse
Finn relevante søkeord for tjenesten:

- **Hovedsøkeord** — det mest åpenbare søket (f.eks. "rørlegger Oslo")
- **Long-tail søkeord** — mer spesifikke søk (f.eks. "bytte varmtvannsbereder pris")
- **Spørsmålssøk** — "hva koster...", "hvordan...", "når bør man..."
- **Lokale søk** — søkeord med stedsnavn

For hvert søkeord, noter:
- Estimert søkevolum (hvis tilgjengelig via verktøy)
- Konkurranse/vanskelighetsgrad
- Søkeintenjon (informasjon, kjøp, sammenligning)

### 2. Konkurrentanalyse
For de viktigste konkurrentene, finn ut:
- Hvilke søkeord rangerer de på?
- Hvilke sider får mest organisk trafikk?
- Hvilke søkeord har de "featured snippets" på?
- Hva mangler de som kunden kan fylle?

### 3. Spørsmål folk stiller
Samle reelle spørsmål fra:
- Google "People Also Ask" (PAA)
- Google autocomplete-forslag
- Forum og Q&A-sider
- Google Trends for sesongvariasjon

### 4. Innholdsgap
Identifiser muligheter der:
- Det søkes mye, men få gode svar finnes
- Konkurrentene har svakt innhold på viktige søkeord
- Lokale søk mangler gode resultater

## Output

```
# SEO Research — [Tjeneste]

## Hovedsøkeord
| Søkeord | Volum | Konkurranse | Intensjon |
|---------|-------|-------------|-----------|
| ... | ... | ... | ... |

## Long-tail søkeord
[samme format]

## Spørsmål folk stiller
1. [spørsmål] — [estimert volum/interesse]
2. ...

## Konkurrentenes posisjon
| Konkurrent | Toppsøkeord | Estimert trafikk | Styrker | Svakheter |
|------------|-------------|------------------|---------|-----------|
| ... | ... | ... | ... | ... |

## Innholdsgap og muligheter
- [mulighet 1]
- [mulighet 2]

## Anbefaling
- **Primært søkeord for siden:** [søkeord]
- **Sekundære søkeord:** [liste]
- **Spørsmål å besvare i innholdet:** [topp 5-10]
- **Vinkling:** [anbefalt vinkling basert på data]
```

Lagre i `.ai/kunder/[bedriftsnavn]/research/[tjeneste-slug]/seo-data.md`.

## Tilgjengelige verktøy

Denne skillen fungerer best med tilgang til SEO-verktøy. Sjekk om noen av disse er tilgjengelig:
- **DataForSEO API** — søkevolum, konkurrentdata, SERP-analyse
- **SerpApi** — Google SERP-data, PAA, autocomplete
- **Google Trends** — sesongdata og trender

Hvis ingen verktøy er tilgjengelig, bruk manuelle søk og estimer basert på tilgjengelig informasjon. Marker tydelig hva som er estimert vs. datadrevet.

## Viktig

- SEO-data er et middel, ikke et mål. Poenget er å forstå hva folk faktisk lurer på slik at vi kan lage innhold som svarer på det.
- Ikke optimaliser for søkemotorer på bekostning av lesbarhet. Skriv for mennesker først.
- Lokale søk er ofte viktigere enn nasjonale for tjenesteleverandører.
