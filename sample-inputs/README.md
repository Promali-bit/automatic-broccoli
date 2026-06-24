# Amazon Monthly Report Specialist

This is a folder-based specialist for turning monthly Amazon marketplace downloads into a clean management report.

It is designed for a real recurring business workflow that used to take a team around two days each month: Amazon source files need to be interpreted, matched, checked, and converted into a useful summary without rebuilding the process or re-explaining the instructions.

## What this specialist does

- Accepts Amazon monthly source files.
- Preserves raw downloads unchanged.
- Uses the user-stated marketplace and month as the report target.
- Separates financial/account-level data from product-level data.
- Applies product-name cleanup using SKU/ASIN mapping.
- Produces a traceable report summary.
- Creates QA notes before treating output as final.

## How to use it

1. Drop original Amazon downloads into `INBOX/`.
2. State the marketplace and reporting month in the request.
3. Read `brief.md` first to understand the client problem.
4. Read `identity.md` to understand the specialist role.
5. Read `rules.md` before doing any work.
6. Use `examples.md` to understand valid request patterns.
7. Use the files in `reference/` as the operating context.

Example request:

```text
Run the Amazon USA monthly report for April 2026.
```

The specialist should then identify the source files, check for ambiguity, stage copies of raw inputs, extract the needed data, perform QA, and produce the final report output.

## Folder map

```text
amazon-monthly-report-specialist/
├── brief.md
├── README.md
├── identity.md
├── rules.md
├── examples.md
├── INBOX/
│   └── README.md
├── reference/
│   ├── data-sources.md
│   ├── file-intake.md
│   ├── product-name-mapping.md
│   ├── qa-checklist.md
│   └── report-layout.md
├── sample-inputs/
│   ├── README.md
│   └── sample-file-names.md
└── sample-output/
    └── example-report-summary.md
```

## Design principle

The folder is the interface.

The markdown files define the specialist's identity, rules, examples, and references. The user does not need to remember the full workflow each month. They only need to state the marketplace, month, and provide the source files.

The `INBOX/` folder exists because Amazon filenames are not reliable enough to use as the only source of truth. The user drops files there, then states the target month and marketplace. That small human input prevents the specialist from guessing.
