# Bluestock Week 2 — FinTech Domain & Software Development Fundamentals

**Internship:** Bluestock FinTech Internship  
**Author:** Lavanish  
**Assignment:** Week 2 Deliverables Package  

---

## Assignment Objective

The objective of this assignment is to bridge financial domain knowledge with software engineering fundamentals. This repository demonstrates:
- Core understanding of Indian stock market operations, exchanges, valuation metrics, and financial statements.
- Rigorous financial statement analysis using corporate disclosures and standard accounting ratios.
- Automated financial data extraction from public REST APIs, JSON parsing, tabular transformation, and schema validation.
- End-to-end software architecture design for scalable, secure FinTech applications.
- Structured product and industry research on a leading digital payments platform (PhonePe).
- Professional software development best practices, documentation, and version control.

---

## Assignment Deliverables

| Deliverable | Topic | Path | Format |
|---|---|---|---|
| **1. Stock Market Summary** | Indian stock market mechanisms, exchanges, indices, IPOs, valuation multiples, and core ratios | `01_stock_market_summary/Stock_Market_Summary.pdf` | PDF Document |
| **2. Financial Statement Analysis** | Tata Consultancy Services (TCS) consolidated performance (FY24–FY26), margin trends, cash flows, and liquidity | `02_financial_analysis/TCS_Financial_Statement_Analysis.xlsx` | Excel Workbook (`.xlsx`) |
| **3. API Data Extraction** | CoinGecko REST API ingestion for BTC & ETH, JSON flattening, validation, and CSV export | `03_api_extraction/CoinGecko_API_Extraction.ipynb` | Jupyter Notebook & CSV |
| **4. GitHub Repository** | Complete, clean, well-documented repository structure conforming to submission requirements | Root directory & `README.md` | Git Repository |
| **5. Software Architecture** | High-level architectural data flow: Client → API → Database → Processing → Analytics | `04_architecture/Software_Architecture_Diagram.png` | Architecture Diagram (PNG) |
| **6. FinTech Research Report** | Comprehensive analysis of PhonePe: platform overview, user journey, business model, architecture, security, and SWOT | `05_fintech_research/PhonePe_FinTech_Research_Report.pdf` | PDF Research Report |

---

## Repository Folder Structure

```text
bluestock-week2-fintech-assignment/
│
├── README.md
│
├── 01_stock_market_summary/
│   └── Stock_Market_Summary.pdf
│
├── 02_financial_analysis/
│   └── TCS_Financial_Statement_Analysis.xlsx
│
├── 03_api_extraction/
│   ├── CoinGecko_API_Extraction.ipynb
│   ├── coingecko_prices.csv
│   ├── coingecko_prices_example.csv
│   └── api_extraction_notes.txt
│
├── 04_architecture/
│   └── Software_Architecture_Diagram.png
│
└── 05_fintech_research/
    └── PhonePe_FinTech_Research_Report.pdf
```

---

## Detailed Deliverable Breakdown

### 1. Stock Market Summary
- **File:** `01_stock_market_summary/Stock_Market_Summary.pdf`
- **Coverage:**
  - Role of stock markets and distinction between primary and secondary markets.
  - Overview of National Stock Exchange (NSE) and BSE Limited; benchmark indices (Nifty 50, Sensex).
  - Public offerings (Mainboard IPO and SME IPO framework).
  - Valuation and equity metrics: Market Capitalisation, Earnings Per Share (EPS), Price-to-Earnings (P/E), Price-to-Book (P/B), Dividend Yield, Bonus Issues, Stock Splits, and Trading Volume.
  - Financial statements triage (Balance Sheet, Profit & Loss Statement, Cash Flow Statement).
  - Four fundamental financial ratios: Net Profit Margin, Current Ratio, Debt-to-Equity Ratio, and Return on Equity (ROE).

### 2. Financial Statement Analysis (TCS Consolidated)
- **File:** `02_financial_analysis/TCS_Financial_Statement_Analysis.xlsx`
- **Sheets:**
  - `Financial Analysis`: Reported revenue from operations, net profit, operating cash flow, assets, liabilities, and equity for FY2024–FY2026. Includes dynamic Excel formulas for revenue growth (`=C5/B5-1`), net profit margin (`=B6/B5`), operating cash flow-to-profit (`=B7/B6`), current ratio (`=C9/C10`), asset growth, and equity growth.
  - `Sources & Method`: Explicit citation of TCS audited consolidated financial statements, method documentation, and analytical limitations.
- **Key Findings:**
  - Revenue expanded from ₹2,55,324 Cr (FY25) to ₹2,67,021 Cr (FY26) (~4.58% growth).
  - Net operating cash flow increased to ₹52,094 Cr, demonstrating cash conversion strength.
  - Current ratio maintained healthy liquidity coverage (2.32 in FY25, 2.23 in FY26).

