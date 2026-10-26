# What the plugin runs, sends and fetches

- **One remote MCP server**, `https://mcp.evaboot.com/mcp`, run by Evaboot. You sign in with your Evaboot account over OAuth; no API key is stored in the plugin. The agent sends the tool calls you ask for (search descriptions, names and company domains to look up, export ids) to that server, and the server returns your searches, exports, leads and email results. It only reaches data that belongs to your Evaboot account.
- **Four skills**, plain instructions with no scripts, binaries or network calls of their own. They use the Evaboot tools above and two local files in your home directory:
  - `define-icp-and-value-prop` interviews you and writes `~/.evaboot/EVABOOT-ICP.md` and `~/.evaboot/EVABOOT-VALUE-PROP.md`.
  - `qualify-leads` reads `~/.evaboot/EVABOOT-ICP.md` and labels each lead in, out or can't tell.
  - `intent-detection` lists the last 7 days of Sales Navigator lead and account alerts.
  - `write-outreach-messages` reads `~/.evaboot/EVABOOT-VALUE-PROP.md` and drafts one first message per person. It never sends anything.

No hooks, commands or local servers. Nothing else is installed, run in the background, or sent to any other service.

The full tool list is documented at [evaboot-team/evaboot-mcp](https://github.com/evaboot-team/evaboot-mcp).

## Support

Help center: [help.evaboot.com](https://help.evaboot.com). Email: support@evaboot.com. [Privacy policy](https://evaboot.com/privacy-policy). [Terms](https://evaboot.com/terms-of-service).

Back to the [README](../README.md).
