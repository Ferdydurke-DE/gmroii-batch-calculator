# GMROII Batch Calculator

A browser-based tool for independent bookstores to analyze inventory performance across multiple titles using **Gross Margin Return on Inventory Investment (GMROII)** — based on Shatzkin's *The Mathematics of Bookselling*.

## Features

- **CSV Upload** — drag & drop or browse; auto-detects comma/semicolon separator and 5 or 6-column format
- **Portfolio Summary** — aggregate metrics: total inventory at cost, weighted GMROII, annual gross margin, average stock turn, underperforming titles count
- **Sortable Table** — 12 columns with color-coded rows (red = GMROII < 1, green = GMROII >= 2); click headers to sort
- **Expandable Detail Panels** — click any row to open a full dashboard per title: 8 metric cards, earning power decline chart, order quantity comparison table
- **Editable Parameters** — per-title order quantity slider and invoice payment days; global reorder frequency and lead time
- **Optimal Order Qty** — automatically calculated to cover demand during reorder cycle + lead time
- **Multilingual Lexicon** — parameter definitions in Romanian, English, German, and French
- **CSV Export** — download results with all calculated metrics

## CSV Format

### 6-column (with title):
```
ISBN,Title,Purchase Price,Sale Price,Units Sold,Current Stock
978-0-06-112008-4,To Kill a Mockingbird,8.40,14.00,12,4
```

### 5-column (without title):
```
ISBN,Purchase Price,Sale Price,Units Sold,Current Stock
978-0-06-112008-4,8.40,14.00,12,4
```

- **Units Sold** = copies sold in the last 4 weeks
- Separator: `,` or `;` (auto-detected)

## Files

| File | Description |
|------|-------------|
| `gmroii-batch-calculator.html` | Main application (single HTML file, no dependencies) |
| `gmroii-sample-150.csv` | Sample dataset with 150 titles for testing |
| `gmroii-calculator.html` | Single-title GMROII calculator (standalone) |

## Usage

1. Open `gmroii-batch-calculator.html` in any modern browser
2. Click **Load Sample Data** to test with built-in data, or upload a CSV file
3. Adjust **Reorder Frequency** and **Lead Time** as needed
4. Click any row to explore detailed metrics
5. Click **Export Results CSV** to download

## Key Metrics Explained

- **GMROII** = Margin per $ Invested × Stock Turn — dollars of gross margin per dollar invested in inventory per year
- **Stock Turn** = Annual sales at cost / Average inventory at cost
- **Recovery** = Days for sales revenue to cover the order cost
- **Earning Power Decline** = How GMROII drops the longer a copy sits unsold

## License

This project is licensed under the GNU General Public License v3.0 — see [LICENSE](LICENSE) for details.
