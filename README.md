<!-- PROJECT TITLE -->
<p align="center">
  <img src="https://img.shields.io/badge/Domain-FinTech-blue" alt="Domain"/>
  <img src="https://img.shields.io/badge/Focus-Risk%20Analytics-brightgreen" alt="Focus"/>
  <img src="https://img.shields.io/badge/Tools-Python%20%7C%20SQL%20%7C%20Excel%20%7C%20Tableau-orange" alt="Tools"/>
</p>

<h1 align="center">📊 Bank Loan Analysis & Risk Assessment</h1>
<p align="center"><i>Data-driven insights for safer lending — tailored for Banks, NBFCs, Risk Teams, and Loan Officers.</i></p>

<br/>

<!-- QUICK LINKS -->
<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-architecture--workflow">Architecture</a> •
  <a href="#-dashboards--screenshots">Dashboards</a> •
  <a href="#-quickstart">Quickstart</a> •
  <a href="#-dataset--schema">Dataset</a> •
  <a href="#-results--impact">Results</a>
</p>

---

## 🚀 Why this project?
Financial institutions need fast, reliable ways to **assess borrower risk**, **monitor loan performance**, and **reduce NPAs**.  
This project delivers an end-to-end analytics workflow — from **data cleaning (SQL/Python)** to **Excel/Tableau dashboards** — that puts **actionable insights** in the hands of decision-makers.

### Who benefits?
- **Loan Officers:** human-friendly Excel dashboards to assess borrower profiles quickly.  
- **Risk & Credit Teams:** risk segmentation, cohort analysis, and trend monitoring.  
- **Management:** portfolio-level KPIs and drilldowns to refine lending policies.

---

## ✨ Features
- 🔎 **Risk Driver Analysis:** income, credit history, DTI, and loan amount.
- 📈 **Excel Dashboards:** pivots + slicers for approval, default, demographics.
- 🧭 **Interactive Tableau:** regional/segment drilldowns for portfolio health.
- ⚙️ **ETL Workflow:** Excel → SQL/Python → curated tables → dashboards.
- ✅ **Reproducible:** notebooks + SQL scripts + documented pipeline.

---

## 🏗️ Architecture & Workflow
```mermaid
flowchart LR
    A[Raw Data\n(Excel: dataset.xlsx)] --> B[SQL Cleaning\n(SQLQuery1.sql)]
    A --> C[Python EDA & ETL\n(Bank Loan Analysis.ipynb)]
    B --> D[Curated Tables / Views]
    C --> D
    D --> E[Excel Dashboards\n(Pivots, Charts, Slicers)]
    D --> F[Tableau Workbook\n(Bank Loan Analysis.twbx)]
    E --> G[Loan Officers]
    F --> H[Risk & Management]
```

<details>
<summary><b>Pipeline Highlights</b></summary>

- **Data Cleaning:** handle nulls, outliers, inconsistent encodings (SQL/Python)  
- **Feature Prep:** credit_score_bins, income_bands, DTI, tenure_buckets  
- **KPIs:** Approval Ratio, Default Rate, PAR(30/60/90), Avg Ticket Size, Recovery %  
- **Delivery:** Excel (operational) + Tableau (strategic) dashboards
</details>

---

## 🖼️ Dashboards & Screenshots
> Replace the placeholders with actual images from your project (put them under `/assets`).

<table>
  <tr>
    <td align="center"><b>Excel: Loan Operations Dashboard</b></td>
    <td align="center"><b>Tableau: Portfolio Risk Overview</b></td>
  </tr>
  <tr>
    <td><img src="assets/excel-dashboard.png" alt="Excel Dashboard" /></td>
    <td><img src="assets/tableau-dashboard.png" alt="Tableau Dashboard" /></td>
  </tr>
</table>

---

## ⚡ Quickstart
```bash
# 1) Clone
git clone https://github.com/your-username/bank-loan-analysis.git
cd bank-loan-analysis

# 2) (Optional) Create environment
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate

# 3) Install Python deps
pip install -r requirements.txt

# 4) Open the notebook
jupyter notebook "Bank Loan Analysis.ipynb"
```

### Run SQL (MS SQL Server / MySQL)
- Open `SQLQuery1.sql` and execute the statements to create cleaned tables/views.  
- Point Tableau/Excel to the curated outputs for visualizations.

### Open Dashboards
- **Excel:** `/excel/Loan-Dashboard.xlsx` *(use your actual path or file name)*  
- **Tableau:** `Bank Loan Analysis.twbx`

---

## 🗂️ Repository Structure
```
bank-loan-analysis/
├── Bank Loan Analysis.ipynb
├── SQLQuery1.sql
├── Bank Loan Analysis.twbx
├── data/
│   ├── raw/
│   │   └── dataset.xlsx
│   └── processed/           # curated tables/exports (CSV/XLSX)
├── excel/
│   └── Loan-Dashboard.xlsx  # your Excel dashboard
├── assets/
│   ├── excel-dashboard.png
│   └── tableau-dashboard.png
├── requirements.txt
└── README.md
```

---

## 🧾 Dataset & Schema
| Field | Type | Description |
|------|------|-------------|
| `customer_id` | string | Unique borrower identifier |
| `age` | int | Applicant age |
| `income` | float | Annual income |
| `loan_amount` | float | Disbursed amount |
| `tenure_months` | int | Loan tenure |
| `credit_score` | int | Credit score (e.g., 300–850) |
| `employment_type` | string | Salaried / Self-employed |
| `region` | string | Branch/State/City |
| `approval_status` | string | Approved / Rejected |
| `default_flag` | int/bool | 1 = default, 0 = no default |
| `recovery_amount` | float | Amount recovered post-default |

> Adjust the schema to match your dataset exactly.

---

## 📊 Results & Impact
- Pinpointed **high-risk cohorts** (e.g., low credit score + high DTI).  
- Enabled **faster approvals** with transparent, auditable criteria in Excel.  
- Provided leadership with **portfolio-level risk heatmaps** in Tableau.  
- Foundation to **reduce NPAs** via targeted policy and collections strategies.

---

## 🛣️ Roadmap
- [ ] Add automated refresh & scheduled extracts  
- [ ] Add model-based PD/LGD scoring notebook  
- [ ] Publish Tableau Public demo

---


