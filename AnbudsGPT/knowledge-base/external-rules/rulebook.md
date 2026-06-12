# Regelbok for anbudskontroll

Status: første operative utkast  
Versjon: 0.1  
Dato: 2026-06-12  
Scope: offentlige/kommunale anskaffelser, særlig bygg, anlegg og eiendom  
Kildegrunnlag: `source-cards.csv` og `source-cards.md`

Dette er et kontrollgrunnlag for agenter og LLM-dommer. Det er ikke juridisk rådgivning og skal ikke brukes som automatisk beslutningsmotor uten faglig kontroll.

## Bruksprinsipper

- Alle regelutfall skal vise kilde-ID fra `source-cards.csv`.
- Alle juridiske, kontraktsmessige, tekniske eller anskaffelsesrettslige vurderinger skal merkes `må fagverifiseres`.
- Agenten skal skille mellom absolutte krav, kvalifikasjonskrav, tildelingskriterier, kontraktsvilkår og veiledende informasjon.
- Agenten skal aldri anta at et tilbud er gyldig hvis frist, signatur, obligatoriske vedlegg eller minstekrav mangler.
- Agenten skal aldri skrive at en KOFA-sak eller NOU er gjeldende rett.
- Regler med `2026-07-01` må versjonskontrolleres mot kunngjøringstidspunkt og gjeldende Lovdata/DFØ-tekst.

## Kontrollnivåer

| Nivå | Betydning | Handling |
|---|---|---|
| `blocker` | Kan gi avvisning, ugyldig tilbud, alvorlig regelbrudd eller sensitiv lekkasje. | Stopp og send til faglig kontroll. |
| `major` | Kan gi lav score, kontraktsrisiko, klagerisiko eller vesentlig svakhet. | Må rettes eller begrunnes før innsending. |
| `minor` | Forbedringspunkt uten åpenbar avvisningsrisiko. | Bør rettes hvis tid. |
| `info` | Kontekst eller sporbar merknad. | Brukes som dokumentasjon. |

## Regler

### META-001 Regelversjon og kunngjøringstidspunkt

- Kilder: `REG-001`, `REG-002`, `REG-005`, `REG-006`, `REG-011`, `REG-012`
- Kontroll: Tilbudskontrollen skal angi kunngjøringstidspunkt, terskelverdi, prosedyre og om konkurransen ligger før eller etter 2026-07-01.
- Beviskrav: Doffin/TED-kunngjøring, konkurransegrunnlag eller annen dokumentert dato.
- Feiltilstand: Agenten bruker 2026-07-01-regler uten å vite hvilken regelversjon konkurransen følger.
- Alvorlighet: `blocker`
- Må fagverifiseres: ja

### SRC-001 Kildekrav for regelpåstander

- Kilder: `REG-001`, `REG-002`, `DFO-001`, `RES-004`, `RES-005`
- Kontroll: Alle regelpåstander i vurderingen skal ha kilde-ID og kilde-URL.
- Beviskrav: Henvisning til kildekort og konkret dokument/side.
- Feiltilstand: Agenten gir juridisk eller anskaffelsesrettslig konklusjon uten kilde.
- Alvorlighet: `blocker`
- Må fagverifiseres: ja

### FORM-001 Frister, signatur og innleveringsform

- Kilder: `DFO-003`, `REG-009`, `DOF-001`, `TED-001`
- Kontroll: Tilbudet må kontrolleres mot innleveringsfrist, kommunikasjonskanal, signaturkrav, filformat og eventuelle systemkrav.
- Beviskrav: Konkurransegrunnlag, Doffin/TED-kunngjøring og innleveringsportalens krav.
- Feiltilstand: Frist, signatur, portal, filformat eller obligatorisk leveranseform er uklar eller mangler.
- Alvorlighet: `blocker`
- Må fagverifiseres: ja

### REQ-001 Absolutte krav og minstekrav

- Kilder: `DFO-003`, `DFO-004`, `REG-009`
- Kontroll: Alle absolutte krav og minstekrav skal være identifisert, besvart eksplisitt og støttet av dokumentasjon.
- Beviskrav: Kravliste, svartekst, vedlegg og dokumentreferanse.
- Feiltilstand: Et minstekrav er ubesvart, delvis besvart, uklart eller besvart med forbehold.
- Alvorlighet: `blocker`
- Må fagverifiseres: ja

### QUAL-001 Kvalifikasjonskrav og dokumentasjon

