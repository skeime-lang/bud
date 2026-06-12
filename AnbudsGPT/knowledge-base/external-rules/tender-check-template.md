# Kontrollrapport for anbud

Status: mal  
Versjon: 0.1  
Dato for mal: 2026-06-12  
Basert på: `rulebook.md` og `llm-judge-rubric.yaml`

Denne malen brukes når en agent eller LLM-dommer skal kontrollere et konkret anbud mot eksterne anskaffelsesregler og konkurransegrunnlaget.

Malen skal ikke fylles ut med juridiske konklusjoner uten fagverifisering.

## 1. Metadata

| Felt | Verdi |
|---|---|
| Kontroll-ID |  |
| Dato for kontroll |  |
| Kontrollert av |  |
| Oppdragsgiver |  |
| Prosjekt/anskaffelse |  |
| Doffin/TED-lenke |  |
| Kunngjøringsdato |  |
| Tilbudsfrist |  |
| Prosedyre |  |
| Estimert verdi/terskelkontekst |  |
| Regelversjon vurdert |  |
| 2026-07-01 relevant? |  |
| Kontraktstype/entrepriseform |  |
| BAE-relevant? |  |

## 2. Inputgrunnlag

Fyll ut hvilke dokumenter som faktisk er kontrollert. Ikke anta at et dokument finnes.

| Dokumenttype | Fil/kilde | Dato/versjon | Kontrollert? | Kommentar |
|---|---|---|---|---|
| Doffin/TED-kunngjøring |  |  |  |  |
| Konkurransegrunnlag |  |  |  |  |
| Kravspesifikasjon |  |  |  |  |
| Kontraktsvilkår |  |  |  |  |
| Prisskjema |  |  |  |  |
| Vedleggsliste |  |  |  |  |
| Tilbudsbrev |  |  |  |  |
| Tilbudsbesvarelse |  |  |  |  |
| Kvalifikasjonsdokumentasjon |  |  |  |  |
| Miljø-/SHA-/seriøsitetsdokumentasjon |  |  |  |  |
| FDV/teknisk dokumentasjon |  |  |  |  |

## 3. Kort konklusjon

| Felt | Verdi |
|---|---|
| Samlet status | `pass` / `needs_review` / `fail` / `insufficient_information` |
| Samlet score |  |
| Hard-fail funnet? | ja/nei |
| Viktigste risiko |  |
| Må fagverifiseres før innsending? | ja/nei |

Kort sammendrag:

> 

## 4. Hard-fail kontroll

Hvis ett punkt får `fail`, skal rapporten samlet minimum være `needs_review`, normalt `fail`, til punktet er rettet eller fagverifisert.

| ID | Regelreferanse | Status | Funn | Bevis | Tiltak |
|---|---|---|---|---|---|
| HF-001 | `FORM-001`, `DOC-001` |  | Frist, kanal, signatur, format eller obligatorisk vedlegg mangler/er uklart. |  |  |
| HF-002 | `REQ-001` |  | Absolutt krav/minstekrav er ubesvart, motsagt eller besvart med uavklart forbehold. |  |  |
| HF-003 | `QUAL-001` |  | Kvalifikasjonsdokumentasjon mangler, er utløpt, feil type eller viser ikke oppfyllelse. |  |  |
| HF-004 | `DEV-001` |  | Skjult forbehold, vesentlig avvik, uklar prisforutsetning eller ikke-bindende tilbudstekst. |  |  |
| HF-005 | `SRC-001`, `AI-001` |  | Agenten/rapporten mangler kilde eller finner på regel, frist, terskel, sak eller juridisk konklusjon. |  |  |
| HF-006 | `META-001` |  | 2026-07-01-sensitiv regel brukes uten kontroll av kunngjøringsdato og regelversjon. |  |  |

Statusverdier: `pass`, `needs_review`, `fail`, `not_applicable`, `insufficient_information`.

## 5. Scoring

| ID | Dimensjon | Poeng maks | Poeng gitt | Kommentar |
|---|---|---:|---:|---|
| S1 | Kildegrunnlag og regelversjon | 15 |  |  |
| S2 | Kravdekning | 20 |  |  |
| S3 | Kvalifikasjon og formalia | 15 |  |  |
| S4 | Tildelingskriterier og evalueringsrespons | 15 |  |  |
| S5 | Forbehold, avvik og kontraktsrisiko | 10 |  |  |
| S6 | Miljø, seriøsitet, SHA/HMS og BAE-dokumentasjon | 15 |  |  |
| S7 | Taushetsplikt, sladding og delbarhet | 5 |  |  |
| S8 | AI-sikkerhet, usikkerhet og sporbarhet | 5 |  |  |
| **SUM** |  | **100** |  |  |

Tolkning:

- `80-100`: kan være klar for innsending dersom ingen hard-fail finnes og fagkritiske punkter er kontrollert
- `65-79`: bør gjennomgås og forbedres før innsending
- `0-64`: høy risiko eller utilstrekkelig grunnlag

## 6. Regelkontroll

