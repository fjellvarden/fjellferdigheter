---
name: innhold-polish
description: Fjern AI-skriveri og poler språket til å bli varmt, tydelig og menneskelig. Bruk denne skillen etter innhold-review, når teksten er godkjent innholdsmessig men trenger språklig polering, eller når noen sier "polish teksten", "fjern AI-språk", "gjør det mer menneskelig", "fikse språket".
---

# Innhold Polish

Denne skillen polerer språket i en tjenesteside for å fjerne typiske AI-kjennetegn og gjøre teksten varm, tydelig og menneskelig. Skillen kjøres etter at innholdet er godkjent i **innhold-review**.

## Problemet

AI-generert tekst har gjenkjennelige mønstre som undergraver troverdigheten. Lesere merker det, selv om de ikke kan sette fingeren på hva det er. Denne skillen fjerner disse mønstrene systematisk.

## Sjekkliste for AI-skriveri

Gå gjennom teksten og fjern/endre følgende:

### Tegnsetting
- ❌ Emdash (—) — erstatt med komma, punktum, eller omskriv setningen
- ❌ Overdreven bruk av kolon for å introdusere lister
- ❌ Semikolon der punktum fungerer bedre

### Setningsstruktur
- ❌ Setninger som er jevnlangt hele veien — variér! Korte. Og litt lengre setninger som gir rom til å puste.
- ❌ Samme setningsstruktur gjentatt (subjekt-verb-objekt, subjekt-verb-objekt)
- ❌ Oppramsinger av tre ting overalt ("profesjonell, pålitelig og effektiv")

### Ordvalg
- ❌ "I en verden der..."
- ❌ "Med vår ekspertise..."
- ❌ "Sømløs" / "sømløst"
- ❌ "Omfattende" brukt som fyllord
- ❌ "Robust" om noe som ikke er fysisk
- ❌ "Banebrytende" / "innovativ" uten konkret innhold
- ❌ "Unik" om noe som ikke er unikt
- ❌ "Helhetlig" / "holistisk"
- ❌ "Ta det til neste nivå"
- ❌ Overdreven bruk av adjektiver — maks 1-2 per avsnitt
- ❌ "Ikke bare... men også..."
- ❌ "Enten du er... eller..."

### Struktur
- ❌ Hvert avsnitt starter med en temasetning som oppsummerer innholdet
- ❌ Avsnitt som alle er like lange
- ❌ Overskrifter som alle følger samme mønster

### Stemme
- ❌ Passiv form der aktiv fungerer ("tjenesten leveres" → "vi leverer")
- ❌ Formelt bedriftsspråk der vanlig norsk fungerer
- ❌ Distansert tone ("man bør vurdere" → "tenk på")

## Hva du erstatter med

### Godt norsk
- Bruk dagligdagse ord. "Bytte" er bedre enn "erstatte". "Fikse" er bedre enn "utbedre".
- Skriv som du snakker til en venn som spør om tjenesten — ikke som en brosjyre.
- Korte, aktive setninger. "Vi bytter varmtvannsberederen din på én dag." er bedre enn "Våre fagfolk sørger for en effektiv utskifting av din varmtvannsbereder."

### Variasjon
- Bland korte og lange setninger
- Bland korte og lange avsnitt
- La noen avsnitt starte med et spørsmål
- Bruk av og til ufullstendige setninger for rytme. Som denne.

### Menneskelighet
- Vis at det er mennesker bak teksten
- Bruk "vi" og "du" naturlig
- Det er OK å være litt uformell — tjenestesider er ikke akademiske tekster
- Legg inn konkrete detaljer fremfor generelle påstander

## Prosess

1. Les gjennom hele teksten først uten å endre noe
2. Gå gjennom sjekklisten punkt for punkt
3. Gjør endringene direkte i filen
4. Les gjennom igjen med friske øyne — flyter det?
5. Presenter endringene for brukeren som en diff eller oppsummering

## Output

Den oppdaterte tjenestesiden i kodebasen, pluss en kort endringslogg:

```
# Polish-logg — [Tjeneste]

## Endringer gjort
- [type endring]: [eksempel før → etter]
- ...

## Sjekkliste
- [x] Emdash fjernet
- [x] Setningslengde variert
- [x] AI-ord fjernet
- [x] Tone sjekket
- ...
```

## Viktig

- Polish betyr ikke omskriving. Behold budskapet og strukturen fra reviewen.
- SEO-søkeordene må fortsatt være med — ikke poler dem bort.
- Noen ganger er den enkleste endringen den beste. Hvis en setning fungerer, la den stå.
- Les høyt. Hvis det høres stivt ut når du leser det høyt, skriv det om.