- Kilder: `REG-002`, `REG-009`, `KOFA-002`, `KOFA-003`
- Kontroll: Kvalifikasjonskrav, ESPD, attester, referanser, kapasitet og dokumentasjonskrav skal være komplette.
- Beviskrav: Vedleggsliste, kvalifikasjonssvar, attester og eventuelle tredjepartsforpliktelser.
- Feiltilstand: Dokumentasjon mangler, er utløpt, er feil type eller viser ikke oppfyllelse.
- Alvorlighet: `blocker`
- Må fagverifiseres: ja

### AWARD-001 Tildelingskriterier og evalueringsrespons

- Kilder: `DFO-004`, `REG-010`, `KOFA-004`
- Kontroll: Tilbudet skal svare direkte på hvert tildelingskriterium og vise dokumenterbar merverdi.
- Beviskrav: Kriteriematrise, tilbudstekst, metode, CV-er, fremdriftsplan, miljødata, pris eller annen etterspurt dokumentasjon.
- Feiltilstand: Tilbudet beskriver generelle fordeler uten å svare på kriteriet eller evalueringsmodellen.
- Alvorlighet: `major`
- Må fagverifiseres: ja

### CONTRACT-001 Kontraktsvilkår og gjennomføringsforpliktelser

- Kilder: `DFO-004`, `DFO-009`, `BAE-003`, `KOFA-005`, `KOFA-006`
- Kontroll: Kontraktsvilkår, opsjoner, garantier, endringer, rapportering, sanksjoner og standardkontrakt skal være forstått og priset.
- Beviskrav: Kontraktsvilkår, tilbudsforutsetninger, prisskjema og intern risikovurdering.
- Feiltilstand: Tilbudet lover leveranse uten å prise eller planlegge kontraktsvilkår, eller tar skjulte forbehold.
- Alvorlighet: `major`
- Må fagverifiseres: ja

### DEV-001 Forbehold, avvik og uklarheter

- Kilder: `REG-009`, `KOFA-003`, `DFO-003`
- Kontroll: Alle forbehold, avvik, alternative løsninger og uklarheter skal identifiseres, risikovurderes og eventuelt avklares før levering.
- Beviskrav: Avviksliste, forbeholdsliste, spørsmål/svar-logg og faglig vurdering.
- Feiltilstand: Tilbudet inneholder skjult forbehold, uklar prising, endrede vilkår eller løsning som ikke oppfyller krav.
- Alvorlighet: `blocker`
- Må fagverifiseres: ja

### DOC-001 Obligatoriske vedlegg og dokumentstruktur

- Kilder: `DFO-003`, `REG-009`, `QUAL-001`
- Kontroll: Alle etterspurte vedlegg, skjemaer, erklæringer og dokumenttyper skal være med og navngitt på en måte som gjør evaluering enkel.
- Beviskrav: Vedleggsliste fra konkurransegrunnlag og faktisk filoversikt.
- Feiltilstand: Obligatorisk vedlegg mangler eller er vanskelig å finne.
- Alvorlighet: `blocker`
- Må fagverifiseres: ja

### CONF-001 Innsyn, taushetsplikt og sladding

- Kilder: `DFO-006`, `DFO-007`
- Kontroll: Tilbudet skal identifisere forretningshemmeligheter, persondata og informasjon som bør sladdes ved innsyn.
- Beviskrav: Sladdet versjon, begrunnelse for sladding og intern sensitivitetssjekk.
- Feiltilstand: Sensitive opplysninger er usladdet, eller hele tilbudet er merket konfidensielt uten konkret begrunnelse.
- Alvorlighet: `major`
- Må fagverifiseres: ja

### ENV-001 Klima og miljø

- Kilder: `SAM-001`, `SAM-002`, `SAM-003`, `SAM-004`, `BAE-008`
- Kontroll: Klima- og miljøkrav, 30 prosent-regel, dokumentasjon, målemetode og kontraktsoppfølging skal besvares konkret.
- Beviskrav: Miljøkrav, tildelingskriterier, produktdata, transportopplegg, avfallsplan, klimagassdata eller annen etterspurt dokumentasjon.
- Feiltilstand: Tilbudet gir generelle miljøløfter uten målbar dokumentasjon eller leveranseplan.
- Alvorlighet: `major`
- Må fagverifiseres: ja

### SER-001 Seriøsitet, lønns- og arbeidsvilkår, lærlinger og UE-kjede

