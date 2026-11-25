# IFG for Claude

**Tax law for your AI.** Official tax texts at the date of the facts, with applicability status, historical versions and a clickable link to each official publisher. IFG is a documentary research infrastructure: it delivers the exact texts; the legal analysis stays yours.

IFG connects Claude to official tax sources across **32 European jurisdictions** (all **27 EU Member States** including **France** and its overseas territories, **Switzerland** and its 26 cantons, the **United Kingdom**, **Monaco**, **Andorra** and its parishes, **Liechtenstein**) and **Israel**, plus **2,389 bilateral tax treaties** (with protocols and MLI effects), **EU tax law**, **OECD Model Commentaries** and the **UN Model**: codes and laws, administrative doctrine, rulings, case law, forms and parliamentary history.

- Every text comes from its official publisher, with `verification: verified` and a citation link carrying the version date.
- Point-in-time reading: the exact wording applicable on the date of the tax event, with past and announced future changes.
- Cross-border assembly: bilateral treaty, MLI, EU directives and domestic rules assembled in one read-only call (`cross_border_sources`).
- Quote verification: `check_sources` verifies every quoted passage against the official text at that date.
- Honest gaps: a missing or unproven text is reported as an explicit gap, never invented.

## What the plugin contains

- **MCP server** `ifg` at `https://ifg.tax/v1/mcp` (Streamable HTTP, OAuth 2.1 with PKCE). Eight tools: `search_authority`, `get_authority`, `browse_instrument`, `cross_border_sources`, `changes_since`, `check_sources`, `coverage` (all read-only) and `report_issue` (reports a suspected source discrepancy without client facts).
- **Skill `tax-research`** (`/ifg:tax-research`): research method (find, assemble cross-border rules, read at the right date, answer like a tax professional with each text named in the sentence and linked to its official version, verify quotes and respect gaps).
- **Skill `setup`** (`/ifg:setup`): sign-in and connection check.

After installing, connect IFG once: **Customize -> Connectors -> IFG -> Connect** on claude.ai (https://claude.ai/customize/connectors), or `/mcp` in Claude Code. An IFG account is required: 7-day free trial, no card required; when it ends, access simply stops unless you subscribe.

- Website: https://ifg.tax
- Connect guide: https://ifg.tax/connect
- Security: https://ifg.tax/security
- Technical specification: https://ifg.tax/ifg-mcp-specification.pdf
- Privacy policy: https://ifg.tax/privacy-policy
- Terms: https://ifg.tax/terms-and-conditions
- Support: contact@ifg.tax

IFG is a documentary infrastructure: the professional and their assistant remain responsible for the legal analysis and conclusion.

---

# IFG pour Claude

**Le droit fiscal pour votre IA.** Les textes fiscaux officiels à la date du fait générateur, avec statut d'applicabilité, versions datées et lien cliquable vers l'éditeur officiel, pour **32 juridictions européennes** (les **27 États membres de l'Union européenne** et l'outre-mer français, la **Suisse** et ses 26 cantons, le **Royaume-Uni**, **Monaco**, **Andorre** et ses paroisses, le **Liechtenstein**), **Israël**, **2 389 conventions fiscales bilatérales** (avec effets MLI), le **droit de l'Union européenne**, les commentaires du **Modèle OCDE** et le **Modèle ONU**.

IFG est une base de recherche documentaire : il fournit les textes officiels via 8 outils MCP (dont `cross_border_sources` et `check_sources`), l'analyse reste la vôtre. Après l'installation, connectez IFG une fois : **Personnaliser -> Connecteurs -> IFG -> Connecter** sur claude.ai (https://claude.ai/customize/connectors), ou `/mcp` dans Claude Code. Essai gratuit de 7 jours, sans carte bancaire : à la fin de l'essai, sans abonnement, l'accès s'arrête simplement sans frais. Site : https://ifg.tax · Contact : contact@ifg.tax
