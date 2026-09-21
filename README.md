# Forest inventory valuation

A browser tool that turns a forest inventory PDF (Latvian State Forest Register, «Nogabalu raksturojošie rādītāji») into a clear-cut valuation.

Drop the PDF into the page. The tool then:

- finds the stands that meet the clear-cut age or diameter limits;
- calculates the harvestable volume by species;
- splits it into timber assortments and prices them;
- subtracts harvesting, forwarding and transport costs and a profit margin;
- shows the maximum purchase price for the property.

All calculations run on your computer. The PDF is never uploaded anywhere.

## How it works

- **Rules, not AI.** The same PDF always gives the same result, and every number can be traced back to the document.
- **Columns found by header words**, not by fixed positions. Documents with a different column order, missing columns or a different decimal separator still work.
- **Built-in checks.** Stand areas are reconciled against the document total and species formulas must sum to 10. If something does not add up, the report shows a red warning instead of a silently wrong total.
- **Everything is editable.** Prices, costs, cutting limits and misread values can be changed in the page, and the result updates immediately.
- **Single HTML file**, no install, no server. It only needs internet access to load the PDF reading library (pdf.js).

## How to run

Double-click `cirsmas_vertibas_aprekins.html` (Chrome or Edge) and drop in any PDF from `testa_dati/`.

## Contents

| File | What it is |
|---|---|
| `cirsmas_vertibas_aprekins.html` | The tool (one file, Latvian interface) |
| `1.uzdevums_INFO.pdf` | Description, step-by-step guide with screenshots, test results (Latvian) |
| `testa_dati/testa_objekts_99990030117.pdf` | Fictional property, 2 blocks, 2 pages: 121 653 EUR |
| `testa_dati/variants_*.pdf` | The same data in different layouts; the result must stay the same |
| `testa_dati/kluda_*.pdf` | Error cases: no volume column, scanned PDF without text |

All test properties are fictional.
