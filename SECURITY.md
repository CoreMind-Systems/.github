# Sikkerhedspolitik

## Rapportering af sårbarheder

Hvis du har fundet en sikkerhedssårbarhed i Helix-platformen eller relaterede systemer, bedes du kontakte os direkte:

**Email:** security@coremindx.com

Vi beder dig om:
- **Ikke** at offentliggøre sårbarheden før den er løst
- At give os rimelig tid til at undersøge og løse problemet
- At inkludere en beskrivelse af sårbarheden og eventuelle trin til reproduktion

## Svartid

| Prioritet | Første svar | Løsning |
|-----------|------------|---------|
| **Kritisk** (datalæk, auth bypass) | Inden for 4 timer | Inden for 24 timer |
| **Høj** (privilege escalation) | Inden for 24 timer | Inden for 72 timer |
| **Medium** (informationsafsløring) | Inden for 48 timer | Inden for 1 uge |
| **Lav** (best practice) | Inden for 1 uge | Planlagt i næste release |

## Sikkerhedsarkitektur

Helix er bygget med følgende sikkerhedsprincipper:

- **Zero-trust dataisolering** — Row-Level Security på databaseniveau sikrer at organisationers data aldrig kan krydse
- **Krypteret kommunikation** — Al trafik krypteret via TLS/HTTPS (Cloudflare)
- **JWT-baseret autentifikation** — Tokens med begrænset levetid og tenant-scoping
- **Rollebaseret adgangskontrol** — Brugerrettigheder håndhæves både i UI og API
- **Automatiseret sikkerhedsvalidering** — Sikkerhedstjek kører på enhver kodeændring

## Ansvarlig offentliggørelse

Vi anerkender sikkerhedsforskere der hjælper med at forbedre vores platform. Med din tilladelse krediterer vi dig gerne i forbindelse med offentliggørelsen af en rettelse.
