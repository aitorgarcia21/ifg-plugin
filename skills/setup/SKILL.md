---
name: setup
description: Connect the IFG tax sources MCP server (sign-in with an IFG account) and check that it works.
---

# Setting up IFG

1. The plugin declares the remote MCP server `https://ifg.tax/v1/mcp` (Streamable HTTP). Installing the plugin does not connect it: the user connects it once.
2. Connect it:
   - claude.ai (web, desktop, mobile) and Cowork: open **Customize -> Connectors** (https://claude.ai/customize/connectors), find **IFG** and click **Connect**.
   - Claude Code: run `/mcp`, choose `ifg`, then authenticate.
   The IFG sign-in page opens (OAuth 2.1 with PKCE): create an account (7-day free trial, no card required; to continue afterwards, €99 excl. VAT per month, no commitment) or sign in. Back in Claude, IFG is connected.
3. Check the connection: call `search_authority` with `query: "CGI 145"` and `jurisdiction: "FR"`, then `get_authority` on the returned id. A text with `verification: verified` and a clickable `citation.markdown` means the connection works.
4. Support: contact@ifg.tax. Privacy policy: https://ifg.tax/privacy-policy. Terms: https://ifg.tax/terms-and-conditions. Security: https://ifg.tax/security.
