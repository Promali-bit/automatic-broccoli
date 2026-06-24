# Examples

## Valid trigger phrases

Before these requests, the user places the original Amazon downloads in `INBOX/`.

```text
Run the Amazon USA monthly report for March 2026.
```

Expected behavior:

- Use USA as the marketplace.
- Use March 2026 as the reporting period.
- Look for the required Amazon source files.
- Do not ask the user to paste the full instructions again.

```text
Run April 2026 Amazon report for Canada.
```

Expected behavior:

- Use Canada as the marketplace.
- Use April 2026 as the reporting period.
- Check that the source files match the requested month.

```text
Check whether April USA files are ready.
```

Expected behavior:

- Inspect available source files.
- Report what is present and what is missing.
- Do not build the final report unless the user asks.

```text
Re-run March 2026 USA report.
```

Expected behavior:

- Check whether a final report already exists.
- Ask before overwriting or replacing previous outputs.

## Ambiguous request

```text
Run the monthly Amazon report.
```

Expected response:

```text
Which marketplace and reporting month should I use?
```

## Conflicting source evidence

User request:

```text
Run the Amazon USA report for April 2026.
```

Available monthly summary:

```text
2026Mar1-2026Mar31CustomUnifiedSummary.pdf
```

Expected response:

```text
I found a conflict. You requested April 2026, but the monthly summary appears to be for March 2026. Please confirm the correct file or reporting month before I continue.
```

## Native Amazon filenames

Amazon may provide files with names like:

```text
BusinessReport-6-22-26.csv
2026Apr1-2026Apr30CustomUnifiedSummary.pdf
```

Expected behavior:

- Do not require the user to rename these files manually.
- Use the requested reporting month and file contents to identify the correct pair.

## Inbox workaround

Problem:

```text
BusinessReport-6-22-26.csv
```

This filename does not prove the report is for June 2026. It may only show when the file was generated or downloaded.

Workflow:

```text
1. User drops the original Amazon files into INBOX/.
2. User says: Run the Amazon USA monthly report for April 2026.
3. Specialist treats April 2026 as the target month.
4. Specialist copies the raw files into the month folder and leaves INBOX originals unchanged.
```

Why this is better:

- no manual renaming
- no unsafe month guessing
- less repeated instruction
- raw files remain untouched
