# workflows

One folder per critical workflow. Each folder holds the map, the ground truth it was built from, and the sources it depends on.

```
workflows/<workflow-slug>/
├── HDSOP.md         # the readable map (the doctrine), written to HDSOP-STANDARD.md
├── working-notes.md # the running interview capture and ground truth the map is built from
└── references/      # every source the workflow depends on (docs, letters, decks, screenshots)
```

Conventions:

- **Slug is kebab-case** and names the workflow, not the department (e.g. `qualify-inbound-lead`, not `sales`).
- **Every workflow here has a row in [`../COVERAGE.md`](../COVERAGE.md).** The folder is where the map lives; the coverage map is where its status is tracked.
- **`_example-qualify-inbound-lead/` ships as an illustration.** Delete it once you have your own workflows mapped.
