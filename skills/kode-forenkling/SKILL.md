---
name: kode-forenkling
description: Rydd opp og forenkle kildekoden til en tjenesteside — fjern duplikater, flytt stiler til globale CSS, og sørg for ren kode. Bruk denne skillen etter design-review, når du trenger å rydde i koden, eller når noen sier "rydd opp koden", "forenkle", "simplify", "kode-cleanup".
---

# Kode-forenkling

Denne skillen rydder opp i kildekoden etter at innhold og design er ferdig. Målet er ren, vedlikeholdbar kode uten duplikater.

## Prosess

### 1. Analyser koden
Les gjennom tjenestesidens kode og identifiser:
- Inline-stiler som burde være i CSS-klasser
- Stiler som dupliserer eksisterende globale stiler
- Komponenter som finnes andre steder og kan gjenbrukes
- Hardkodede verdier som burde bruke variabler/tokens
- Ubrukt kode eller kommentarer

### 2. Sammenlign med eksisterende kode
Se på andre sider i kodebasen:
- Bruker de samme layoutmønstre? Bør det bli en delt komponent?
- Er det CSS som er copy-pastet mellom sider?
- Finnes det et designsystem med tokens/variabler som burde brukes?

### 3. Refaktorer
For hvert funn, vurder:
- **Flytt til global CSS:** Stiler som brukes av 2+ sider
- **Bruk eksisterende komponent:** Ikke lag en ny når det finnes en
- **Trekk ut komponent:** Hvis et mønster gjentar seg og det gir mening
- **Erstatt hardkodede verdier:** Bruk designtokens der de finnes

### 4. Valider
Etter endringer:
- Sjekk at siden fortsatt ser lik ut visuelt
- Kjør eventuelle tester eller linting
- Verifiser at andre sider ikke er påvirket av CSS-endringer

## Output

Oppdatert kode i kodebasen, pluss en endringslogg:

```
# Kode-forenkling — [Tjeneste]

## Endringer
- [fil]: [hva som ble endret og hvorfor]
- ...

## Stiler flyttet til global CSS
- [klasse/stil]: [fra → til]

## Komponenter gjenbrukt
- [komponent]: [brukt i stedet for inline-kode]

## Verifisering
- [ ] Visuelt identisk etter endringer
- [ ] Ingen sideeffekter på andre sider
- [ ] Linting passerer
```

## Viktig

- Ikke refaktorer for refaktoreringens skyld. Hvis koden fungerer og er lesbar, la den stå.
- Vær forsiktig med å flytte stiler til global CSS — sørg for at det ikke påvirker andre sider uventet.
- Små, trygge endringer er bedre enn store omskrivinger.
