# Reference: Data Sources

The monthly report is built from three source types.

## 1. Amazon Business Report CSV

Purpose:

- product-level performance
- ordered product sales
- units ordered
- business-to-business sales and units, when available

Typical issue:

- the filename may show the download date rather than the reporting period
- product titles may be long, inconsistent, or unsuitable for management reporting

## 2. Amazon Monthly Summary PDF

Purpose:

- account-level income
- fees
- refunds
- advertising
- service charges
- transfers
- final financial reconciliation

Typical issue:

- the PDF contains the authoritative financial totals, but those totals need to be mapped into a clean report structure

## 3. SKU/ASIN Mapping

Purpose:

- convert Amazon SKU and ASIN identifiers into clean product display names
- avoid using long marketplace listing titles in the final report

Typical issue:

- new products may appear in Amazon reports before the mapping file has been updated

## Source priority

When sources disagree, do not average, merge, or guess.

Use this priority:

1. Monthly summary PDF for account-level financial totals.
2. Business report CSV for product-level totals.
3. SKU/ASIN mapping for display names.
4. QA notes for any mismatch or unresolved variance.
