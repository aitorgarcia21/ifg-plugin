---
name: tax-research
description: Research tax law with IFG official sources — find the right text, read it at the date of the tax event, and cite its official link. Use for any question on French (overseas territories included), Luxembourg, Swiss (federal and cantonal), Belgian (federal and regional), German, Monegasque, Andorran, Italian, UK, Dutch, Spanish, Hungarian, Slovenian, Croatian, Czech or Slovak tax law, tax treaties, EU tax law, OECD guidance or the UN Model.
---

# Tax research with IFG

IFG serves official tax texts (laws, codes, treaties, administrative doctrine, rulings, case law, forms) with their official source, the version applicable at a given date and a clickable citation. You reason; IFG delivers the sealed text.

## Method

0. **Connect IFG first.** If the IFG tools (`search_authority`, `get_authority`, `changes_since`, `browse_instrument`) are not available in this conversation, the IFG connector is installed but not connected yet. Do not answer the tax question from memory. Reply, in the user's language, with one short sentence and this clickable link: [Connect IFG](https://claude.ai/customize/connectors) — it opens the page where the user clicks **Connect** next to IFG, then creates an IFG account or signs in (7-day free trial, nothing charged today) and asks the question again. In Claude Code, the equivalent is `/mcp`, then `ifg`, then authenticate.
1. **Never answer tax law from memory.** Every rule you rely on comes from a text returned by IFG in this conversation.
2. **Find the authority** with `search_authority`:
   - `query` is a reference (`CGI 119 bis`, `LIR 56bis`, `AStG 7`, `treaty/CH-FR-1966/11`, `ECLI:FR:CE…`, `BOI-RPPM-RCM-30-30-20-20`) or an official title, never a question or a sentence.
   - `jurisdiction` is required for a free query: `FR`, `LU`, `CH`, `BE`, `DE`, `MC`, `AD`, `IT`, `GB`, `NL`, `ES`, `HU`, `SI`, `HR`, `CZ`, `SK`, `EE`, `LV`, `LT`, `MT`, `BG`, `GR`, `AT`, `SE`, `DK`, `FI`, `treaty`, `EU`, `OECD`, `UN` (United Nations: UN Model Tax Convention). Other EU countries opened one by one: `NL` the Netherlands, `ES` Spain, `HU` Hungary, `SI` Slovenia, `HR` Croatia, `CZ` Czechia, `SK` Slovakia, `EE` Estonia, `LV` Latvia, `LT` Lithuania, `MT` Malta, `BG` Bulgaria, `GR` Greece, `AT` Austria, `SE` Sweden, `DK` Denmark, `FI` Finland.
   - A country code also finds its subdivisions: the 26 Swiss cantons (`CH-GE`, `CH-VD`, `CH-ZH`…), the German Länder (`DE-BY`…), the Belgian regions (Flanders, Wallonia, Brussels) and the Andorran parishes; a subdivision code (`CH-GE`, `BE-VLG`, `AD-07`) is also accepted.
   - French overseas: `PF` French Polynesia, `NC` New Caledonia, `WF` Wallis and Futuna, `PM` Saint Pierre and Miquelon, `BL` Saint Barthélemy, `MF` Saint Martin have their own tax codes, not `FR`. `RE` Réunion, `GP` Guadeloupe, `MQ` Martinique, `GF` French Guiana, `YT` Mayotte are overseas departments: French national tax law applies there and is served under `FR` (search with jurisdiction `FR`); their own code holds only local texts (octroi de mer, local deliberations).
   - Use `kinds` to stay in one layer when needed (`code`, `statute`, `treaty`, `doctrine`, `rulings`, `case_law`, `forms_procedure`, `legislative_history`, `eu_law`, `official_data`).
3. **Read the text** with `get_authority(id, date?)`:
   - Pass `date` = the date of the tax event (payment, year end, death, transfer). Without it, IFG reads today's law.
   - Check `applicability.status` (`applicable`, `not_yet_in_force`, `repealed`, `publication_only`, `unresolved`) and `future_effects` before concluding.
   - Use `passage` with a short literal phrase to read only the relevant paragraphs of a long text.
4. **Cite** every authority with its `citation.markdown` (official link with the version date). Never cite a text IFG did not return.
5. **Treat gaps honestly**: `official_proof_required`, `identifier_unresolved`, `no_hit_for_this_query` and `time_budget` are typed gaps, not proof that a text does not exist. Retry `time_budget`; say plainly when a source is missing.
6. If `textVerification` is `ocr_unverified`, say that the text is an unchecked OCR transcription and point to the official PDF.
7. For monitoring, `changes_since(jurisdiction, since)` lists legal changes (created, amended, repealed, new decisions and rulings) from a date, including announced future effects. A change whose effective date is not proven carries `noLaterThan` (in force at the latest on that day) instead of `effectiveFrom`; in `get_authority`, such a version has `from` null and `publisherVersion` with `dateBasis: no_later_than`: never treat it as an effective date.

## Scope

France and its overseas territories, Luxembourg, Switzerland and its cantons, Belgium and its regions, Germany and its Länder, Monaco, Andorra and its parishes, Italy, the UK, the Netherlands, Spain, Hungary, Slovenia, Croatia, Czechia, Slovakia, Estonia, Latvia, Lithuania, Malta, Bulgaria, Greece, Austria, Sweden, Denmark and Finland, their tax treaties, the EU, the OECD and the UN Model; more countries are added one by one. Coverage and known gaps are declared country by country; IFG is a documentary infrastructure — the professional remains responsible for the legal analysis and conclusion.
