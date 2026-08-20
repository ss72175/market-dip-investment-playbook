#  Market Dip Investment Playbook

### A Data-Driven Framework for Investing Through Market Corrections

This project is a Power BI-based multi-asset market analysis and investment decision-support dashboard designed to monitor market corrections, drawdowns and potential opportunities for systematic capital deployment.

The objective is simple:

> **Track the market → Measure the correction → Identify the investment zone → Follow a predefined playbook.**

Instead of trying to predict the exact market bottom, the dashboard uses historical price data and predefined correction levels to create a systematic framework for deploying capital during market declines.

---

##  Project Objective

The purpose of this project is to build a data-driven investment monitoring system that helps answer:

- How far is an asset currently below its All-Time High?
- What was the maximum historical correction?
- When did previous corrections occur?
- Has the asset recovered from a previous correction?
- Has a selected correction level been reached?
- What investment code should be activated based on the current drawdown?
- Which assets are currently experiencing meaningful corrections?

The dashboard is designed as a **decision-support tool**, not a market prediction system.

---

#  Assets Tracked

The current version tracks:

| Asset | Historical Data |
|---|---|
| HNGSNGBEES | 2010 – 2026 |
| MON100 | 2011 – 2026 |
| GOLD | 2018 – 2026 |
| SILVER | 2018 – 2026 |
| NIFTY 50 | 2018 – 2026 |
| NIFTY MIDCAP 150 | 2020 – 2026 |
| NIFTY NEXT 50 | 2020 – 2026 |
| NIFTY SMALLCAP 250 | 2020 – 2026 |

The different start dates reflect the availability of the historical datasets used in the project.

---

#  Investment Framework

The investment framework uses market drawdown from the All-Time High to classify the current market condition.

### Example correction framework

| Market Drawdown | Investment Code |
|---|---|
| < 10% | Normal |
| 10% – 20% | Code Alpha |
| 20% – 30% | Code Bravo |
| 30% – 40% | Code Charlie |
| 40% – 50% | Code Delta |
| > 50% | BOOM |

The actual capital allocation is defined separately in my investment playbook.

The purpose of these levels is to create predefined rules so that investment decisions are less influenced by emotions during periods of market volatility.

---

#  Dashboard Features

### 1. Asset Selector

The dashboard allows the user to switch between:

- Gold
- Silver
- MON100
- HNGSNGBEES
- Nifty 50
- Nifty Midcap 150
- Nifty Next 50
- Nifty Smallcap 250

---

### 2. All-Time High Analysis

The dashboard calculates:

- All-Time High
- Date of All-Time High
- Current value
- Current drawdown from ATH

---

### 3. Correction Analysis

The dashboard identifies predefined correction levels such as:

- 5%
- 10%
- 15%
- 20%
- 25%
- 30%
- 35%
- 40%
- 45%
- 50%
- 55%
- 60%

This allows the user to investigate when an asset historically reached a particular drawdown level.

---

### 4. Maximum Correction

The dashboard identifies:

- Maximum historical correction after ATH
- Date of maximum correction after ATH
- Lowest price following the ATH

---

### 5. Latest Correction

A selected correction percentage can be used to identify the latest occurrence of that correction level.

For example:

> Latest 15% Correction

The dashboard returns the corresponding price/date or indicates:

> Target Not Reached Yet

---

### 6. Investment Signal

The current drawdown is translated into the predefined investment framework:

**Normal → Alpha → Bravo → Charlie → Delta → BOOM**

This creates a simple visual decision-support mechanism.

---

# 🔄 Data Automation

One of the main objectives of this project was to avoid manually rebuilding the dashboard every time new market data becomes available.

The workflow is:

```text
Market Data
     ↓
Excel Files
     ↓
Automated Folder
     ↓
Power Query
     ↓
Data Cleaning & Transformation
     ↓
Combine Data
     ↓
Power BI Data Model
     ↓
DAX Calculations
     ↓
Interactive Dashboard
