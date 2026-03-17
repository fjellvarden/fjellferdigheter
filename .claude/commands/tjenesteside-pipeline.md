Kjør hele tjenesteside-pipelinen for en kunde. Denne kommandoen styrer prosessen fra start til slutt med minimal input.

## Stegene i pipelinen

Følg disse stegene i rekkefølge. Hvert steg har en egen skill — bruk den. Vent på godkjenning der det er markert med ⏸️.

### Fase 1: Kartlegging (krever kundeinteraksjon)

1. **Kunde-intervju** ⏸️
   Bruk `kunde-intervju`-skillen. Samle inn info om virksomheten, tjenester, konkurrenter og målgruppe. Vent på kundens svar.

2. **Tjenestelister**
   Bruk `tjenestelister`-skillen. Research bransjen og bygg en komplett tjenesteliste basert på intervjuet.

3. **Tjeneste-gruppering** ⏸️
   Bruk `tjeneste-gruppering`-skillen. Grupper tjenestene og foreslå sidestruktur. Be om godkjenning av strukturen og oppgavelisten.

---
⚡ Herfra kan pipelinen kjøre mer automatisk, side for side.

### Fase 2: Per tjenesteside (gjenta for hver side i prioritert rekkefølge)

4. **Innhold-research**
   Bruk `innhold-research`-skillen. Samle kilder og faginnhold for denne spesifikke tjenesten.

5. **SEO Research**
   Bruk `seo-research`-skillen. Finn søkeord, spørsmål og konkurrentdata. (Kan kjøres parallelt med steg 4.)

6. **Outline Review** ⏸️
   Bruk `outline-review`-skillen. Lag artikkeloutline og be om godkjenning før du skriver.

7. **Tjenesteside-utkast**
   Bruk `tjenesteside-utkast`-skillen. Skriv første utkast basert på godkjent outline, research og SEO-data.

8. **Innhold Review**
   Bruk `innhold-review`-skillen. Kvalitetsjekk innholdet — plagiat, fakta, kundereise, målgrupper.

9. **Innhold Polish**
   Bruk `innhold-polish`-skillen. Fjern AI-skriveri og poler språket.

10. **Design Review**
    Bruk `design-review`-skillen. Sjekk visuelt at siden ser bra ut på desktop, tablet og mobil.

11. **Kode-forenkling**
    Bruk `kode-forenkling`-skillen. Rydd opp i koden — fjern duplikater, bruk globale stiler.

12. **SEO Metadata**
    Bruk `seo-metadata`-skillen. Legg til schema markup, title tags, meta descriptions.

13. **Intern Linking**
    Bruk `intern-linking`-skillen. Koble den nye siden inn i nettstedets lenkestruktur.

### Fase 3: Levering

14. **Kunde-epost**
    Bruk `kunde-epost`-skillen. Skriv e-post med oversikt over endringene og lenke til staging/preview.

15. **Deploy til staging**
    Push til en Netlify preview branch slik at kunden kan se endringene.

## Kjøremodus

- **Full pipeline:** Kjør alle steg fra 1. Bruk dette for helt nye kunder.
- **Ny tjenesteside:** Start fra steg 4 (research) for en eksisterende kunde som allerede har kundeprofil og sidestruktur.
- **Forbedre eksisterende side:** Start fra steg 7 (utkast) eller 8 (review) avhengig av hva som trengs.

Spør brukeren hvilken modus de ønsker, eller detekter det basert på hva som allerede finnes i `.ai/kunder/`-mappen.
