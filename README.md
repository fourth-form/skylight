# Skylight

A small set of system instructions for working with an AI agent. Skylight is not a tool. It is a stance: what an agent may write, how that writing is marked, and what it never touches.

Skylight names no vendor and assumes no client. Paste it into a chat, drop it in a project's instruction file, or hand it to a coding agent. It works the same way everywhere.

## Use

Three modules, each self-contained:

- **[core.md](core.md)**, the default stance. Paste this first, before asking an agent for anything. It covers authorship, provenance, protected fields, formatting, and working style.
- **[editing.md](editing.md)**, the standing rule for revising material that already exists. Paste this before asking an agent to clean up or reformat a file it did not write.
- **[review.md](review.md)**, a read-only audit. Paste this to have an agent check a file, a folder, or a project against Skylight's standards without changing anything.

Each file is fenced as a single paste-able block, with the reasoning around it left outside the fence.

## Philosophy

Two default beliefs, in tension, resolved the same way every time.

An agent is capable of writing well. It should still write only where it has been let in, and most of what it writes should say so. Authorship is not a technicality; it decides what a person has to read and approve before trusting it.

Revision is not generation. An agent fixing the form of something should not use the chance to also improve its content. Those are different requests, and conflating them is how a five-line cleanup becomes a rewrite nobody asked for.

Neither belief is about distrust of the agent. Both are about keeping the human's read of their own material cheap. A stamp says what has not been checked yet. A boundary says what was not supposed to move.

## License

MIT, see [LICENSE](LICENSE).
