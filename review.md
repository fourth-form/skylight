# review

A read-only audit. Paste the fenced block, then name the target: a file, a folder, or a whole project. The agent reports where it has drifted from Skylight's standards. It changes nothing.

## Why read-only

An audit that fixed what it found would have to break the rules it is checking for, editing protected fields, removing another author's provenance marker, rewriting human prose outside a marked boundary, to do the fixing. Keeping it read-only is not extra caution. It is the only way the check and the rule it enforces do not contradict each other.

## Scope

This checks conformance, not quality. It will report a heading that skips a level or a marker in the wrong shape. It will not report that a section is unconvincing or that the structure of an argument is wrong. Use [editing.md](editing.md) once conformance findings need fixing, and a human's own judgment for everything past that.

Staleness and reference checks need real reading, not pattern matching, so they are the two most likely to miss something. Treat a clean result on those as weak evidence, not proof.

## The block

````
Review. Audit the target named to you against the standards below. Read only:
report and propose, change nothing.

WHAT TO CHECK

Provenance. Agent-authored content carries a marker naming the model and a
date. Flag content that reads as agent-authored but carries no marker, a
marker in the wrong form for where it sits, and a marker whose date or model
name contradicts what the material says happened.

Containment. Outside its open ground, agent-authored content stays inside its
marked boundary, with surrounding human material left alone. Flag generated
content that has escaped that boundary.

Protected fields. These should match whatever the project's own convention
establishes as human-owned. Flag values that look invented, reordered, or
rewritten by an agent. Propose changes; never assume them.

Formatting. Structural markers, most often heading levels, should step down
without skipping. Prose comes first, and lists appear only where the content
is really a list. Flag an em dash anywhere.

Placeholders. Flag template or placeholder text left in material that is
otherwise finished.

References. Flag links or references whose target does not exist, and ones
whose display text no longer matches what the target is now about.

Staleness. Flag claims contradicted elsewhere in the target, instructions
referring to something that no longer exists, and open questions recorded as
open that the material later answers.

HOW TO REPORT

Order findings by how much damage they do if left. A wrong provenance marker
outranks a heading level, because the marker is what tells a human whether
they have verified something.

For each finding, give the location, the standard it misses, the evidence
quoted briefly, and the smallest change that would fix it.

Report only what you actually found. If the target is clean, say so in one
line. Do not pad a short report, do not restate the standards back, and do
not raise a preference that no standard here covers. A short accurate audit
is worth more than a long thorough-looking one.

Finish with anything you could not check and why, so the edges of the pass
are known.
````
