# ClientFlow OS English

A freelance client management system built in Excel. Track projects and billable hours, manage invoices, log payments and expenses, and export professional PDF invoices in a few clicks.

**Version:** 1.0 (dual-format: `.xlsm` and `.xlsx`)

---

## Features

- Time and task logging for ongoing client projects
- Invoice tracking with status updates
- Payment and expense tracking
- Auto-populated invoice template: pick an Invoice ID and all details, totals, and line items fill in instantly
- One-click **Export to PDF** (macro version) with a built-in fail-safe fallback
- Customizable business name, address, contact info, and bank details

## Which File Should I Use?

| File | Type | Best For | Key Features |
|------|------|----------|--------------|
| `ClientFlow_OS_English.xlsm` | Macro-enabled | Windows / Desktop Excel | 1-click "Export to PDF" button with auto fail-safe print fallback |
| `ClientFlow_OS_English.xlsx` | Standard spreadsheet | macOS, Excel Online, Google Sheets | 100% macro-free, clean formulas, no security prompts or ActiveX issues |

**Rule of thumb:** on Windows Excel and want single-click PDF export? Use `.xlsm`. On macOS, Excel for the web, or prefer macro-free files? Use `.xlsx`.

## Quick Start

### 1. Unblock and enable macros (`.xlsm` on Windows only)

1. Right-click `ClientFlow_OS_English.xlsm` and select **Properties**.
2. On the **General** tab, check **Unblock** (if present), then click **Apply > OK**.
3. Open the file in Microsoft Excel and click **Enable Content** on the security bar.

### 2. Manage client and invoice data

| Sheet | Purpose |
|-------|---------|
| `04_Tasks_TimeLog` | Log ongoing projects and hours |
| `05_Invoices` | Record invoice summaries and status updates |
| `07_Payments` | Track client payments |
| `08_Expenses` | Track business expenses |

### 3. Generate and export PDF invoices

1. Go to the `06_Invoice_Template` sheet.
2. Select an **Invoice_ID** from the dropdown in cell `C3` / `C4`. Details, billing totals, and line items populate automatically.
3. Export:
   - **`.xlsm`:** click the **Export to PDF** button.
     - *Direct export* generates the PDF immediately.
     - *Fail-safe fallback:* if Windows security blocks ActiveX components, a popup guides you to standard PDF printing (select **Microsoft Print to PDF**), with no crashes or debug errors.
   - **`.xlsx` / macOS:** go to **File > Save As > PDF**, or **File > Print > Save as PDF**.

## Customization

Edit your business name, address, contact info, and bank details directly on the `06_Invoice_Template` sheet, in **rows 6-10**.

## FAQ

**Should I use `.xlsm` or `.xlsx`?**
Use `.xlsm` on Windows Excel for one-click PDF export. Use `.xlsx` on macOS, Excel for the web, or if you prefer macro-free files.

**Can I customize the invoice logo and business details?**
Yes. See the [Customization](#customization) section above.

**Windows says direct PDF export is restricted. What now?**
Your system blocks ActiveX PDF libraries. Follow the on-screen prompt, choose **Microsoft Print to PDF**, and save.

## Repository Contents

```
.
├── ClientFlow_OS_English.xlsm          # Macro-enabled version (Windows)
├── ClientFlow_OS_English.xlsx          # Macro-free version (Mac / Web / Sheets)
├── ClientFlow_OS_Quick_Start_Guide.pdf # Official quick start & user guide
└── README.md
```

## License

ClientFlow OS English © 2026. All rights reserved.
Created for freelancers, agency owners, and independent professionals.
