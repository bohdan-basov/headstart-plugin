# Headstart

Headstart finds your next clients on X. This plugin gives Claude and ChatGPT one skill, `find-leads`, and the `headstart` connector it uses. Tell your model what you sell and who buys it; it searches X for people whose posts show they need that right now, reads the profile behind every name, and hands you ten people worth a look, ranked, each with the why. You write every message yourself.

## Install

**Claude (claude.ai, Desktop, Cowork).** Customize → Plugins → Add → Add marketplace, paste `bohdan-basov/headstart-plugin`, add Headstart. On the plugin's Connectors tab connect `headstart`. First use opens the sign-in.

**Claude Code.**

```
claude plugin marketplace add bohdan-basov/headstart-plugin
/plugin install headstart@headstart
```

**ChatGPT.** chatgpt.com/plugins → + → Add custom MCP server: name `Headstart`, URL `https://mcp.useheadstart.ai`, authentication OAuth, create as a plugin and install it. Then Settings → Personal Skills → upload a ZIP of the `skills/find-leads/` folder (the folder at the archive root; the release page of this repo carries a ready one).

## What this plugin does with data

- It talks to one server, `https://mcp.useheadstart.ai`, over HTTPS.
- It sends that server the search queries and the X handles the skill asks for, nothing else from your chat.
- The server fetches public X posts and public X profiles and returns them to your model.
- The server keeps your sign-in, and writes one log line per tool call: the tool, its arguments (the query or the handle), your customer id, timing, the size of the result and what the call cost. It does not store the posts or profiles it returns, and it never sees your chat.
- Your credit balance is held in Autumn (useautumn.com), a billing ledger: it holds your customer id, name, email and balance, and the server passes those to it.
- Nothing is read from your files, your memory or your other chats.
- Each search or profile read costs one credit; checking the balance is free. Credits are granted by hand for now: message Bohdan on X ([@bohdanbasov](https://x.com/bohdanbasov)).

## Files

- `skills/find-leads/SKILL.md` and `skills/find-leads/agents/openai.yaml`: the skill, byte for byte the text in the Headstart repo's `docs/skills/find-leads.md`.
- `plugin.json`, `mcp.json`: the Agent Plugins manifests ChatGPT and Codex read.
- `.claude-plugin/plugin.json`, `.claude-plugin/marketplace.json`, `.mcp.json`: what Claude reads.

MIT licensed.