- Kilder: `SAM-005`, `SAM-006`, `SAM-007`, `SAM-008`, `SAM-009`, `SAM-010`
- Kontroll: Tilbudet skal kunne dokumentere seriøsitetskrav, lønns- og arbeidsvilkår, lærlingkrav, bankbetaling og underleverandørkjede der dette er relevant.
- Beviskrav: Egenerklæringer, rutiner, UE-oversikt, lærlingplan, timelister eller annen etterspurt dokumentasjon.
- Feiltilstand: Underleverandørkjede, lærlingbruk eller lønns-/arbeidsvilkår er uklart eller ikke dokumenterbart.
- Alvorlighet: `major`
- Må fagverifiseres: ja

### SHA-001 SHA/HMS og byggherreforskriften

- Kilder: `BAE-006`, `SAM-005`
- Kontroll: Tilbudet skal svare på SHA/HMS-krav, risikoforhold, roller, koordinering og fremdriftsmessige sikkerhetshensyn.
- Beviskrav: SHA/HMS-erklæring, risikovurdering, organisasjonsplan, fremdriftsplan og relevante rutiner.
- Feiltilstand: SHA-krav er ikke besvart, eller HMS-rutiner brukes som erstatning for prosjektspesifikk SHA-forståelse.
- Alvorlighet: `major`
- Må fagverifiseres: ja

### BAE-001 Bygg, anlegg, FDV, TEK17 og produktdokumentasjon

- Kilder: `BAE-001`, `BAE-002`, `BAE-004`, `BAE-007`, `BAE-008`, `BAE-009`, `BAE-010`
- Kontroll: Tilbudet skal håndtere BAE-spesifikke krav til FDV, teknisk dokumentasjon, produktdokumentasjon, mengder og overlevering.
- Beviskrav: FDV-plan, teknisk dokumentasjon, produktdokumentasjon, mengdebeskrivelse, referanse til krav og faglig kontroll.
- Feiltilstand: Tilbudet lover teknisk samsvar eller FDV-leveranse uten dokumentasjon eller avgrensning.
- Alvorlighet: `major`
- Må fagverifiseres: ja

### PROC-001 Kunngjøring, Doffin/TED, eForms og CPV

- Kilder: `DOF-001`, `DOF-002`, `DOF-003`, `DOF-004`, `DOF-005`, `TED-001`, `TED-002`, `TED-003`, `TED-004`, `TED-005`, `TED-006`, `TED-007`
- Kontroll: Agenten skal skille mellom kunngjøringsdata, konkurransegrunnlag og statistikk. Original kunngjøring skal være styrende.
- Beviskrav: Doffin/TED-lenke, notice type, CPV, frist, kontraktstype og eventuelle endringskunngjøringer.
- Feiltilstand: Agenten bruker statistikk eller søkedata som fasit for krav, frister eller rettigheter.
- Alvorlighet: `major`
- Må fagverifiseres: ja

### KOFA-001 Praksisbruk

- Kilder: `KOFA-001`, `KOFA-002`, `KOFA-004`, `KOFA-005`, `KOFA-006`, `KOFA-007`, `RES-002`
- Kontroll: KOFA-saker skal bare brukes som praksisindikator og må leses i fulltekst før de brukes i en konkret vurdering.
- Beviskrav: Saksnummer, dato, faktum, regelverk, terskel og konkret relevans.
- Feiltilstand: Agenten generaliserer fra en KOFA-sak uten faktumsammenligning.
- Alvorlighet: `major`
- Må fagverifiseres: ja

### AI-001 LLM-hallusinasjon og sporbarhet

- Kilder: `RES-004`, `RES-005`, `SRC-001`
- Kontroll: LLM-genererte vurderinger skal være sporbare, kildebaserte og tydelig markere usikkerhet.
- Beviskrav: Kilde-ID, sitatnær oppsummering der lovlig, tydelig usikkerhet og fagverifisering.
- Feiltilstand: Agenten finner på kilde, saksnummer, regeltekst, frist, terskelverdi eller juridisk konklusjon.
- Alvorlighet: `blocker`
- Må fagverifiseres: ja

## Minimumsrapport fra agent

En agent som kontrollerer et tilbud skal levere:

1. Kort konklusjon med samlet risiko.
2. Tabell med regel-ID, status, funn, kilde og alvorlighet.
3. Liste over manglende dokumentasjon.
4. Liste over forbehold, avvik og uklarheter.
5. Liste over punkter som må fagverifiseres.
6. Versjon: dato, konkurranse, kunngjøring, terskelverdi og regelversjon.
