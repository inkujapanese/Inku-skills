---
name: inku-japanese
description: Use Inku Japanese to look up Japanese words and phrases, study from Inku flashcards, check review progress, and organize the learner's Inku decks. Use when the learner asks to connect Inku or to search, save, or review with their Inku library.
---

# Inku Japanese

## Connect and verify

- Use the connected Inku MCP tools. If they are unavailable, share the [Inku setup guide](https://inkujapanese.com/docs/agents/setup) and wait for the learner to connect Inku themselves. The learner controls client settings and approves access in their browser. Keep credentials and tokens out of the chat.
- Inku tool access requires active Inku Pro, including an active trial or complimentary Pro. If the connection or plan check fails, explain the next step and stop the tool workflow until access works.
- For a first connection check, call `inku_search_cards` for `きっぷ` and show the reading and meaning returned by Inku. Expect a match for `きっぷ`, meaning “ticket.” Keep the check read-only and ungraded.

## Look up and study

- Search the catalog before proposing a new card. Use the reading and meaning returned by Inku. Label examples you write yourself as practice examples.
- Use `inku_get_progress` to report study progress on request. Keep vocabulary lookup and casual practice read-only.
- Start a recorded review only when the learner requests one. Present one prompt at a time and wait for a genuine recall attempt before recording the answer with `inku_answer_review`. Show the meaning after their attempt.

## Update the learner's library

- Use the current Inku tool descriptions and the learner's write permissions. Confirm the target deck or card if it is ambiguous.
- Reuse the existing card when the learner wants a catalog match in their deck. Use custom cards for new content. Treat curated card content as read-only.
- Read the current deck or card before changing it. Use the revisions required by the tool. If a change reports a conflict, read the current state before proposing another edit.
- Use write tools only for changes the learner requests. Ask for explicit confirmation before deleting a card, removing cards in bulk, or changing recorded progress. Keep browsing and practice read-only by default.
- Report what changed using the tool result. Include the available undo option when the tool returns one. The [agent reference](https://inkujapanese.com/agent) explains library changes, review, and undo.
