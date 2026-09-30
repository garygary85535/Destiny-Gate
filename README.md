# Destiny Gate

`Destiny轉運站` is a standalone static Postype index built from the `付費明細` sheet.

## Files

- `index.html`: searchable portal UI
- `destiny-data.js`: generated data

## Refresh Data

1. Export the latest workbook to `/private/tmp/destiny-book.xlsx`.
2. Run `sync_destiny_gate.py` from the parent `書目管理` folder.

## Publishing

This folder is intended to become an independent GitHub Pages project, separate from `Annyeongz`, so visitors cannot trim the URL back into the private translation site.

## Report API

Reports are collected in the `書目` spreadsheet tab `Destiny Gate 回報`.

1. Create a Google Apps Script project and paste `/Users/ellenrock/Documents/書目管理/destiny_gate_report_api.gs`.
2. Run `setupDestinyGateReportSheet` once if the report tab needs to be rebuilt.
3. Deploy as a Web App:
   - Execute as: Me
   - Who has access: Anyone
4. Copy the Web App URL into `REPORT_ENDPOINT` in `index.html`.

Until `REPORT_ENDPOINT` is filled, reports are saved only in the visitor browser.

Do not place the Apps Script file inside this public site folder or publish it to GitHub Pages.
