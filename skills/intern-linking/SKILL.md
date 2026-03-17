---
name: intern-linking
description: Finn og legg til interne lenker fra eksisterende sider til den nye tjenestesiden, og fra den nye siden til relevante eksisterende sider. Bruk denne skillen når en ny tjenesteside er publisert og trenger å kobles inn i nettstedets lenkestruktur, eller når noen sier "intern lenking", "legg til lenker", "koble sidene sammen".
---

# Intern Linking

Denne skillen sørger for at den nye tjenestesiden er lenket til fra relevante eksisterende sider, og at den nye siden lenker tilbake der det er naturlig.

## Prosess

### 1. Kartlegg eksisterende sider
Gå gjennom nettstedets sider og finn:
- Sider som omtaler samme tjeneste eller relaterte tjenester
- Bloggposter eller artikler som berører temaet
- Kategorisider og oversiktssider
- Forsiden eller landingssider med tjenestelister

### 2. Finn lenkemuligheter
For hver eksisterende side, identifiser:
- Steder der tjenesten nevnes uten å lenke
- Steder der en lenke ville vært naturlig for leseren
- Ankertekst som er relevant og beskrivende (ikke "klikk her")

### 3. Legg til lenker
- Fra eksisterende sider → ny tjenesteside
- Fra ny tjenesteside → relevante eksisterende sider
- Oppdater eventuell meny/navigasjon hvis tjenesten bør synes der

### 4. Valider
- Ingen ødelagte lenker
- Lenketekst er beskrivende og naturlig
- Ikke for mange lenker per avsnitt (1-2 er nok)

## Output

```
# Intern Linking — [Tjeneste]

## Lenker lagt til

### Fra eksisterende sider → ny side
| Side | Ankertekst | Kontekst |
|------|-----------|----------|
| [side-URL] | [ankertekst] | [kort om hvor lenken ble plassert] |

### Fra ny side → eksisterende sider
| Mål | Ankertekst | Kontekst |
|-----|-----------|----------|
| [side-URL] | [ankertekst] | [kort om hvor lenken ble plassert] |

### Navigasjon
- [eventuelle endringer i meny/nav]

## Verifisering
- [ ] Alle nye lenker fungerer
- [ ] Ankertekst er naturlig og beskrivende
- [ ] Ingen side har unormalt mange lenker
```

Lagre i `.ai/kunder/[bedriftsnavn]/review/[tjeneste-slug]-intern-linking.md`.
