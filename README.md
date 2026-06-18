# TaxBuddy — Indian Income Tax Filing Assistant

**Smart, document-driven tax filing assistant for FY 2025-26 (AY 2026-27)**

TaxBuddy parses your Form 16, AIS, and Form 26AS, then guides you through ITR-1 / ITR-2 filing with auto-computed exemptions, regime comparison, and portal-ready values.

---

## What It Does

- **Parses** Form 16, AIS (Annual Information Statement), Form 26AS
- **Detects** multiple employers, cross-validates TDS across documents
- **Audits** like the IT Department — flags discrepancies before you file
- **Computes** HRA, LTA, 80C, 80CCD, 80D, 80E, 80G, and 15+ deductions automatically
- **Compares** Old vs New Regime — recommends the one that saves more tax
- **Shows** exact values to copy-paste into the IT portal
- **Warns** about headroom in each section so you don't miss deductions

---

## Installation (5 minutes)

### Prerequisites
- **Python 3.9 or higher** — check with `python3 --version`

### Step 1: Download & Extract
Unzip `TaxBuddy.zip` to any folder on your laptop.

### Step 2: Open Terminal
- **Mac:** Open `Terminal` app
- **Windows:** Open `Command Prompt` or `PowerShell`

### Step 3: Navigate to the folder
```bash
cd path/to/TaxBuddy
```

### Step 4: Install

**Option A — Use the install script (easiest):**
```bash
bash install.sh
```

**Option B — Install manually:**
```bash
python3 -m pip install .
```
This installs TaxBuddy and all dependencies (Streamlit, pdfplumber, openpyxl).

### Step 5: Launch the Web App
```bash
python3 -m taxbuddy
```
This opens TaxBuddy in your default browser at `http://localhost:8501`.

**That's it!** Upload your documents and follow the guided steps.

---

## Alternative: Run Without Installing

If `python3 -m pip install .` gives permission issues:

```bash
python3 -m pip install -r requirements.txt
python3 -m streamlit run taxbuddy/app.py
```

---

## Documents You'll Need

| Document | Where to Get It |
|----------|----------------|
| **Form 16** | From your employer's HR/Payroll. One per employer if you switched jobs. |
| **AIS** | IT Portal → Login → Services → AIS → FY 2025-26 → Download PDF |
| **Form 26AS** | IT Portal → Login → e-File → View Form 26AS → TRACES → AY 2026-27 → Export PDF |

---

## Features at a Glance

| Step | What Happens |
|------|-------------|
| 1. Upload Documents | Auto-parses Form 16, AIS, 26AS instantly |
| 2. Parsed Summary | Shows consolidated salary, TDS, deductions from all employers |
| 3. AIS Audit | Cross-checks your data like the IT Department would |
| 4. Smart Tax Optimizer | HRA, LTA, 80C, 80CCD, 80D, 80E, 80G — all auto-computed with headroom alerts |
| 5. Tax Computation | Old vs New Regime comparison with exact savings |
| 6. ITR Recommendation | Which form + complete deduction plan + optimization tips |
| 7. Filing Guide | Page-by-page portal walkthrough with copy-paste values |

---

## Troubleshooting

**"command not found: pip" or "zsh: command not found: pip"**
→ Do **not** use bare `pip`. Use `python3 -m pip install .` instead — this always works.
→ If that also fails: `python3 -m ensurepip --upgrade`

**"command not found: taxbuddy"**
→ Use `python3 -m taxbuddy` instead, or `python3 -m streamlit run taxbuddy/app.py`

**"No module named streamlit"**
→ Run `python3 -m pip install streamlit pdfplumber openpyxl`

**Port 8501 already in use**
→ Run `python3 -m streamlit run taxbuddy/app.py --server.port=8502`

**Python version too old**
→ Install Python 3.9+ from [python.org](https://www.python.org/downloads/)

**"Permission denied" during install**
→ Add `--user`: `python3 -m pip install . --user`

---

## Disclaimer

TaxBuddy is a computation and guidance tool. Always verify final figures on the official Income Tax portal (https://eportal.incometax.gov.in). All references cite the Income Tax Act, 1961. This is not legal or financial advice.

---

Built with ❤️ for Indian taxpayers | FY 2025-26 | MIT License
