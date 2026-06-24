# Rules

## Core rule

Route the request through the monthly report workflow before doing analysis.

The user should only need to provide:

- marketplace
- reporting month
- source files

Original source files should be placed in `INBOX/`.

## Source of truth

- Account-level financial totals come from the Amazon monthly summary report.
- Product-level performance comes from the Amazon business report CSV.
- Clean product names come from SKU/ASIN mapping.
- The user-stated reporting month and marketplace are authoritative unless source evidence clearly conflicts.

## Raw file safety

- Never edit raw Amazon downloads.
- Never overwrite raw files.
- Never rename the user's original files.
- Stage copies into the working report folder when processing is needed.

## Month handling

Amazon download filenames may include the date the report was downloaded or generated. That date is not necessarily the reporting period.

Do not infer the reporting month from a filename such as:

```text
BusinessReport-6-22-26.csv
```

This filename may show when the report was downloaded, not the month being reported.

If the user says:

```text
Run the Amazon USA monthly report for April 2026.
```

then April 2026 is the target reporting period.

The correct pattern is:

```text
Drop files into INBOX/.
Run the Amazon USA monthly report for April 2026.
```

## Conflict handling

Stop and ask for clarification when:

- the requested month conflicts with the monthly summary report period
- more than one possible source file pair exists
- the marketplace is missing or unclear
- required source files are missing
- SKU/ASIN mapping cannot identify a product cleanly

## QA requirement

Do not call a report final until QA notes exist.

QA should check:

- product revenue totals
- unit totals
- financial subtotal reconciliation
- unmatched SKU/ASIN mappings
- missing or conflicting source files
- visible notes for any variance

## Scope limits

Do not:

- rebuild the workflow unless it is missing or broken
- invent missing financial lines
- invent product names
- edit raw reports
- make marketplace strategy recommendations unless separately requested
- include private business data in public examples
