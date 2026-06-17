# 📊 Business Insights 360 — AtliQ Hardware Power BI Dashboard

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)](#)
[![DAX](https://img.shields.io/badge/DAX-Data%20Analysis%20Expressions-2C5BB4?style=flat)](#)
[![Power Query](https://img.shields.io/badge/Power%20Query-ETL-1B6F5C?style=flat)](#)
[![Status](https://img.shields.io/badge/Status-Completed-success?style=flat)](#)

An end-to-end Power BI dashboard built for **AtliQ Hardware**, consolidating Finance, Sales, Marketing, Supply Chain, and Executive reporting into a single, interactive analytics suite.

---

## Table of Contents
- [Overview](#overview)
- [Business Problem](#business-problem)
- [Objectives & Key Business Questions](#objectives--key-business-questions)
- [Dashboard Walkthrough](#dashboard-walkthrough)
  - [Home Page](#-home-page)
  - [Executive View](#-executive-view)
  - [Finance View](#-finance-view)
  - [Sales View](#-sales-view)
  - [Marketing View](#-marketing-view)
  - [Supply Chain View](#-supply-chain-view)
- [Key Insights](#key-insights)
- [Tools & Skills Demonstrated](#tools--skills-demonstrated)
- [Metrics Glossary](#metrics-glossary)
- [Repository Structure](#repository-structure)
- [Future Enhancements](#future-enhancements)
- [Disclaimer](#disclaimer)
- [Author](#author)

---

## Overview

AtliQ Hardware is a (fictional) global computer hardware manufacturer that sells PCs, peripherals, and accessories across **APAC, EU, LATAM, and NA** through **Retail, Direct, and Distributor** channels. This project builds a unified Power BI reporting layer on top of AtliQ's sales, forecast, and financial data so that five different stakeholder groups — Finance, Sales, Marketing, Supply Chain, and Executive leadership — can each get a tailored view of the same underlying numbers, with full drill-down by region, market, customer, segment, category, and product.

The result is a **7-page interactive report** with consistent slicers (region/market, customer, segment/category/product), time intelligence (2019–2022 Est, by quarter, YTD/YTG), and benchmarking (vs. Last Year and vs. Target) applied uniformly across every view.

## Business Problem

AtliQ Hardware had historically made major decisions — including a costly push into Latin America — based on surveys, intuition, and basic Excel analysis. As the business scaled and transaction volumes grew, leadership could no longer rely on manual reporting to understand:

- Where revenue and profit were actually being generated, and where they were leaking
- How actual performance compared to internal benchmarks and prior-year results
- Where inventory and demand-forecasting risk was building up before it hit the P&L

This dashboard replaces that ad-hoc process with a single source of truth.

## Objectives & Key Business Questions

- Which regions, products, and customers are driving — or dragging down — profitability?
- Is the business margin-healthy, and if so, why is net profit still negative?
- How accurate is AtliQ's demand forecast, and where is that accuracy weakest?
- Is inventory risk skewed toward overstock (Excess Inventory) or understock (Out of Stock), and for which products/customers?
- How is AtliQ's PC market share trending against named competitors over time?
- How concentrated is revenue by channel and by customer?

---

## Dashboard Walkthrough

### 🏠 Home Page

The landing page is the navigation hub for the whole report. Each tile routes a different stakeholder to the view built for them:

| Tab | Purpose |
|---|---|
| **Info** | Download the user manual and get oriented on the tool |
| **Finance View** | Pull a P&L statement for any customer / product / country, aggregated over any time period |
| **Sales View** | Analyze customer performance across Net Sales, Gross Margin, and a profitability/growth matrix |
| **Marketing** | Analyze product performance across Net Sales, Gross Margin, and a profitability/growth matrix |
| **Supply Chain View** | Track Forecast Accuracy, Net Error, and risk profile by product, segment, category, customer |
| **Executive View** | A top-level dashboard consolidating insights across every dimension of the business |
| **Support** | Connect with a support specialist to resolve issues |

### 📈 Executive View

The single screen a CXO would actually look at. Top-row KPI cards carry color-coded benchmarking, with everything else drillable below.

| KPI | Value | Benchmark |
|---|---|---|
| Net Sales | $508.43M | $108.41M |
| Gross Margin % | 36.98% | 36.34% (+1.74 pts) |
| Net Profit % | -14.62% | -6.30% |
| Forecast Accuracy % | 81.53% | 80.64% (+1.1 pts) |

It also includes: revenue split by Division (PC / P&A / N&S) and by Channel (Retailer / Direct / Distributor); a sub-zone breakdown (India, NA, ROA, NE, SE, ANZ) with margin, market share, and risk flags; a five-year revenue/margin/market-share trend; AtliQ's PC market share against named competitors (bp, dale, innovo, pacer); and Top 5 Customers and Top 5 Products by revenue.

### 💰 Finance View

A full Profit & Loss statement — from Gross Sales down to Net Profit % — with Benchmark and Change% columns for every line item: invoice deductions, manufacturing/freight/other cost, COGS, gross margin, operating expense, and net profit. Paired with a net sales trend chart and a Top/Bottom Products & Customers breakdown by region and segment.

### 🤝 Sales View

Customer-level performance (Net Sales, Gross Margin $/%) for every account, a Performance Matrix plotting customers by region on a GM% vs. Net Sales grid, a segment-level product table, and a unit-economics breakdown showing how Gross Sales decomposes down to Gross Margin.

### 📣 Marketing View

The product-side mirror of the Sales View: segment-level Net Sales/GM/Net Profit, a Performance Matrix by division (PC / P&A / N&S), a region/market/customer performance table, and unit economics with a Gross Margin → Operating Expense → Net Profit waterfall.

### 🚚 Supply Chain View

Forecast Accuracy %, Net Error, and ABS Error KPIs (current vs. Last Year), an accuracy/net error trend chart, and customer- and product-level forecast tables flagging each as **EI (Excess Inventory)** or **OOS (Out of Stock)** risk.

---

## Key Insights

- **The LATAM problem is visible in the numbers.** LATAM contributes just **$1.86M** in net sales — 0.4% of the company's $508M total — against APAC's $275M, NA's $119M, and EU's $113M. This regional imbalance is consistent with AtliQ's well-known struggles establishing a presence in Latin America.
- **Margin-healthy, but profit-negative.** Company-wide Gross Margin sits at a respectable ~37% (every product segment lands in a tight 36.9–37.5% band), yet Net Profit % is **-14.62%** across the board. The waterfall view shows Operating Expense (~$262M) outweighing Gross Margin (~$188M) — this looks like a cost-structure problem, not a pricing or COGS problem.
- **Blended forecast accuracy hides customer-level risk.** The headline Forecast Accuracy of 81.5% looks strong, but several major accounts — Notebillig (41.5%), Staples (42.8%), Circuit City (46.0%), Epic Stores (44.2%) — sit far below that average and are flagged as Excess Inventory (EI) risk.
- **Inventory risk runs in both directions at once.** Accessories, Desktop, and Networking are flagged Excess Inventory (EI), while Storage and Peripherals are flagged Out of Stock (OOS) with Net Errors of roughly -198.7K and -1.02M units respectively — overstock and stockout problems happening simultaneously across the portfolio.
- **Heavy channel concentration.** Roughly 70% of revenue flows through the Distributor channel, versus 16% Direct and 14% Retail — a notable reliance on third-party distribution.
- **Customer concentration is moderate but real.** The top 5 customers account for 37.5% of total net sales, with Amazon alone contributing 13.6%.
- **Regional margin gap.** North America posts the highest Gross Margin at 45.0%, well ahead of APAC (34.7%) and EU (34.2%) — despite generating less total revenue than APAC.

## Tools & Skills Demonstrated

- **Power BI Desktop & Service** — multi-page report design, role-based navigation, bookmarks
- **Data Modeling** — star-schema design across sales/actuals and forecast fact tables with customer, product, date, and market dimensions
- **DAX** — KPI measures, YoY and vs.-Target benchmarking, time intelligence (YTD/YTG), conditional risk flagging
- **Power Query** — data cleaning and transformation (ETL)
- **Dashboard UX** — consistent slicer/filter design, drill-down hierarchies, conditional formatting for risk (EI/OOS)
- **Data Storytelling** — translating raw metrics into role-specific narratives for Finance, Sales, Marketing, Supply Chain, and Executive audiences

## Metrics Glossary

| Term | Meaning |
|---|---|
| NS $ | Net Sales |
| GM % / GM $ | Gross Margin (percentage / value) |
| RC % | Revenue Contribution % |
| BM | Benchmark |
| LY | Last Year |
| MS % | Market Share % |
| YTD / YTG | Year-to-Date / Year-to-Go |
| EI | Excess Inventory (risk flag) |
| OOS | Out of Stock (risk flag) |

## Repository Structure

```
Business-Insights-360/
└── README.md
```

> 📌 This repository is documentation/portfolio-only. The `.pbix` file and underlying dataset are not included.

## Future Enhancements

- Add SKU-level drill-through pages from the Marketing/Sales views
- Introduce what-if parameters for forecast scenario planning
- Expand competitor market-share tracking with additional external data
- Schedule automated data refresh via Power BI Service / Gateway

## Disclaimer

AtliQ Hardware is a fictional company used as a case study for practicing real-world business intelligence workflows. All figures shown are illustrative sample data, not actual financial results.

## Author

**Muhammad Yousaf**

📧 [yousafzadran50@gmail.com](mailto:yousafzadran50@gmail.com) • 🔗 [LinkedIn](https://www.linkedin.com/in/muhammad-yousaf-b67706240/) 

---

⭐ If you found this project useful or interesting, consider giving it a star!
