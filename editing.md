# editing

The standing rule for revising material that already exists. Paste the fenced block before asking an agent to clean up, reformat, or audit-and-fix a file it did not write.

## Why this is a separate module

[core.md](core.md) governs what an agent writes from nothing. This governs what it does to something that is already finished, where only the form is in question, not the content.

The two get conflated constantly. Someone asks for a cleanup pass and gets back a rewrite, because fixing a heading level and improving a sentence feel like the same kind of work to the agent doing them. They are not the same kind of work to the person who now has to reread the whole file to find out what changed. This module exists to keep that distinction explicit instead of relying on the agent to notice it in the moment.

## Reinforce, do not introduce

A pass may correct the form of what is on the page. It may not add to what the page says.

Form is a heading at the wrong level, a list that is really a paragraph, a broken reference, leftover placeholder text, a marker in the wrong shape for where it sits. Content is a new section, a summary, an example, a definition of a term already used, or a sentence written to fill a gap the agent noticed.

The test: do the claims survive unchanged. If the material asserted five things before the pass and the same five after, it was a tidy. If it asserts six, it was a rewrite, no matter how good the sixth one is. Rephrasing a human's sentences fails the same test, because a sentence they did not write is one they now have to read and approve.

Anything the agent believes is missing goes in its reply, not in the file. If the human wants it written, they will ask, and generation rules apply from there.

## Propose before changing

Nothing is applied on the first pass, including changes that look purely mechanical. The pass reads, reports what it found, and stops.

The human approves in their reply, item by item or in a batch. The agent then applies exactly what was approved, nothing that occurred to it in between. A fix that turns out to need a different approach than the one proposed comes back as a new proposal, not a substitution.

This is slower than a formatter, on purpose. Mechanical fixes are cheap to approve in bulk. The reason to route them through the same gate anyway is that the agent does not reliably know which of its own changes are mechanical. Deciding that is the human's half of the work.

## What a pass looks for

- Structural markers out of place: headings that skip a level, a section repeated, an opening marker missing where the format expects one.
- Placeholder or template text left in material that has since been written into.
- References whose target no longer exists, or whose display text no longer matches what the target is now about.
- Content that reads as agent-authored but carries no provenance marker, or carries one in the wrong shape for where it sits.
- Generated content that has escaped its marked boundary into surrounding human material.
- Formatting drift that no deterministic tool already owns: stray whitespace, inconsistent list markers, an em dash.
- Prose broken into a list, or a list of one item.

That is the whole list. A pass reports what it found against these and says nothing about what it would have written differently.

## What a deterministic tool already owns

If a formatter or linter runs on save, proposing anything it owns wastes a reply. Check what it corrects automatically before adding an item to the list above, and drop anything it already handles. What it does not correct automatically, most often heading levels, still belongs on the list, because nothing else will catch it.

## Exceptions

A file with its own established convention, a README, a changelog, a license, is correct in its own shape, not the general one. A pass checks its references and its provenance markers, and leaves its structure alone.

An intentionally empty file, a template not yet filled in, is not incomplete. It is material not written yet.

## The block

````
Cleanup pass. Read the target named to you and report. Change nothing yet.

REINFORCE, DO NOT INTRODUCE
You may correct the form of what is on the page. You may not add to what it
says. No new sections, summaries, examples, or definitions. Do not rephrase
existing sentences. If the material asserts five things now, it asserts the
same five when you are done. Anything you think is missing goes in your
reply, not in the file.

PROPOSE FIRST
Apply nothing on this pass, including changes that look purely mechanical.
Report, then wait. Approval will come in the reply, and you apply only what
was approved, as it was described. If a fix turns out to differ from what
you proposed, propose it again before applying it.

WHAT TO LOOK FOR
Structural markers out of place: a skipped heading level, a repeated section,
a missing opening marker. Placeholder or template text left in material that
has been written into. References whose target no longer exists, or whose
display text no longer matches the target. Content that reads as
agent-authored but carries no provenance marker, or one in the wrong shape
for where it sits. Generated content that has escaped its marked boundary.
Formatting drift no deterministic tool already owns. Prose broken into a
list, or a list of one item.

That is the whole list. Do not report what you would have written
differently.

DO NOT TOUCH
Protected fields belong to the human. Propose changes to them; do not make
them. Never remove a provenance marker, and never re-date one you did not
write. Removing a marker is how the human records that they have verified
something.

HOW TO REPORT
Order findings by how much damage each does if left. Give the location, the
standard it misses, the evidence quoted briefly, and the smallest change
that would fix it. Report only what you actually found. If the target is
clean, say so in one line. Finish with what you could not check and why.
````
