<p align="center">
  <a href="https://inkujapanese.com/">
    <img src="https://inkujapanese.com/share/sumi-loop-20261024.jpg" width="760" alt="Learn Japanese that sticks. Sumi, the Inku mascot.">
  </a>
</p>

<h1 align="center">Inku: Learn Japanese with Flashcards</h1>

<p align="center">
  Look up words in Inku’s curated library, save them to your decks, and review in your AI chat.
</p>

<p align="center">
  <a href="https://inkujapanese.com/library">Japanese library</a> ·
  <a href="https://inkujapanese.com/mcp">Inku MCP</a> ·
  <a href="https://inkujapanese.com/docs/agents/setup">Setup guide</a>
</p>

## Install the skill

```sh
npx skills add inkujapanese/Inku-skills --skill inku-japanese
```

Choose your client when the installer prompts you. For manual installation, copy the [`inku-japanese` skill folder](skills/inku-japanese/) into the skills directory your client uses. The [skill instructions](skills/inku-japanese/SKILL.md) show the agent how to look up Japanese and work with your Inku library.

## Connect your Inku account

The skill is free to install. The hosted MCP connector requires active Inku Pro, including an active trial or complimentary Pro. Use an AI client that supports remote MCP and browser OAuth.

| Client | Add Inku |
| --- | --- |
| Codex CLI | Run `codex mcp add inku-japanese --url https://inkujapanese.com/api/mcp`. If Codex asks you to sign in again, run `codex mcp login inku-japanese`. [Codex MCP docs](https://learn.chatgpt.com/docs/extend/mcp?surface=cli) |
| Claude | Add a custom web connector named **Inku Japanese** with the URL below. [Claude connector setup](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp) |
| Cursor | Add a remote MCP server in **Customize → MCPs** or add a server entry with the URL below in `mcp.json`. [Cursor MCP docs](https://cursor.com/docs/mcp) |
| Another remote MCP client | Add a custom connector with the URL below and follow the authorization prompts. [Inku setup guide](https://inkujapanese.com/docs/agents/setup) |

```text
https://inkujapanese.com/api/mcp
```

Sign in to Inku in your browser and approve read access for the first lookup. Choose write access when you want your agent to change your library or record reviews.

## Try it

> Look up きっぷ in Inku and show me its reading and meaning. Use read-only tools.

Look for **きっぷ** (*kippu*), meaning **ticket**. Try a workflow once that lookup works.

| Workflow | Prompt to try |
| --- | --- |
| Look up vocabulary | “Find polite ways to ask for directions in Inku. Give me three phrases and their readings.” |
| Save a word to a deck | “Find きっぷ in Inku and save the existing card to my Japan trip deck. Ask me if you find more than one match.” |
| Check study progress | “How many cards are due for review? Keep this read-only.” |
| Review in chat | “Quiz me on the words in my Japan trip deck. Show one card at a time and wait for my answer before revealing the meaning.” |

## What your agent can do

- **Search and read** curated or custom cards, decks, and study progress.
- **Organize your library** by saving cards, managing personal decks, and adding or editing custom cards.
- **Study and review** using Inku’s review scheduler after you answer.
- **Export your library** as JSON or vocabulary CSV and undo supported edits.

See [Inku’s agent reference](https://inkujapanese.com/agent) for tool names, permissions, and undo rules.

## Manage access

Open **Profile → API keys** in Inku to disconnect an AI app. Use your AI client’s connector settings to remove its local connection. [Inku privacy policy](https://inkujapanese.com/privacy) · [Contact Inku](https://inkujapanese.com/contact)
