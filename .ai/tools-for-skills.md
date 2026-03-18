# Verktøy som kan forbedre skills

Oversikt over verktøy, API-er og integrasjoner som ville gjort hver skill bedre. Disse er ikke laget ennå — dette er en ønskeliste for fremtidig utvikling.

---

## SEO-verktøy

### DataForSEO API
**Relevant for:** `seo-research`, `seo-metadata`, `tjenestelister`, `innhold-research`
**Hva det gir oss:**
- Søkevolum og keyword difficulty for norske søkeord
- Konkurrents organiske søkeord og trafikk
- SERP-analyse (hvem rangerer på hva)
- Relaterte søkeord og "People Also Ask"
- Google SERP-resultater for spesifikke søk
- Google autocomplete-forslag
- Google Maps-resultater (viktig for lokale tjenester)
**Prioritet:** Høy — dette er den viktigste manglende brikken for datadrevet innhold.

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

**📁 Lagring av crawlet innhold:**

Hver crawlet side lagres som en markdown-fil. Standard plassering er `.ai/research/` på root i kundeprosjektet, organisert per tjeneste:

```
<prosjekt-root>/
└── .ai/
    └── research/
        ├── <tjeneste-slug>/
        │   ├── konkurrent-1-tjenesteside.md
        │   ├── konkurrent-2-tjenesteside.md
        │   └── underleveranser/
        │       ├── energiberegning-kilde-1.md
        │       └── varmekilder-kilde-2.md
        └── <annen-tjeneste-slug>/
            └── ...
```

Hver markdown-fil skal ha frontmatter med metadata:
```markdown
---
url: https://example.com/tjeneste
domain: example.com
crawled: 2026-03-18
tjeneste: vannbåren-varme
type: konkurrent | fagressurs | bransjeinfo
---

# Sidetittel

[Innhold konvertert til ren markdown...]
```

Hvis en skill kjøres med en spesifikk promptfil eller arbeidsmappe, lagres research-data ved siden av den filen i en `research/`-undermappe. Ellers faller den tilbake til `.ai/research/` på prosjektroot.

**⚠️ Anti-blokkering — viktig oppsett:**

CloudFront, Cloudflare og lignende CDN/WAF-tjenester blokkerer ofte forespørsler som ser ut som automatiserte crawlere. For å unngå dette:

**1. Realistisk User-Agent:**
Sett alltid en oppdatert, ekte nettleser User-Agent. Unngå standardverdier som `python-requests` eller `HeadlessChrome`.
```
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/125.0.0.0 Safari/537.36
```
Roter gjerne mellom 3–5 ulike User-Agents (Chrome, Firefox, Safari) for å unngå fingerprinting.

**2. Playwright-konfigurasjon (anbefalt):**
```javascript
const browser = await playwright.chromium.launch({
  headless: true,
  args: [
    '--disable-blink-features=AutomationControlled', // Fjerner navigator.webdriver=true
    '--no-sandbox',
  ]
});
const context = await browser.newContext({
  userAgent: 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/125.0.0.0 Safari/537.36',
  viewport: { width: 1920, height: 1080 },
  locale: 'nb-NO',
  timezoneId: 'Europe/Oslo',
  // Sett ekte skjerm-properties
  deviceScaleFactor: 1,
  hasTouch: false,
});
```

**3. HTTP-headers som matcher en ekte nettleser:**
```
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: nb-NO,nb;q=0.9,no;q=0.8,en-US;q=0.7,en;q=0.6
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Sec-Fetch-User: ?1
```
Disse headerne er kritiske — CloudFront sjekker ofte `Sec-Fetch-*` headers, og manglende headers er et tydelig crawler-signal.

**4. Rate limiting og oppførsel:**
- Vent 2–5 sekunder mellom forespørsler (randomisert, ikke fast intervall)
- Besøk forsiden først, deretter naviger til undersider (simuler naturlig browsing)
- Hold cookies/session mellom requests (CloudFront setter ofte test-cookies)
- Respekter `robots.txt` — dette er etisk scraping av offentlig tilgjengelig innhold

**5. Fallback-strategi ved blokkering:**
- Prøv igjen med en annen User-Agent etter 30 sekunder
- Bruk Google Cache (`cache:url`) som alternativ kilde
- Bruk DataForSEO SERP API for å hente cached versjoner av sider
- Som siste utvei: bruk en proxy-tjeneste (f.eks. ScraperAPI, Bright Data)

**6. Playwright stealth-plugins:**
Vurder `playwright-extra` med `stealth`-plugin som automatisk patcher mange av de vanligste deteksjonsmekanismene (WebGL, canvas fingerprinting, navigator.plugins osv).

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

## Miljøvariabler og oppsett

Alle API-nøkler og credentials lagres i `.env` på prosjektroot (gitignored). Se `.env.example` for dokumentasjon.

| Variabel | Tjeneste | Brukes av skills | Skaff her |
|----------|----------|------------------|-----------|
| `DATAFORSEO_LOGIN` | DataForSEO | seo-research, seo-metadata, tjenestelister, innhold-research | [dataforseo.com](https://dataforseo.com/) → Dashboard → API Access |
| `DATAFORSEO_PASSWORD` | DataForSEO | (samme som over) | (samme som over) |
| `SCRAPER_PROXY_URL` | Proxy (valgfri) | tjenestelister, innhold-research | ScraperAPI, Bright Data e.l. |
| `COPYSCAPE_USERNAME` | Copyscape | innhold-review | [copyscape.com/apiconfigure.php](https://www.copyscape.com/apiconfigure.php) |
| `COPYSCAPE_API_KEY` | Copyscape | innhold-review | (samme som over) |
| `GOOGLE_PAGESPEED_API_KEY` | Google Cloud | design-review, seo-metadata, kode-forenkling | [Google Cloud Console](https://console.cloud.google.com/apis/credentials) — aktiver PageSpeed Insights API |
| `FJELLVARDEN_OS_API_URL` | Fjellvarden OS | tjeneste-gruppering, pipeline | Intern |
| `FJELLVARDEN_OS_API_KEY` | Fjellvarden OS | (samme som over) | Intern |
| `RESEND_API_KEY` | Resend | kunde-epost | [resend.com](https://resend.com/) |
| `NETLIFY_AUTH_TOKEN` | Netlify | pipeline | [Netlify User Settings](https://app.netlify.com/user/applications#personal-access-tokens) |
| `NETLIFY_SITE_ID` | Netlify | pipeline | Netlify dashboard for aktuelt site |

**Minstekrav for å komme i gang:** `DATAFORSEO_LOGIN` + `DATAFORSEO_PASSWORD`. Alt annet er valgfritt og kan legges til etter behov.

---

## Oppsummering — prioritert rekkefølge

| # | Verktøy | Påvirker skills | Prioritet |
|---|---------|-----------------|-----------|
| 1 | DataForSEO API | seo-research, seo-metadata, tjenestelister | Høy |
| 2 | Web Scraping (Playwright) | tjenestelister, innhold-research, design-review | Høy |
| 3 | Playwright MCP | design-review, seo-metadata | Høy |
| 4 | Fjellvarden OS API | tjeneste-gruppering, pipeline | Medium |
| 5 | Lighthouse API | design-review, seo-metadata, kode-forenkling | Medium |
| 6 | Plagiatsjekk | innhold-review | Medium |
| 7 | Google Trends | seo-research | Lav-medium |
| 8 | Netlify API | pipeline | Medium |
| 9 | E-post-sending | kunde-epost | Lav |
