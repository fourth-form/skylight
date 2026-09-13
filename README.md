# Skylight

A small set of system instructions for working with an AI agent. Skylight is not a tool. It is a stance: what an agent may write, how that writing is marked, and what it never touches.

Skylight names no vendor and assumes no client. Paste it into a chat, drop it in a project's instruction file, or hand it to a coding agent. It works the same way everywhere.

## Philosophy

Two default beliefs, in tension, resolved the same way every time.

An agent is capable of writing well. It should still write only where it has been let in, and most of what it writes should say so. Authorship is not a technicality; it decides what a person has to read and approve before trusting it.

Revision is not generation. An agent fixing the form of something should not use the chance to also improve its content. Those are different requests, and conflating them is how a five-line cleanup becomes a rewrite nobody asked for.

Neither belief is about distrust of the agent. Both are about keeping the human's read of their own material cheap. A stamp says what has not been checked yet. A boundary says what was not supposed to move.

## Use

Three modules, each self-contained:

- **[core.md](core.md)**, the default stance. It covers authorship, provenance, protected fields, formatting, and working style.
- **[editing.md](editing.md)**, the standing rule for revising material that already exists.
- **[review.md](review.md)**, a read-only audit against Skylight's standards.

Each file is fenced as a single paste-able block, with the reasoning around it left outside the fence.

## Install

There is nothing to install in the usual sense. Two ways to bring Skylight into a session:

1. Paste `core.md`'s block as the first message, before asking an agent for anything else. Add `editing.md` or `review.md` in the same way for a session that needs that mode.
2. Save the files in a project and reference `core.md` from that project's own instruction file, a system prompt, an `AGENTS.md`, a `CLAUDE.md`, so every session in that project starts from it automatically. Point a session at `editing.md` or `review.md` only when that session needs that mode.

## Limits

Skylight is instructions, not enforcement. Nothing here checks that an agent actually followed a rule, and an agent can still drift. The [review.md](review.md) module catches drift only as well as the read behind it; staleness and reference checks need real reading, not pattern matching, and are the most likely to miss something. Effectiveness depends on the agent reading and following plain instructions reliably, which no single model or tool guarantees.

## Privacy

Skylight is plain text. It has no code, makes no network requests, and collects nothing. Pasting it into a session adds only the words in the block.

## Develop

Plain markdown, no build step. Edit a module directly, and keep its fenced block self-contained per [AGENTS.md](AGENTS.md).

## License

MIT, see [LICENSE](LICENSE).
