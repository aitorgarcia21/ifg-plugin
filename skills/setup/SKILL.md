---
name: setup
description: Connect the IFG tax sources MCP server (sign-in with an IFG account) and check that it works.
---

# Setting up IFG

1. The plugin declares the remote MCP server `https://ifg.tax/v1/mcp` (Streamable HTTP).
2. On first use, the client opens the IFG sign-in page (OAuth 2.1 with PKCE). Sign in with an IFG account (plans: https://ifg.tax).
3. Check the connection: call `search_authority` with `query: "CGI 145"` and `jurisdiction: "FR"`, then `get_authority` on the returned id. A text with `verification: verified` and a clickable `citation.markdown` means the connection works.
4. Support: contact@ifg.tax. Privacy policy: https://ifg.tax/politique-confidentialite-en
