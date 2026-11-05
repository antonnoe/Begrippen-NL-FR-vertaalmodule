# CLAUDE.md

Repo: Begrippen-NL-FR-vertaalmodule

## Wat dit is

Een lexicon NL naar FR met begrippen voor Nederlandstaligen in Frankrijk: een landingspagina met tegels, per domein een viewerpagina en per domein een JSON-bestand.

## Live adres

Niet vastgelegd als eigen adres. De pagina's verwijzen met een absoluut pad naar /Begrippen-NL-FR-vertaalmodule/data/, wat past bij GitHub Pages onder antonnoe.github.io.

## Opbouw

- index.html: landing met tegels voor de domeinen
- 404.html: pagina niet gevonden
- domains/<slug>/index.html: viewer per domein (aanwezig voor belastingen, klussen-en-verbouwen, medisch-en-gezondheid, notariaat-en-vastgoed, overheden, wonen-en-nuts; de landing linkt ook naar toeslagen-en-sociaal, verkeer-en-voertuigen, onderwijs, werk-en-ondernemen, justitie-en-procedures en alles, die als viewer nog ontbreken)
- domains/klussen-en-verbouwen/index-klussen-en-verbouwen.html: extra variant
- domains/domains: leeg bestand
- data/<slug>.json: de begrippen per domein, plus data/alle-begrippen.json
- COPILOT_CHAT.md: afspraken voor Copilot Chat
- LICENSE

## Techniek

Statische HTML met inline CSS en JavaScript, geen externe bibliotheken, geen package.json, geen build. De viewers laden de JSON met fetch. Schema per bestand: domain_title, default_more_info_url, search_sites en terms (nl, fr, cats, subcats, note, aliases, more_info_url, updated).

## Externe diensten en namen van omgevingsvariabelen

Geen eigen diensten en geen omgevingsvariabelen. Verwijst naar infofrankrijk.com en nederlanders.fr, en gebruikt Google-zoeken met site: voor 'zoek verder'.

## Hoe het live gaat

Niet in de repo vastgelegd (geen workflow, CNAME of vercel.json).

## Regels en besluiten

Uit COPILOT_CHAT.md:
- Eén landing met tegels, per domein één viewerpagina en één JSON in /data.
- Stijl: inline HTML, CSS en JS, geen externe libs, mobiel eerst, geen hoofdletters-overdaad.
- Zoeken is accentonafhankelijk op nl, fr, aliases, cats, subcats en note.
- Knoppen per term: kopieer, uitspraak (alleen NL naar FR), meer informatie, zoek verder.
- Geen Bercy-label, gebruik Belastingen of DGFiP waar relevant.
- Verouderde termen niet tonen, hoogstens als alias in note.

## Laatst nagelopen

Laatst nagelopen: 5 november 2026
