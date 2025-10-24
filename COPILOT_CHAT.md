# Repo-gedrag voor Copilot Chat

Doel: NL↔FR lexicon. Eén landing met tegels, per domein één viewer-pagina en één JSON in /data.
Stijl: inline HTML/CSS/JS (geen externe libs), mobiele first, geen hoofdletters-overdaad.
Padconventies:
- Landing: /index.html
- Domeinen: /domains/<slug>/index.html (bijv. overheden, klussen-en-verbouwen, ...)
- Data: /data/<slug>.json
JSON-schema (korte versie):
{
  "domain_title": "...",
  "default_more_info_url": "https://infofrankrijk.com/...",
  "search_sites": ["infofrankrijk.com","nederlanders.fr"],
  "terms": [
    {"nl":"...", "fr":"...", "cats":["..."], "subcats":["..."], "note":"...", "aliases":["..."], "more_info_url":"", "updated":"YYYY-MM-DD"}
  ]
}
Functioneel:
- Viewer: zoek (accent-onafhankelijk) op nl/fr/aliases/cats/subcats/note.
- Knoppen per term: kopieer, (alleen NL→FR) uitspraak, “meer informatie” (term-url of domain default), “zoek verder” (site:infofrankrijk.com / site:nederlanders.fr).
- Geen “Bercy”-label; gebruik “Belastingen” of “DGFiP” waar relevant.
- Verouderde termen niet tonen; hoogstens als alias in note.