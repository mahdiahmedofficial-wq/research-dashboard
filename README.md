# Business Research Dashboard

## Folder Structure

```
research-dashboard/
├── index.html                          ← The dashboard (don't edit)
└── businesses/
    ├── fire-pump-flow-testing/
    │   ├── meta.json                   ← Business info + phase status
    │   ├── 01-research.pdf
    │   └── 02-sales-team.pdf
    ├── aerial-lift-inspection/
    │   ├── meta.json
    │   └── 01-research.pdf
    └── your-new-business/              ← Copy this pattern for new ones
        └── meta.json
```

## Adding a New Business

1. Create a new folder under `businesses/` (use hyphens, no spaces)
2. Create a `meta.json` file in that folder (copy from an existing one)
3. Update `meta.json` with the business details
4. Add the folder name to the `BUSINESSES` array in `index.html` (line ~130)
5. Upload your PDFs to the folder

## meta.json Template

```json
{
  "name": "Your Business Name",
  "date": "2026-03-14",
  "verdict": "pursue",
  "market": "Twin Cities, MN",
  "notes": "Key insight about this opportunity",
  "phases": {
    "research": "01-research.pdf",
    "sales-team": null,
    "hormozi": null,
    "customer-acquisition": null,
    "challenger-sale": null
  }
}
```

- Set `verdict` to `"pursue"` or `"nogo"`
- Set a phase to `null` if not yet run
- Set a phase to the filename (e.g. `"02-sales-team.pdf"`) when complete

## Adding a New PDF

1. Download the PDF from Claude
2. Rename it to match the pattern: `01-research.pdf`, `02-sales-team.pdf`, etc.
3. Upload it to the correct business folder on GitHub
4. Update `meta.json` to point to the file
5. Dashboard updates automatically within 60 seconds