| Regel-ID | Status | Alvorlighet | Funn | Bevis/dokumentreferanse | Kildekort | Anbefalt tiltak | Må fagverifiseres |
|---|---|---|---|---|---|---|---|
| `META-001` |  | `blocker` |  |  | `REG-001`, `REG-002`, `REG-005`, `REG-006`, `REG-011`, `REG-012` |  | ja |
| `SRC-001` |  | `blocker` |  |  | `REG-001`, `REG-002`, `DFO-001`, `RES-004`, `RES-005` |  | ja |
| `FORM-001` |  | `blocker` |  |  | `DFO-003`, `REG-009`, `DOF-001`, `TED-001` |  | ja |
| `REQ-001` |  | `blocker` |  |  | `DFO-003`, `DFO-004`, `REG-009` |  | ja |
| `QUAL-001` |  | `blocker` |  |  | `REG-002`, `REG-009`, `KOFA-002`, `KOFA-003` |  | ja |
| `AWARD-001` |  | `major` |  |  | `DFO-004`, `REG-010`, `KOFA-004` |  | ja |
| `CONTRACT-001` |  | `major` |  |  | `DFO-004`, `DFO-009`, `BAE-003`, `KOFA-005`, `KOFA-006` |  | ja |
| `DEV-001` |  | `blocker` |  |  | `REG-009`, `KOFA-003`, `DFO-003` |  | ja |
| `DOC-001` |  | `blocker` |  |  | `DFO-003`, `REG-009`, `QUAL-001` |  | ja |
| `CONF-001` |  | `major` |  |  | `DFO-006`, `DFO-007` |  | ja |
| `ENV-001` |  | `major` |  |  | `SAM-001`, `SAM-002`, `SAM-003`, `SAM-004`, `BAE-008` |  | ja |
| `SER-001` |  | `major` |  |  | `SAM-005`, `SAM-006`, `SAM-007`, `SAM-008`, `SAM-009`, `SAM-010` |  | ja |
| `SHA-001` |  | `major` |  |  | `BAE-006`, `SAM-005` |  | ja |
| `BAE-001` |  | `major` |  |  | `BAE-001`, `BAE-002`, `BAE-004`, `BAE-007`, `BAE-008`, `BAE-009`, `BAE-010` |  | ja |
| `PROC-001` |  | `major` |  |  | `DOF-*`, `TED-*` |  | ja |
| `KOFA-001` |  | `major` |  |  | `KOFA-*`, `RES-002` |  | ja |
| `AI-001` |  | `blocker` |  |  | `RES-004`, `RES-005`, `SRC-001` |  | ja |

## 7. Manglende dokumentasjon

| Nr. | Mangler | Hvor etterspurt | Konsekvens | Tiltak | Ansvar |
|---:|---|---|---|---|---|
| 1 |  |  |  |  |  |
| 2 |  |  |  |  |  |
| 3 |  |  |  |  |  |

## 8. Forbehold, avvik og uklarheter

| Nr. | Type | Tekst/funn | Mulig konsekvens | Anbefalt tiltak | Må fagverifiseres |
|---:|---|---|---|---|---|
| 1 | forbehold/avvik/uklarhet |  |  |  | ja |
| 2 | forbehold/avvik/uklarhet |  |  |  | ja |
| 3 | forbehold/avvik/uklarhet |  |  |  | ja |

## 9. Spørsmål til oppdragsgiver

Bruk denne listen når uklarheter bør avklares før tilbudsfrist. Spørsmål må være nøkterne og ikke røpe unødvendig tilbudsstrategi.

| Nr. | Tema | Foreslått spørsmål | Hvorfor spørsmålet er nødvendig | Frist/status |
|---:|---|---|---|---|
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |

## 10. Fagverifisering

| Område | Må verifiseres av | Hvorfor | Status |
|---|---|---|---|
| Anskaffelsesrett | jurist/anskaffelsesfaglig | Juridiske vurderinger, avvisning, forbehold, klage, regelversjon |  |
| Kontrakt | kontraktsansvarlig/jurist | Standardvilkår, risiko, forbehold, opsjoner, endringer |  |
| Pris/økonomi | kalkyleansvarlig | Prisskjema, mengder, forutsetninger, risiko |  |
| SHA/HMS | SHA/HMS-ansvarlig | Byggherreforskrift, prosjektspesifikk risiko, fremdrift |  |
| Miljø | miljø-/prosjektansvarlig | Klima-/miljøkrav, dokumentasjon, oppfølging |  |
| Teknisk/FDV | fagansvarlig | TEK17, FDV, produktdokumentasjon, tekniske krav |  |

## 11. Endelig leveransekontroll

| Punkt | Status | Kommentar |
|---|---|---|
| Alle obligatoriske dokumenter er med |  |  |
| Alle absolutte krav er besvart |  |  |
| Alle kvalifikasjonskrav er dokumentert |  |  |
| Alle tildelingskriterier er besvart tydelig |  |  |
| Prisskjema er komplett og konsistent |  |  |
| Forbehold og avvik er fjernet eller fagverifisert |  |  |
| Sladdet versjon er vurdert |  |  |
| Regelversjon og kunngjøringsdato er kontrollert |  |  |
| Fagverifisering er utført der nødvendig |  |  |

## 12. Agentinstruks for bruk

Når denne malen brukes av en agent:

1. Les `source-cards.csv`, `rulebook.md` og `llm-judge-rubric.yaml`.
2. Les kun de anbudsdokumentene som eksplisitt er gitt for kontroll.
3. Fyll ut metadata og inputgrunnlag før vurdering.
4. Kjør hard-fail kontroll før scoring.
5. Bruk `insufficient_information` når dokumentasjon ikke er gitt.
6. Marker alle juridiske og faglige vurderinger med `må fagverifiseres`.
7. Ikke skriv at tilbudet er gyldig eller lovlig. Skriv heller om risiko, mangler og anbefalt kontroll.
