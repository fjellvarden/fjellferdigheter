---
name: seo-metadata
description: Siste SEO-sjekk — legg til og valider schema markup, title tags, meta descriptions og annen teknisk SEO. Bruk denne skillen når en tjenesteside er ferdig og du trenger å sette opp metadata, eller når noen sier "SEO metadata", "schema markup", "title tag", "meta description", "teknisk SEO".
---

# SEO Metadata

Denne skillen legger til og validerer all teknisk SEO-metadata for en tjenesteside. Den kjøres mot slutten av prosessen, når innholdet er ferdig.

## Utgangspunkt

Du trenger:
- Ferdig tjenesteside i kodebasen
- SEO-data med primær- og sekundærsøkeord (fra **seo-research**)
- Kundens domene og eksisterende metadata-mønstre

## Prosess

### 1. Title tag
- Inneholder primærsøkeord
- Under 60 tegn
- Følger kundens eksisterende mønster (f.eks. "Tjeneste | Bedriftsnavn")
- Er unik — ikke lik andre siders titler

### 2. Meta description
- Inneholder primærsøkeord naturlig
- 120-155 tegn
- Inkluderer en handling eller verdiforslag
- Er engasjerende nok til å klikke på i søkeresultatene

### 3. Schema markup (JSON-LD)
Legg til relevant strukturert data:

**Service schema** (for tjenestesider):
```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "name": "[tjenestenavn]",
  "provider": {
    "@type": "LocalBusiness",
    "name": "[bedriftsnavn]",
    "address": { ... }
  },
  "areaServed": "[område]",
  "description": "[kort beskrivelse]"
}
```

**FAQ schema** (hvis siden har spørsmål/svar):
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "[spørsmål]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[svar]"
      }
    }
  ]
}
```

**BreadcrumbList** (for navigasjon):
```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [...]
}
```

### 4. Open Graph og social
- `og:title` — sidetittel (kan avvike fra title tag)
- `og:description` — kort beskrivelse
- `og:image` — relevant bilde hvis tilgjengelig
- `og:type` — "website"

### 5. Teknisk sjekk
- Canonical URL er satt riktig
- Ingen noindex/nofollow (med mindre tilsiktet)
- Hreflang hvis relevant (flerspråklige sider)
- Bildene har alt-tekst med relevante søkeord
- Overskriftshierarki er korrekt (kun én H1)

## Output

Oppdatert kode i kodebasen, pluss en rapport:

```
# SEO Metadata — [Tjeneste]

## Title tag
[tittel] — [X tegn]

## Meta description
[beskrivelse] — [X tegn]

## Schema markup
- [x] Service
- [x] FAQ (X spørsmål)
- [x] BreadcrumbList

## Open Graph
- [x] title, description, image, type

## Teknisk sjekk
- [x] Canonical URL
- [x] Alt-tekst på bilder
- [x] Overskriftshierarki
- [x] Ingen noindex

## Validering
- [ ] Testet med Google Rich Results Test
- [ ] Testet med Facebook Sharing Debugger
```

Lagre i `.ai/kunder/[bedriftsnavn]/review/[tjeneste-slug]-seo-metadata.md`.
