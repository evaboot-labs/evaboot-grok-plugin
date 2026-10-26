# Connect your agent by hand

The prompt in the README does all of this for you. These are the same steps, for when you want to do them yourself.

1. **Create your Evaboot account** at [dash.evaboot.com](https://dash.evaboot.com/accounts/signup/?last_click_origin=evaboot-plugin-repo) and install the [Chrome extension](https://dash.evaboot.com/install/) to connect Sales Navigator.
2. **Install the plugin or the skills.**
   - **Claude Code:** `/plugin marketplace add evaboot-labs/evaboot-plugin`, then `/plugin install evaboot-plugin@evaboot-labs-evaboot-plugin`. The plugin brings the MCP server with it.
   - **Codex, Cursor and other agents:** `npx skills add evaboot-labs/evaboot-plugin`.
   - **Grok Build:** `grok plugin install https://github.com/evaboot-labs/evaboot-plugin.git`.
3. **Connect the Evaboot MCP server**, `https://mcp.evaboot.com/mcp`, and sign in with your Evaboot account when the browser opens:
   - **Claude Code:** done by the plugin. Run `/mcp` and pick `evaboot` to sign in.
   - **Codex:** `codex mcp add evaboot --url https://mcp.evaboot.com/mcp`, then `codex mcp login evaboot`.
   - **Cursor:** add the server to your MCP config:
     ```json
     { "mcpServers": { "evaboot": { "url": "https://mcp.evaboot.com/mcp" } } }
     ```
   - **Claude, ChatGPT or Grok on the web:** add `https://mcp.evaboot.com/mcp` as a custom connector.
   - **A client without OAuth:** send the header `Authorization: Bearer <your key>`, with the key from [dash.evaboot.com/dash/api/](https://dash.evaboot.com/dash/api/).
4. **Check:** ask your agent "What is my Evaboot export quota?". It answers with your remaining exports and credits.

Then ask your agent: **"Define my ICP and value prop."**

Back to the [README](../README.md).
