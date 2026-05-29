# M3 AP Invoice Import — Field Reference

## Required Fields (marked *)
All must be populated for M3 to accept the row.

| Field | Type | Max Length | Notes |
|---|---|---|---|
| CompanyID* | Numeric | 3 | From Hollander vendor master |
| PropertyID* | Numeric | 3 | Always = CompanyID for Hollander |
| VendorNumber* | Alpha Numeric | 10 | From Hollander vendor master |
| VendorName* | Alpha Numeric | 50 | Match M3 vendor master name exactly |
| InvoiceNumber* | Alpha Numeric | 25 | As printed; use account# for utilities |
| InvoiceDate* | Date | — | mm/dd/yyyy |
| PostDate* | Date | — | mm/dd/yyyy — equals InvoiceDate for Hollander |
| DueDate* | Date | — | mm/dd/yyyy |
| Amount* | Money | — | Total invoice amount due |
| AccountNumber* | Numeric | — | GL account code |
| LineItemAmount* | Money | — | Usually same as Amount for single-GL invoices |

## Optional Fields
| Field | Type | Max Length | Notes |
|---|---|---|---|
| Phone | Alpha Numeric | 10 | Format: ##########  (no dashes) |
| Fax | Alpha Numeric | 25 | |
| Email | Alpha Numeric | 100 | |
| AddressLine1 | Alpha Numeric | 75 | Vendor remit-to address |
| AddressLine2 | Alpha Numeric | 75 | |
| City | Alpha Numeric | 75 | |
| State | — | — | 2-digit postal abbreviation |
| Zip | Alpha Numeric | 10 | |
| Title | Alpha Numeric | 5 | Dr., Miss, Mr., Mrs., Ms. |
| FirstName | Alpha Numeric | 50 | Vendor contact |
| LastName | Alpha Numeric | 50 | |
| Description | Alpha Numeric | 100 | Free text description |
| LineItemDescription | Alpha Numeric | 100 | Line item detail |
| TaxGroup | — | — | |
| TaxCode | — | — | |
| PO # | Alpha Numeric | 25 | Purchase order number if applicable |

## Date Format
Always use mm/dd/yyyy (e.g. 05/21/2026).

## Hollander-Specific Rules
- PostDate = InvoiceDate (confirmed rule as of 2026-05-28)
- PropertyID = CompanyID (confirmed from M3 company tree)
- For single-GL invoices: LineItemAmount = Amount
- Phone format: digits only, no dashes or parentheses (e.g. 2066251412)
