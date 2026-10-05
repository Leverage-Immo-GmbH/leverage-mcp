# Leverage MCP server

Real estate investment analysis for AI agents: deal search across German portals, reproducible yield and financing figures, document extraction and due diligence.

[Leverage](https://leverage.immo) is a platform for property investors in Germany. Its MCP server lets agents such as Claude, Claude Code, Cursor and Codex work with a user's Leverage account instead of guessing from pasted text.

This repository is documentation for a hosted service. The server is not open source and there is no code to run here.

## Connect

| | |
|---|---|
| Server URL | `https://api.leverageimmo.com/mcp` |
| Transport | Streamable HTTP |
| Authentication | OAuth 2.0. The client registers itself; you sign in with your Leverage account in the browser. |

In most clients this is one step: add a remote MCP server with the URL above and complete the sign-in. A client that cannot open a browser sign-in uses a personal connector URL from the Leverage profile instead.

Setup is documented in one place, so it stays current:

- Per-client setup steps: <https://api.leverageimmo.com/agent-setup/prompt.md>
- Guide for agents: <https://api.leverageimmo.com/skill.md>
- Product page: <https://leverage.immo/en/for-ai-agents/> (German: <https://leverage.immo/fuer-ki-agenten/>)

You need a Leverage account. Some capabilities depend on your plan: <https://leverage.immo/en/pricing/>.

## What an agent can do

The server tells the client which tools it offers, so this page does not list them one by one. In short:

- **Portfolio and properties.** Read and maintain properties, units, tenancies and loans, and get key figures such as yield, cashflow and financing from the same calculations the app uses.
- **Property search.** Search listings from the major German property portals, save acquisition profiles and run search agents that keep looking.
- **Documents.** Upload exposés, leases and other property documents and get their contents back as structured fields.
- **Deal screening and due diligence.** Screen a listing against an acquisition profile and review a dataroom.
- **Routines, tasks and contacts.** Schedule recurring work and keep the people and to-dos around a property.

## Security

The server acts as the signed-in user, within that user's account and plan. Access granted to an agent can be revoked in the Leverage profile. Authentication details for agents: <https://leverage.immo/auth.md>.

## Support

Questions and feedback: <https://leverage.immo>.

---

This file is published from Leverage's main repository. Changes made here are overwritten.
