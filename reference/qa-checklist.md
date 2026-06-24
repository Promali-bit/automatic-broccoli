# Reference: QA Checklist

Before the report is final, create QA notes.

## File checks

- Business report CSV is present.
- Monthly summary PDF is present.
- Requested marketplace is known.
- Requested reporting month is known.
- Source files do not obviously conflict with the requested month.

## Product checks

- Product rows were extracted from the business report.
- Unit totals were calculated.
- Revenue totals were calculated.
- B2B units and revenue were included when available.
- SKU/ASIN mapping was applied.
- Unmapped products were listed.

## Financial checks

- Income lines were extracted from the monthly summary.
- Expense lines were extracted from the monthly summary.
- Refunds, rebates, advertising, service fees, and adjustments were not silently dropped.
- Gross income was calculated.
- Any variance was explained.

## Final output checks

- Report title includes marketplace, month, and year.
- Income and expense section is readable.
- Product performance section is readable.
- Negative values are visually distinguishable.
- QA notes are saved before final output is marked complete.

## Completion rule

If QA notes do not exist, the report is not final.
