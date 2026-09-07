# The HDSOP standard

Every workflow map in this repo follows the **HDSOP** (Hyperdocumented SOP) standard. Use [`_TEMPLATE.md`](./_TEMPLATE.md) to start a new one. This repo is one instance of the [Hyperdocumentation Protocol](https://truthmanagement.wiki/concepts/hyperdocumentation-protocol); the standard below is the per-workflow unit the protocol is built from.

## What makes it an HDSOP

A traditional SOP is human-only prose. An HDSOP is structurally different on five axes:

1. **Dual-readable.** A human can follow it and an agent can execute it.
2. **Branch-explicit.** Every decision point is drawn (mermaid), not buried in paragraphs.
3. **Metadata-rich.** Machine-readable frontmatter (frequency, automation potential, related skills).
4. **Cross-linked.** Wired to related work and reference materials, not standalone.
5. **Skill-extractable.** An agent can read it and crystallize its repeatable branches into skills.

## Separation-of-concerns convention

- **Steps say *what* happens.** Never mark who does each step inside the prose.
- **The flowchart color-codes *who*:** amber = irreducibly human, blue = agent-executed or agent-proposed.
- **The Automation Opportunities section holds the ROI analysis:** what is already automatable, the strongest next candidate, and the irreducibly-human core.

Actor designation never clutters the step prose.

## Naming WHICH human, when there is more than one

A map with one human in it can say `amber` and be complete, because there is only one person
the color could mean. **The moment a second human enters the process, `amber` stops carrying
information.** It says a person must act, which the reader already knew, and it does not say
which person, which is the only thing they needed. A board built from those maps reports every
blocked step to both people, and each one reads it as waiting on the other.

So: **more than one human in a workflow means every human is named.**

- **`operators:` in the frontmatter lists them**, each with the short key the map refers to
  them by. `owner:` still names the one person accountable for the workflow itself, which is a
  different question from who performs a given step.
- **The Roles table has one row per named human**, never a single generic `Human operator` row.
  A generic row in a multi-human map is the same failure as a generic color.
- **Each named human gets their own class in the flowchart**, in the amber family so the
  human-versus-agent read survives, and distinct enough that the two are separable at a glance.
  Put the key in the node label as well, because color alone fails for a colorblind reader and
  fails completely in a printout.
- **Every handoff between two humans is drawn as an edge**, labelled with what is handed over.
  The handoffs are where a multi-human process actually loses time, and a map that hides them
  behind a single amber blob cannot show you that.

A single-human map changes nothing and needs no `operators:` list. The rule fires on the second
human, never the first.

## HDSOP vs skill (map vs machine)

- A **skill** is a packaged, auto-invocable unit of agent capability (the SKILL.md contract): machine-discoverable and portable across runtimes.
- An **HDSOP** is *process truth*: the canonical, branch-explicit map of how a process actually works, followable by a human or an agent.

The relationship is **map vs machine**: the HDSOP is the doctrine; skills are machines that automate stretches of the map. One HDSOP orchestrates many skills, and skills get *quarried out of* proven HDSOPs. Document and prove the process first, then crystallize its repeatable branches into skills.

## The load-bearing step

The map an agent drafts will be confidently plausible and wrong in places. The step that cannot be skipped is **review against reality**: the operator reads the draft back against how the process truly runs and names every drift. Only the operator knows the real shape.

## How each map feeds the coverage map

Documenting or automating a workflow is not finished until [`COVERAGE.md`](./COVERAGE.md) reflects it. When a map reaches `proven`, or when a repeatable stretch gets crystallized into a skill and the automation status moves, update that workflow's row and the rollup in the same commit. The coverage map is the protocol's scoreboard; a map that is done but uncounted does not exist to the business.
