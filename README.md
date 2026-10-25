# Evaboot plugin for Grok and Cursor

Evaboot turns LinkedIn Sales Navigator into a clean lead list. Describe the people you want to reach, and Evaboot builds the Sales Navigator search, exports the leads and accounts it returns, then finds and verifies each lead's professional email. Finished exports can be pushed to a CRM or webhook you connect.

You need an Evaboot account and an active Sales Navigator seat. Exports and email lookups use the credits in your Evaboot plan.

## Install

- **Grok Bot and Cursor:** open Connect Apps (Grok Bot) or the Cursor Marketplace, search for **Evaboot** and add it.
- **Grok Build:** open Plugins, search for **Evaboot** and install it, or run `grok plugin install https://github.com/evaboot-labs/evaboot-grok-plugin.git`.

On first use, sign in with your Evaboot account on the OAuth consent page.

Without the plugin, add the server as a custom connector: `https://mcp.evaboot.com/mcp`.

## What the plugin runs, sends and fetches

- **One remote MCP server**, `https://mcp.evaboot.com/mcp`, run by Evaboot. You sign in with your Evaboot account over OAuth; no API key is stored in the plugin. The agent sends the tool calls you ask for (search descriptions, names and company domains to look up, export ids) to that server, and the server returns your searches, exports, leads and email results. It only reaches data that belongs to your Evaboot account.
- **Four skills**, plain instructions with no scripts, binaries or network calls of their own. They use the Evaboot tools above and two local files in your home directory:
  - `define-icp-and-value-prop` interviews you and writes `~/.evaboot/EVABOOT-ICP.md` and `~/.evaboot/EVABOOT-VALUE-PROP.md`.
  - `qualify-leads` reads `~/.evaboot/EVABOOT-ICP.md` and labels each lead in, out or can't tell.
  - `intent-detection` lists the last 7 days of Sales Navigator lead and account alerts.
  - `write-outreach-messages` reads `~/.evaboot/EVABOOT-VALUE-PROP.md` and drafts one first message per person. It never sends anything.

No hooks, commands or local servers. Nothing else is installed, run in the background, or sent to any other service.

The full tool list is documented at https://github.com/evaboot-team/evaboot-mcp.

## Support

Help center: https://help.evaboot.com. Email: support@evaboot.com. Privacy policy: https://evaboot.com/privacy-policy. Terms: https://evaboot.com/terms-of-service.

## License

MIT
