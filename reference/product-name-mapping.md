# Reference: Product Name Mapping

Amazon product titles are often too long or inconsistent for management reports.

The report should use clean product names from a SKU/ASIN mapping table whenever possible.

## Mapping fields

Recommended fields:

```text
Marketplace
SKU
ASIN
Clean Product Name
```

## Matching order

Use this matching order:

1. SKU and marketplace
2. ASIN and marketplace
3. SKU only, if marketplace is unavailable and the match is unique
4. ASIN only, if marketplace is unavailable and the match is unique

## If no match is found

Do not invent a product name.

Use a clear placeholder and record the issue in QA notes:

```text
Unmapped product: SKU [value], ASIN [value]
```

## Final report rule

The final product performance table should show clean product names, not long Amazon listing titles, unless no mapping is available.
