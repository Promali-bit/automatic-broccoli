# Brief: Amazon Monthly Report Specialist

Every month my team downloads Amazon marketplace reports for my ecommerce business and turns them into a management report. This used to take around two days because Amazon files arrive with names based on download dates, not reporting periods; financial totals live in one report while product performance lives in another; product names need to be cleaned through SKU/ASIN mapping; and the same instructions had to be remembered every month.

I tried handling this with repeated prompts, manual file renaming, and memory-based instructions, but that created friction and risk. The workflow was easy to forget, easy to mislabel, and too dependent on me explaining the process again each time.

The biggest setback was file intake. I could not safely infer the reporting month from Amazon's Business Report filename, so the workaround became an `INBOX/` folder plus a simple command-style request where I state the marketplace and month.

I need a folder-based specialist that knows how to intake Amazon monthly report files, route them through a repeatable workflow, preserve raw downloads, apply product-name mapping, run QA checks, and produce a clean monthly sales report. The specialist should not guess when source files conflict, should not edit raw reports, and should only ask questions when the month, marketplace, or inputs are ambiguous.

The goal is to make the monthly report process boring: drop in the files, state the marketplace and month, and receive a clean report with traceable sources and QA notes.
