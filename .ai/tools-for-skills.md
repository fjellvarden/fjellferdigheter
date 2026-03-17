# Verktøy som kan forbedre skills

Oversikt over verktøy, API-er og integrasjoner som ville gjort hver skill bedre. Disse er ikke laget ennå — dette er en ønskeliste for fremtidig utvikling.

---

## SEO-verktøy

### DataForSEO API
**Relevant for:** `seo-research`, `seo-metadata`, `tjenestelister`
**Hva det gir oss:**
- Søkevolum og keyword difficulty for norske søkeord
- Konkurrents organiske søkeord og trafikk
- SERP-analyse (hvem rangerer på hva)
- Relaterte søkeord og "People Also Ask"
- Backlink-data

**Prioritet:** Høy — dette er den viktigste manglende brikken for datadrevet innhold.

### SerpApi
**Relevant for:** `seo-research`, `innhold-research`
**Hva det gir oss:**
- Google SERP-resultater for spesifikke søk
- "People Also Ask"-spørsmål
- Google autocomplete-forslag
- Google Maps-resultater (viktig for lokale tjenester)

**Prioritet:** Medium — overlapper delvis med DataForSEO, men gir raskere SERP-snapshots.

### Google Trends API
**Relevant for:** `seo-research`
**Hva det gir oss:**
- Sesongvariasjon i søkeinteresse (f.eks. varmepumpe-søk peaker om høsten)
- Regionale forskjeller i søkeinteresse
- Trendanalyse over tid

**Prioritet:** Lav-medium — nyttig for timing og vinkling, men ikke kritisk.

---

## Innholds- og research-verktøy

### Web Scraping / Crawling
**Relevant for:** `tjenestelister`, `innhold-research`
**Hva det gir oss:**
- Automatisk scraping av konkurrenters tjenestesider
- Strukturert data fra nettsider (tjenester, priser, beskrivelser)
- Bulk-innhenting av innhold for research

**Implementering:** MCP-server med Playwright eller Puppeteer for JavaScript-rendrede sider. Eventuelt en enklere HTTP-basert scraper for statiske sider.

**Prioritet:** Høy — uten dette må research gjøres manuelt.

### Plagiatsjekk-verktøy
**Relevant for:** `innhold-review`
**Hva det gir oss:**
- Automatisk sjekk av tekstlikhet mot kilder
- Prosentvis overlapp med publisert innhold
- Flagging av passasjer som er for like

**Implementering:** API som Copyscape eller en lokal tekst-sammenligningsalgoritme.

**Prioritet:** Medium — kan gjøres manuelt ved å sammenligne med research-kilder, men automatisering sparer tid.

---

## Design- og kodeverktøy

### Playwright / Browser Automation
**Relevant for:** `design-review`, `seo-metadata`
**Hva det gir oss:**
- Automatisk skjermbildetaking på ulike skjermstørrelser
- Visuell regresjonstesting
- Tilgjengelighetssjekk
- Automated Lighthouse-kjøring

**Implementering:** MCP-server som wrapper rundt Playwright.

**Prioritet:** Høy — gjør design-review mye mer effektiv og pålitelig.

### Lighthouse / PageSpeed API
**Relevant for:** `design-review`, `seo-metadata`, `kode-forenkling`
**Hva det gir oss:**
- Performance-score
- Tilgjengelighets-score
- SEO-score
- Best practices-sjekk
- Core Web Vitals

**Prioritet:** Medium — nyttig for kvalitetssikring, men kan også kjøres manuelt.

### Google Rich Results Test API
**Relevant for:** `seo-metadata`
**Hva det gir oss:**
- Validering av schema markup
- Forhåndsvisning av hvordan siden vises i Google

**Prioritet:** Medium — viktig for SEO, men kan også sjekkes manuelt.

---

## Prosjektstyringsverktøy

### Fjellvarden OS / SOP-integrasjon
**Relevant for:** `tjeneste-gruppering`, `tjenesteside-pipeline`
**Hva det gir oss:**
- Automatisk oppretting av oppgaver i kundens oppgaveliste
- Statusoppdatering når sider er ferdige
- Sporing av hele pipelinen per kunde

**Implementering:** API-integrasjon mot Fjellvarden OS.

**Prioritet:** Medium — sparer manuell oppgaveopprettelse, men ikke kritisk for innholdskvalitet.

---

## Kommunikasjonsverktøy

### E-post-sending
**Relevant for:** `kunde-epost`
**Hva det gir oss:**
- Direkte sending av e-post fra pipelinen
- Sporing av om kunden har åpnet/lest

**Implementering:** SMTP-integrasjon eller tjeneste som Resend/Postmark.

**Prioritet:** Lav — e-posten kan enkelt kopieres og sendes manuelt.

---

## Deployment-verktøy

### Netlify API
**Relevant for:** `tjenesteside-pipeline`
**Hva det gir oss:**
- Automatisk deploy til preview-branch
- Generering av preview-URL for kunden
- Statussjekk på build

**Implementering:** MCP-server eller enkel CLI-wrapper.

**Prioritet:** Medium — forenkler leveranseprosessen.

---

## Oppsummering — prioritert rekkefølge

| # | Verktøy | Påvirker skills | Prioritet |
|---|---------|-----------------|-----------|
| 1 | DataForSEO API | seo-research, seo-metadata, tjenestelister | Høy |
| 2 | Web Scraping (Playwright) | tjenestelister, innhold-research, design-review | Høy |
| 3 | Playwright MCP | design-review, seo-metadata | Høy |
| 4 | SerpApi | seo-research, innhold-research | Medium |
| 5 | Fjellvarden OS API | tjeneste-gruppering, pipeline | Medium |
| 6 | Lighthouse API | design-review, seo-metadata, kode-forenkling | Medium |
| 7 | Plagiatsjekk | innhold-review | Medium |
| 8 | Google Trends | seo-research | Lav-medium |
| 9 | Netlify API | pipeline | Medium |
| 10 | E-post-sending | kunde-epost | Lav |
