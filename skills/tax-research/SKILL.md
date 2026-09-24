---
name: tax-research
description: Research tax law with IFG official sources — find the right text, read it at the date of the tax event, and cite its official link. Use for any question on French, Luxembourg, Swiss, Belgian, German, Monegasque, Andorran or Italian tax law, tax treaties, EU tax law or OECD guidance.
---

# Tax research with IFG

IFG serves official tax texts (laws, codes, treaties, administrative doctrine, rulings, case law, forms) with their official source, the version applicable at a given date and a clickable citation. You reason; IFG delivers the sealed text.

## Method

1. **Never answer tax law from memory.** Every rule you rely on comes from a text returned by IFG in this conversation.
2. **Find the authority** with `search_authority`:
   - `query` is a reference (`CGI 119 bis`, `LIR 56bis`, `AStG 7`, `treaty/CH-FR-1966/11`, `ECLI:FR:CE…`, `BOI-RPPM-RCM-30-30-20-20`) or an official title, never a question or a sentence.
   - `jurisdiction` is required for a free query (`FR`, `LU`, `CH`, `BE`, `DE`, `MC`, `AD`, `IT`, `EU`, `OECD`, `treaty`).
   - Use `kinds` to stay in one layer when needed (`code`, `statute`, `treaty`, `doctrine`, `rulings`, `case_law`, `forms_procedure`, `legislative_history`, `eu_law`, `official_data`).
3. **Read the text** with `get_authority(id, date?)`:
   - Pass `date` = the date of the tax event (payment, year end, death, transfer). Without it, IFG reads today's law.
   - Check `applicability.status` (`applicable`, `not_yet_in_force`, `repealed`, `publication_only`, `unresolved`) and `future_effects` before concluding.
   - Use `passage` with a short literal phrase to read only the relevant paragraphs of a long text.
4. **Cite** every authority with its `citation.markdown` (official link with the version date). Never cite a text IFG did not return.
5. **Treat gaps honestly**: `official_proof_required`, `identifier_unresolved`, `no_hit_for_this_query` and `time_budget` are typed gaps, not proof that a text does not exist. Retry `time_budget`; say plainly when a source is missing.
6. If `textVerification` is `ocr_unverified`, say that the text is an unchecked OCR transcription and point to the official PDF.
7. For monitoring, `changes_since(jurisdiction, since)` lists legal changes (created, amended, repealed, new decisions and rulings) from a date, including announced future effects.

## Scope

France and its neighbours, their tax treaties, the EU and the OECD. Coverage and known gaps are declared country by country; IFG is a documentary infrastructure — the professional remains responsible for the legal analysis and conclusion.
