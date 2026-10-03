# IFG for Claude

**The right tax text, at the right date, in your AI** — with applicability status, versions and a clickable official link.

IFG connects Claude to official tax sources for **France** and its neighbours (**Luxembourg, Switzerland, Belgium, Germany, Monaco, Andorra, Italy**), their **tax treaties** (including MLI effects), **EU** tax law and **OECD** guidance: codes and laws, administrative doctrine, rulings, case law, forms and parliamentary work.

- Every text comes from its official publisher, with `verification: verified` and a citation link carrying the version date.
- Point-in-time reading: the version applicable on the date of the tax event, with past and announced future changes.
- Honest gaps: a missing or unproven text is reported as an explicit gap, never invented.

## What the plugin contains

- **MCP server** `ifg` → `https://ifg.tax/v1/mcp` (Streamable HTTP, OAuth 2.1). Four tools: `search_authority`, `get_authority`, `changes_since`, `browse_instrument`.
- **Skill `tax-research`** (`/ifg:tax-research`): the research method (find, read at the right date, cite, respect gaps).
- **Skill `setup`** (`/ifg:setup`): sign-in and connection check.

After installing, connect IFG once: **Customize → Connectors → IFG → Connect** on claude.ai (https://claude.ai/customize/connectors), or `/mcp` in Claude Code. An IFG account is required: 7-day free trial, nothing charged today. Plans: https://ifg.tax — Support: contact@ifg.tax — Privacy: https://ifg.tax/privacy-policy

IFG is a documentary infrastructure: the professional and their assistant remain responsible for the legal analysis and conclusion.

---

# IFG pour Claude

**Le bon texte fiscal, à la bonne date, dans votre IA** : statut d'applicabilité, versions et lien officiel cliquable, pour la France, ses voisins (Luxembourg, Suisse, Belgique, Allemagne, Monaco, Andorre, Italie), les conventions fiscales, le droit de l'Union et l'OCDE. Après l'installation, connectez IFG une fois : **Personnaliser → Connecteurs → IFG → Connecter** sur claude.ai (https://claude.ai/customize/connectors), ou `/mcp` dans Claude Code. Un compte IFG est nécessaire : essai gratuit de 7 jours, aucun débit aujourd'hui. https://ifg.tax
