# Eksternt regelgrunnlag for anbudsprosesser

Status: forskningsgrunnlag  
Kartleggingsdato: 2026-06-11  
Scope: offentlige/kommunale anskaffelser, med vekt på bygg, anlegg og eiendom

Dette området samler eksterne kilder om anbudsprosesser og offentlige anskaffelser. Det er laget som fundament for en senere regelbok og en eventuell LLM-dommer som kan kvalitetssikre tilbudstekster.

Dette er ikke juridisk rådgivning, ikke en komplett kravmatrise og ikke en kontroll av lokale anbudsdokumenter.

## Innhold

- `agent-briefs.md` beskriver foreslåtte subagenter, søkeområder og arbeidsregler.
- `source-cards.csv` er maskinlesbare kildekort med tema, kilde, praktisk betydning, risiko og fagverifisering.
- `source-cards.md` er en lesbar oversikt over de samme kildene og de viktigste kontrollpunktene.
- `rulebook.md` gjør kildekortene om til operative kontrollregler for anbud.
- `llm-judge-rubric.yaml` definerer hard-fail gates, scoring og outputskjema for en LLM-dommer.
- `tender-check-template.md` er en rapportmal for fremtidig kontroll av konkrete anbudsdokumenter.

## Bruksregler

- Bruk kortene som kildeindeks, ikke som juridisk konklusjon.
- Kontroller alltid gjeldende tekst i Lovdata, Doffin/TED, DFØ eller annen primærkilde før en regel brukes i tilbud.
- Knytt alltid regelvurdering til konkret konkurransegrunnlag, kunngjøringstidspunkt, terskelverdi, kontraktstype og prosedyre.
- KOFA-saker, NOU-er og forskningskilder skal brukes som praksis- eller bakgrunnskilder, ikke som selvstendig fasit.
- Betalte standarder fra Standard Norge skal bare refereres på overordnet nivå. Ikke gjengi standardtekst uten rettighet.
- Alle juridiske, anskaffelsesrettslige, tekniske og kontraktsmessige vurderinger må fagverifiseres før ekstern bruk.

## Særskilt versjonsmarkering

Flere anskaffelsesregler endres rundt 2026-07-01. Kildekort med `change_marker = 2026-07-01` må behandles som versjonsfølsomme:

- Kartleggingen er gjort 2026-06-11.
- 2026-07-01 var fremtidig på kartleggingstidspunktet.
- Konkurranser kunngjort før og etter 2026-07-01 kan måtte vurderes etter ulike regelversjoner.
- DFØ opplyser at innslagspunktet økes fra 100 000 kroner ekskl. mva. til 500 000 kroner ekskl. mva. fra 2026-07-01, men konkrete konkurranser må kontrolleres mot gjeldende regelverk og overgangsregler.

## Kildehierarki for senere regelbok

1. Lovdata og vedtatte lover/forskrifter.
2. Regjeringen/NFD for ikrafttredelse, forarbeider og departementskilder.
3. Doffin/TED/eForms for konkrete kunngjøringer og tekniske kunngjøringsdata.
4. DFØ/Anskaffelser.no for veiledning, maler, prosess og praktiske kontrollpunkter.
5. KOFA og domstoler for praksis, alltid lest opp mot faktum.
6. Arbeidstilsynet, DIBK og Standard Norge for BAE, SHA/HMS, TEK17, produktdokumentasjon og kontraktstandarder.
7. NOU-er, DFØ-rapporter og forskning som bakgrunn for metode, modenhet og AI-kvalitet.

## Foreslåtte kvalitetsporter for LLM-dommer

En senere LLM-dommer bør minimum kontrollere:

- at alle krav i konkurransegrunnlaget er adressert eksplisitt
- at absolutte krav, tildelingskriterier og kontraktsvilkår ikke blandes
- at dokumentasjon, frister, signaturer og formalia er dekket
- at forbehold, avvik og uklarheter er identifisert og fagvurdert
- at klima, miljø, seriøsitet, lærlinger, lønns- og arbeidsvilkår og SHA/HMS er svart på der det er relevant
- at tilbudet ikke inneholder juridiske konklusjoner uten kilde og fagverifisering
- at dato, terskelverdi, prosedyre og regelversjon er eksplisitt angitt