### 3. Public API Data Extraction
- **Directory:** `03_api_extraction/`
- **Files:**
  - `CoinGecko_API_Extraction.ipynb`: Automated Python extraction pipeline.
  - `coingecko_prices.csv`: Clean, live extracted dataset containing Bitcoin and Ethereum market quotes in USD and INR with UTC timestamp.
  - `coingecko_prices_example.csv`: Schema template illustrating expected data structure.
  - `api_extraction_notes.txt`: Technical execution notes, rate limits, and verification guidance.
- **Pipeline Implementation:**
  - HTTP `GET` request using `requests` with custom timeouts and error handling (`raise_for_status()`).
  - Response payload parsing and validation (`dict` structure with coin identifiers).
  - Data flattening into a normalized `pandas.DataFrame`.
  - Timestamp attribution in ISO 8601 UTC format.
  - Assertion-based schema and null-value testing.

### 4. Software Architecture Diagram
- **File:** `04_architecture/Software_Architecture_Diagram.png`
- **Architectural Flow:**
  - `User / Client`: Mobile application and web portal interfaces.
  - `Application / API Layer`: API Gateway, token-based authentication (OAuth2/JWT), rate limiting, and request validation.
  - `Database Layer`: Relational/document storage for accounts, ledger entries, transactions, and audit logs.
  - `Data Processing Layer`: Asynchronous worker queues, message streams, ETL pipelines, and data validation engines.
  - `Analytics Dashboard`: Real-time monitoring, transaction analytics, reporting KPIs, and dispute reconciliation.
  - `Auth & Security`: Zero-trust network principles, end-to-end TLS encryption, field-level encryption for sensitive PII/tokens.

### 5. FinTech Research Report (PhonePe)
- **File:** `05_fintech_research/PhonePe_FinTech_Research_Report.pdf`
- **Coverage:**
  - Platform overview and UPI-first product ecosystem.
  - Problem statement: friction in everyday merchant and peer transactions, cash dependency reduction.
  - 6-step user journey from registration and bank account linkage to PIN authorization and settlement notification.
  - Multi-sided business model and value creation mechanisms.
  - Technical architecture and asynchronous payment state reconciliation.
  - Security, fraud prevention, RBI/NPCI regulatory conformance, and data privacy safeguards.
  - Comprehensive SWOT matrix and cited primary references.

---

## Tools and Technologies Used

- **Programming & Scripting:** Python 3.12+ / 3.15
- **Data Manipulation & Analysis:** `pandas`, `openpyxl`
- **Networking & API Integration:** `requests`
- **Interactive Development:** Jupyter Notebook, `ipython`, `nbformat`
- **Visualization & Design:** Matplotlib
- **Document Processing:** PyPDF
- **Version Control & Repository Management:** Git & GitHub

---

## Instructions for Running the API Notebook

### Prerequisites
Ensure Python 3.10+ is installed on your system.

### 1. Set Up Environment
Create and activate a virtual environment (optional but recommended):
```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 2. Install Required Dependencies
```bash
pip install requests pandas jupyter
```

### 3. Launch and Execute
Navigate to the API extraction folder and launch Jupyter:
```bash
cd 03_api_extraction
jupyter notebook CoinGecko_API_Extraction.ipynb
```
Select **Kernel → Restart & Run All** to make a live call to the CoinGecko public API, execute validations, and generate a fresh `coingecko_prices.csv`.

---

## Data Limitations & Academic Integrity

- **Financial Statements:** All figures in `02_TCS_Financial_Statement_Analysis.xlsx` are sourced directly from Tata Consultancy Services (TCS) audited consolidated financial disclosures. Calculated ratios represent mathematical derivatives for academic demonstration and do not constitute financial advice or investment recommendations.
- **API Market Quotes:** Cryptocurrency prices are real-time, highly volatile, point-in-time observations. The included `coingecko_prices_example.csv` is provided solely as a schema reference; live prices are generated dynamically upon notebook execution.
- **Academic Standard:** No metrics, financials, market share figures, or proprietary system designs were fabricated. All citations refer to official regulatory (SEBI, RBI, NPCI) and corporate portals.

---

## How to Publish & Submit to GitHub

Follow these steps to push this repository to your personal GitHub account:

### Step 1: Create a New GitHub Repository
1. Log in to [GitHub](https://github.com).
2. Click **New Repository**.
3. Name the repository: `bluestock-week2-fintech-assignment`.
4. Choose **Public** (or according to your internship requirements).
5. Do **not** initialize with a README, `.gitignore`, or license (these are already configured).

### Step 2: Link and Push Local Repository
In your terminal, navigate to the project directory and run:
```bash
# Verify status and stage all files
git status
git add .

# Create initial commit
git commit -m "feat: complete Bluestock Week 2 FinTech assignment deliverables"

# Set default branch to main
git branch -M main

# Link to your remote GitHub repository
git remote add origin https://github.com/Lavanish007/bluestock-week2-fintech-assignment.git

# Push to GitHub
git push -u origin main
```

### Step 3: Submit Repository URL
Copy the resulting repository URL (`https://github.com/Lavanish007/bluestock-week2-fintech-assignment`) and paste it into the official Bluestock internship submission portal.

