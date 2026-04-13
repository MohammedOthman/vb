# Prompt: Consolidated Financial Statements Generator

> Copy the full prompt below into shortcut.ai. Attach your PDF financial documents when running it.

---

## PROMPT

```
You are a certified financial analyst and IFRS specialist. Your task is to read the attached PDF financial documents for a company and produce a complete, verified set of consolidated financial statements in a single structured document.

## INSTRUCTIONS

### Step 1 — Identify & Classify Documents

Read every attached PDF and classify each one:
- **Audited Financial Statements** → extract exact SAR figures. Note the year(s) covered (current + comparative).
- **Valuation Reports** → extract financial data tables (usually in thousands SAR). Note which years are audited vs internal/unaudited.
- **Internal/Management Accounts** → flag as unaudited. Note the period covered.

For each document, record:
- Company name, legal form, registration number
- Financial year(s) covered
- Auditor name and opinion (if audited)
- Currency and unit (SAR, thousands SAR, etc.)
- Accounting standard (IFRS for SMEs, Full IFRS, SOCPA, etc.)

### Step 2 — Extract All Financial Data

From each document, extract the following statements in full, preserving every line item and every year column:

**A. Statement of Financial Position (Balance Sheet / قائمة المركز المالي)**
- All current assets (cash, receivables, inventory, prepaid, other)
- All non-current assets (PPE, intangible, investments, right-of-use)
- All current liabilities (loans, payables, related parties, accrued, zakat, current portion of long-term)
- All non-current liabilities (employee benefits, long-term loans, lease liabilities)
- All equity components (share capital, additional capital, statutory reserve, retained earnings, OCI reserves)

**B. Statement of Comprehensive Income (Income Statement / قائمة الدخل الشامل)**
- Revenue
- Cost of revenue / cost of sales
- Gross profit
- General & administrative expenses
- Selling & distribution expenses (if any)
- Finance costs
- Other income / (expenses)
- Profit before zakat / tax
- Zakat / income tax
- Net income
- Other comprehensive income items
- Total comprehensive income

**C. Statement of Changes in Equity (قائمة التغيرات في حقوق الملكية)**
- Opening balance for each equity component
- Each movement: net income, dividends, capital changes, reserve transfers, OCI, restatements
- Closing balance for each equity component

**D. Statement of Cash Flows (قائمة التدفقات النقدية)**
- Operating activities: profit before zakat, non-cash adjustments, working capital changes, zakat/tax paid
- Investing activities: PPE/intangible additions, disposals, investments
- Financing activities: loans, capital, dividends, lease payments
- Net change, opening cash, closing cash

### Step 3 — Cross-Reference & Reconcile

Before producing output, verify these mandatory checks:

**Balance Sheet Checks (for every year):**
- Total Assets = Total Liabilities + Total Equity
- Current Assets = sum of all current asset line items
- Non-Current Assets = sum of all non-current asset line items
- Current Liabilities = sum of all current liability line items
- Total Equity = Capital + Additional Capital + Reserves + Retained Earnings

**Income Statement Checks (for every year):**
- Revenue − Cost of Revenue = Gross Profit
- Gross Profit − Operating Expenses = Income from Main Activities
- Income from Main Activities + Other Income = Profit Before Zakat
- Profit Before Zakat − Zakat = Net Income

**Equity Reconciliation (for every year):**
- Opening Retained Earnings + Net Income − Dividends ± Other = Closing Retained Earnings
- Opening Total Equity + Total Comprehensive Income + Capital Changes − Dividends = Closing Total Equity

**Cash Flow Checks (for every year):**
- Operating + Investing + Financing = Net Change in Cash
- Opening Cash + Net Change = Closing Cash
- Closing Cash must equal Balance Sheet cash for same year

**Cross-Statement Checks:**
- Net Income in Income Statement = Net Income in Equity Statement = Starting figure in Cash Flow
- Closing equity in Equity Statement = Total Equity in Balance Sheet
- Closing cash in Cash Flow = Cash in Balance Sheet

If ANY comparative year appears in multiple documents, verify the figures match. Flag discrepancies.

### Step 4 — Produce the Consolidated Output

Generate one unified document with this exact structure:

---

# [Company Name] — Consolidated Financial Statements ([First Year]–[Last Year])

**Company:** [Full legal name]
**Type:** [Legal form — LLC, JSC, etc.]
**Registration:** [Commercial registration number, city, date]
**Location:** [City, Country]
**Activity:** [Business description]
**Currency:** SAR (Saudi Riyal)
**Accounting Standard:** [IFRS for SMEs / Full IFRS / etc.]

### Data Sources
| Year | Source Document | Status |
|------|---------------|--------|
| [Year] | [Document name] | Audited / Internal |

---

## 1. Statement of Financial Position
*As at 31 December — SAR*

[Table with columns: Line Item | Note | Year1 | Year2 | Year3 | Year4]

Present in this order:
- Current Assets (with subtotal)
- Non-Current Assets (with subtotal)
- **TOTAL ASSETS**
- Current Liabilities (with subtotal)
- Non-Current Liabilities (with subtotal)
- **TOTAL LIABILITIES**
- Equity components
- **TOTAL EQUITY**
- **TOTAL LIABILITIES & EQUITY**

### Balance Sheet Verification
| Check | Year1 | Year2 | Year3 | Year4 |
| Total Assets = Total L&E | ✓/✗ | ✓/✗ | ✓/✗ | ✓/✗ |

---

## 2. Statement of Comprehensive Income
*For the year ended 31 December — SAR*

[Table with columns: Line Item | Note | Year1 | Year2 | Year3 | Year4]

### Income Statement Verification
| Check | Year1 | Year2 | Year3 | Year4 |
| Revenue − COGS = Gross | ✓/✗ | ... |
| Gross − Expenses = Main | ✓/✗ | ... |
| Main + Other = PBZ | ✓/✗ | ... |
| PBZ − Zakat = Net | ✓/✗ | ... |

### Key Margins
| Metric | Year1 | Year2 | Year3 | Year4 |
| Gross margin | x% | ... |
| Net margin | x% | ... |

---

## 3. Statement of Changes in Equity
*SAR*

[One sub-table per year showing: Opening → each movement → Closing, with columns for each equity component + Total]

### Equity Verification
| Check | Year1 | Year2 | Year3 | Year4 |
| Opening + Changes = Closing | ✓/✗ | ... |

---

## 4. Statement of Cash Flows
*For the year ended 31 December — SAR*

[Table with columns: Line Item | Year1 | Year2 | Year3 | Year4]

### Cash Flow Verification
| Check | Year1 | Year2 | Year3 | Year4 |
| Ops + Inv + Fin = Net Change | ✓/✗ | ... |
| Opening + Net = Closing | ✓/✗ | ... |

---

## 5. Key Financial Ratios

| Ratio | Year1 | Year2 | Year3 | Year4 |
|-------|-------|-------|-------|-------|
| **Profitability** | | | | |
| Gross margin | | | | |
| Operating margin | | | | |
| Net margin | | | | |
| Return on equity (ROE) | | | | |
| Return on assets (ROA) | | | | |
| **Liquidity** | | | | |
| Current ratio | | | | |
| Quick ratio | | | | |
| **Leverage** | | | | |
| Debt-to-equity | | | | |
| Equity / Total assets | | | | |
| **Activity** | | | | |
| Receivables days | | | | |
| Inventory days | | | | |
| Payables days | | | | |
| Cash conversion cycle | | | | |
| **Growth** | | | | |
| Revenue growth YoY | | | | |
| Net income growth YoY | | | | |
| Total assets growth YoY | | | | |

---

## 6. Notes & Observations

- [Any valuation summary if a valuation report is attached]
- [Any significant accounting policy changes between years]
- [Any red flags: negative cash, declining margins, going concern, etc.]
- [Cross-document discrepancies found and how resolved]

---

### FORMATTING RULES

1. **Numbers:** Use SAR with comma separators. Negative numbers in parentheses: (1,234,567)
2. **Unaudited years:** Mark with ¹ superscript and footnote explaining source
3. **Rounding:** If source data is in thousands, multiply by 1,000 and note "approximate"
4. **Arabic labels:** Include Arabic line item names alongside English where available
5. **Verification:** Every section MUST have a verification table. Every check must show ✓ or explain the discrepancy
6. **No guessing:** If a number cannot be extracted or derived, write "N/A" — never fabricate figures
7. **Discrepancies:** If the same year appears in multiple documents with different figures, show both and explain which was used and why

### CRITICAL RULES

- NEVER swap line items (e.g., PPE vs Intangible, Receivables vs Prepaid). Cross-reference across documents to confirm each line item's identity.
- ALWAYS verify that comparative columns in newer statements match the primary columns in older statements.
- Present Balance Sheet items in consistent order across all years even if source documents use different ordering.
- For equity changes, derive from audited statements — do not rely solely on valuation report summaries.
- Cash flow closing balance MUST equal the balance sheet cash figure for the same year.
```

---

## HOW TO USE

1. Go to **shortcut.ai**
2. Paste the full prompt above
3. Attach your PDF files (audited financials, valuation reports, management accounts)
4. Run — the AI will produce a complete verified consolidated financial statements document

## SUPPORTED DOCUMENT TYPES

- Audited annual financial statements (Arabic or English)
- Valuation reports (IFRS 13, IVS-based)
- Internal / management financial reports
- Quarterly financials
- Budget vs actual reports

## TIPS FOR BEST RESULTS

- **Attach all years** — if you have 2022, 2023, and 2024 audited statements, attach all three even though each contains comparative data. This enables cross-verification.
- **Include the valuation report** if available — it often contains a clean multi-year summary that helps resolve extraction errors from Arabic PDFs.
- **Name your files clearly** — e.g., "Company_2024_Audited.pdf" so the AI can identify each document.
- **Specify the company name** in your message if the PDFs have unclear or generic titles.
