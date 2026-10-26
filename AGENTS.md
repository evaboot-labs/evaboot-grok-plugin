# Agent instructions

This repo is the Evaboot plugin: Evaboot's hosted MCP server (`https://mcp.evaboot.com/mcp`, configured in `.mcp.json`) plus five skills in `skills/`. Together they turn a description of the user's buyers into Sales Navigator leads with verified emails, qualified against the user's ICP, with a first message drafted for each.

1. Install the plugin for the client you run in, after the user confirms:
   - Claude Code: `claude plugin marketplace add evaboot-labs/evaboot-plugin`, then `claude plugin install evaboot-plugin@evaboot-labs-evaboot-plugin`.
   - Codex, Cursor and other agents: `npx skills add evaboot-labs/evaboot-plugin`, then connect the MCP server as `docs/connect-your-agent.md` says for that client.
2. Have the user sign in to Evaboot when the client opens the OAuth page. If they have no account, send them to `https://dash.evaboot.com/accounts/signup/?last_click_origin=evaboot-plugin-repo`. Tell them to restart the session if the client needs it to load new skills or servers.
3. Check the connection with the `get_daily_export_quota` tool. If it fails, follow `docs/connect-your-agent.md`.
4. Follow `skills/define-icp-and-value-prop/SKILL.md` step by step.
5. Then offer the other skills, in this order: `build-pipeline`, `intent-detection`, `qualify-leads`, `write-outreach-messages`.

Confirm with the user before every call that saves, exports, spends credits or changes anything. Never ask for or handle an API key in the chat: OAuth sign-in needs none. Never send a message to a prospect. Never commit `.env`.
