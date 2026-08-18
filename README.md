# Vendor TDS Calculator

Single-page calculator: pick a **vendor / company**, enter the **inclusive-GST amount** (decimals allowed), and get **Net-of-GST**, **TDS (rounded to integer)**, and the **Payable-to-Vendor** amount.

## Formula

- `exclusive = inclusive / (1 + GST%)`
- `TDS = round(exclusive * TDS%)`  (rounded to integer)
- `payable = inclusive - TDS`

## Use

Open `index.html` in any browser. No build, no dependencies. Rates persist in the browser (`localStorage`).

## Default vendor rates (seeded from the source sheet)

| Vendor / Company | GST | TDS |
|---|---|---|
| Noida Stallion | 18% | 1% |
| CA - Slash | 18% | 10% |
| Noida Industra | 18% | 1% |
| Vinayak Industries | 18% | 0% |
| ROOMSTYLE | 18% | 0% |
| M K ENTERPRISES | 18% | 0% |
| SHANKAR THAKUR | 0% | 0% |

Notes:
- GST% for **Goods / Material** (18%) and **House Rent** (0%) were not given in the source sheet — they are editable assumptions in the UI.
- Stallion Firemen / HK were consolidated into a single **Noida Stallion** vendor (same rate).

## Live site

https://judy2026797.github.io/Vendor-TDS-Calculation-
