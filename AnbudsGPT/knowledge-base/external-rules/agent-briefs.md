# Subagenter for innhenting av anbudsregler

Formål: samle og strukturere kilder om offentlige anskaffelser som senere kan bli regelbok og kvalitetsdommer for tilbud. Agentene skal ikke teste mot repo, ikke kontrollere lokale dokumenter og ikke skrive juridiske konklusjoner.

## Felles arbeidsregler

- Bruk primært offisielle kilder: Lovdata, DFØ/Anskaffelser.no, Doffin, TED, Regjeringen, KOFA, Arbeidstilsynet, DIBK og Standard Norge.
- Marker dato, versjon og om kilden er lov/forskrift, veileder, praksis, statistikk, standardreferanse eller forskning.
- Skill mellom bindende regel, veiledning, praksis, teknisk datakilde og forsknings-/bakgrunnskilde.
- Marker alt som må fagverifiseres før bruk i tilbud.
- Marker regler som er endret eller varslet endret rundt 2026-07-01.
- Ikke gjengi betalt standardtekst fra Standard Norge.
- Ikke konkluder juridisk. Skriv heller "må vurderes", "kan være relevant" eller "krever fagverifisering".

## Felles outputformat

Hver agent skal levere kildekort med disse feltene:

- `tema`
- `regel/source topic`
- `kilde`
- `dato/versjon`
- `praktisk betydning for tilbud`
- `risiko`
- `må fagverifiseres`
- `change_marker` når relevant, for eksempel `2026-07-01`

## Regelverksagent

Ansvar:

- Anskaffelsesloven
- Anskaffelsesforskriften (FOA)
- Forsyningsforskriften
- Konsesjonskontraktforskriften
- terskelverdier
- prosedyrer
- avvisning
- tildeling
- karens og meddelelse
- endringer rundt 2026-07-01

Startkilder:

- https://lovdata.no/dokument/NL/lov/2016-06-17-73
- https://lovdata.no/dokument/SF/forskrift/2016-08-12-974
- https://lovdata.no/dokument/SF/forskrift/2016-08-12-975
- https://lovdata.no/dokument/SF/forskrift/2016-08-12-976
- https://www.anskaffelser.no/nn/anskaffelsesregelverk/lov-og-forskrifter-om-offentlege-anskaffingar
- https://www.anskaffelser.no/anskaffelsesregelverk/terskelverdier-offentlige-anskaffelser

## DFØ-agent

Ansvar:

- anskaffelsesprosess
- konkurransegrunnlag
- kravspesifikasjon
- kvalifikasjonskrav
- tildelingskriterier
- kontraktsvilkår
- innsyn og taushetsplikt
- klage
- kontraktsoppfølging

Startkilder:

- https://www.anskaffelser.no/anskaffelsesprosess/anskaffelsesprosessen-steg-steg
- https://www.anskaffelser.no/anskaffelsesprosess/anskaffelsesprosessen-steg-steg/avklare-behov-og-forberede-konkurransen/konkurransegrunnlag
- https://www.anskaffelser.no/anskaffelsesprosess/anskaffelsesprosessen-steg-steg/avklare-behov-og-forberede-konkurransen/kravspesifikasjoner-tildelingskriterier-og-kontraktsvilkar
- https://www.anskaffelser.no/nn/anskaffelsesregelverk/innsyn-og-offentlegheit
- https://www.anskaffelser.no/anskaffelsesregelverk/taushetsplikt-og-offentlige-anskaffelser
- https://www.anskaffelser.no/anskaffelsesregelverk/klage-pa-offentlig-anskaffelse

## Doffin/TED-agent

Ansvar:

- Doffin
- TED
- eForms
- CPV-koder
- kunngjøringer
- kontraktskunngjøringer
- resultatkunngjøringer
- teknisk datainnhenting og søk

Startkilder:

- https://www.doffin.no/
- https://www.doffin.no/data
- https://www.anskaffelser.no/data-statistikk-og-analyse/kunngjoringer-av-konkurranser
- https://ted.europa.eu/en/
- https://docs.ted.europa.eu/eforms/latest/index.html
- https://single-market-economy.ec.europa.eu/single-market/public-procurement/digital-procurement/common-procurement-vocabulary_en

## BAE-agent

Ansvar:

- bygg, anlegg og eiendom
- entrepriseformer
- kontraktstyper
- Standard Norge-referanser
- SHA/HMS
- FDV/FDVU
- TEK17
- SAK10
- byggevaredokumentasjon

Startkilder:

- https://www.anskaffelser.no/kategorispesifik-veiledning/bygg-anlegg-og-eiendom-bae
- https://www.anskaffelser.no/kategorispesifik-veiledning/bygg-anlegg-og-eiendom-bae/kontrakter-bygg-og-anlegg
- https://standard.no/fagomrader/kontraktstandarder-bygg-anlegg-og-eiendom/
- https://www.arbeidstilsynet.no/regelverk/forskrifter/byggherreforskriften/
- https://www.dibk.no/regelverk/byggteknisk-forskrift-tek17

## Samfunnshensyn-agent

Ansvar:

- klima og miljø
- 30 prosent-regelen
- seriøsitetsbestemmelser
- lønns- og arbeidsvilkår
- lærlinger
- leverandørkjede
- Norgesmodellen
- betaling via bank

Startkilder:

- https://www.anskaffelser.no/samfunnshensyn-i-offentlige-anskaffelser/klima-og-miljo-i-offentlige-anskaffelser
- https://www.anskaffelser.no/maler-veiledere-eksempler-og-andre-verktoy/veiledere/veileder-til-regler-om-klima-og-miljohensyn-i-offentlige-anskaffelser
- https://www.anskaffelser.no/samfunnshensyn-i-offentlige-anskaffelser/arbeidslivskriminalitet-og-sosial-dumping
- https://www.anskaffelser.no/anskaffelsesregelverk/krav-om-bruk-av-laerlinger-i-offentlige-kontrakter/veileder-om-bruk-av-laerlinger-i-offentlige-kontrakter

## KOFA/praksis-agent

Ansvar:

- KOFA-praksis
- avvisning
- forbehold og avvik
- dokumentasjon og avklaring
- evaluering
- ulovlig direkte anskaffelse
- rammeavtaler og avrop

Startkilder:

- https://www.kofa.no/
- https://www.klagenemndssekretariatet.no/klagenemda-for-offentlige-anskaffelser-kofa
- https://www.klagenemndssekretariatet.no/klagenemda-for-offentlige-anskaffelser-kofa/utvalgte-saker
- https://www.anskaffelser.no/veileder-til-reglene-om-offentlige-anskaffelser/35-ettersendings-og-avklaringsadgangen
- https://www.anskaffelser.no/veileder-til-reglene-om-offentlige-anskaffelser/36-avvisning

## Forskning-agent

Ansvar:

- NOU-er
- DFØ-rapporter
- anskaffelsesundersøkelsen
- innkjøpsmodenhet
- AI/LLM-kvalitet, hallucination og evaluering
- metodekilder for senere LLM-dommer

Startkilder:

- https://www.regjeringen.no/no/dokumenter/nou-2023-26/id3013726/
- https://www.regjeringen.no/no/dokumenter/nou-2024-9/id3039569/
- https://www.anskaffelser.no/innkjopsledelse/anskaffelsesundersokelsen
- https://arxiv.org/abs/2401.01301
- https://arxiv.org/abs/2305.11747
