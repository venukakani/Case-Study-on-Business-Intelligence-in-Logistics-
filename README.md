# Business Intelligence in Logistics
### Case Study — SOSE 2023 | University of Duisburg-Essen

> **Faculty of Engineering Sciences — Transport System and Logistics**  
> Submitted by: Venu Kakani (Matriculation No. 3100376) | M.Sc. Technical Logistics  
> Submitted to: Prof. Frank Marrenbach

---

## Table of Contents

- [Overview](#overview)
- [What is Business Intelligence?](#what-is-business-intelligence)
- [Why BI in Logistics?](#why-bi-in-logistics)
- [BI Tools Covered](#bi-tools-covered)
- [Case Studies](#case-studies)
  - [Task A — ABC/XYZ Analysis (Computer AG)](#task-a--abcxyz-analysis-computer-ag)
  - [Task B — Distribution Cost Optimization (Snack Deliveries)](#task-b--distribution-cost-optimization-snack-deliveries)
- [Future Trends](#future-trends)
- [Limitations](#limitations)
- [References](#references)

---

## Overview

The logistics and supply chain sector generates enormous volumes of data daily — spanning clients, freight forwarders, warehousing, transport, customs, and more. Without the right tools, this data can be lost or misinterpreted, leading to poor decisions and reduced profitability.

This case study explores how **Business Intelligence (BI)** — specifically **Microsoft Power BI** — can be applied to real logistics challenges:

- Performing **ABC/XYZ inventory analysis** for warehouse optimization
- Evaluating **distribution network scenarios** to minimize transportation costs

---

## What is Business Intelligence?

Business Intelligence (BI) refers to a broad set of technologies, tools, and processes that allow organizations to collect, analyze, and interpret data to make informed decisions. BI converts raw data into actionable information for strategic planning and operational improvement.

**Brief History:**
| Era | Milestone |
|-----|-----------|
| 1865 | Richard Millar Devens coins the term "business intelligence" |
| 1958 | Hans Peter Luhn (IBM) explores technology-driven BI |
| 1960s–70s | Early DSS, OLAP, and data warehouse systems emerge |
| 1990s | BI gains popularity but remains IT-heavy |
| 2000s–present | Self-service BI, cloud platforms, real-time processing |

---

## Why BI in Logistics?

BI delivers value across six core logistics functions:

| Function | Description |
|----------|-------------|
| **Data Integration** | Consolidates data from ERP, TMS, WMS, and external providers |
| **Data Analysis & Reporting** | Tracks KPIs, identifies trends, and surfaces growth opportunities |
| **Performance Measurement** | Monitors on-time delivery, order accuracy, inventory turnover, cost per unit |
| **Predictive Analytics** | Forecasts demand, optimizes routes, and allocates resources proactively |
| **Supply Chain Optimization** | Identifies inefficiencies in transportation, inventory, and supplier networks |
| **Decision Support** | Provides timely, data-driven insights for strategic and tactical decisions |

**Key benefits for logistics companies:**
- Greater insight into costs and profits
- Enhanced operational efficiency
- Increased load factors
- Optimized routes
- Better driver and vehicle management
- Deeper customer understanding

---

## BI Tools Covered

### Tools Discussed

| Tool | Vendor | Key Strength |
|------|--------|--------------|
| **Power BI** | Microsoft | Data integration, interactive dashboards, DAX modeling |
| **Tableau** | Salesforce | Visual analytics, user-friendly interface |
| **QlikView / Qlik Sense** | Qlik | Associative data model, self-service exploration |
| **SAP BusinessObjects** | SAP | Deep integration with SAP ERP/SCM ecosystem |
| **MicroStrategy** | MicroStrategy | Advanced analytics, mobile BI, reporting |

### Types of BI Tools

- **Spreadsheets** — Microsoft Excel for accessible reporting and goal tracking
- **Query & Visualization Tools** — Dashboards, scorecards, ad hoc reporting
- **OLAP Tools** — Multidimensional "slice and dice" analysis
- **Data Mining Tools** — Neural networks, ML, decision trees for predictive analytics

### Tool Selection Criteria

When choosing a BI tool, consider:
- Product features and ease of use
- Scalability and user interface options
- Access to disparate data sources
- Integration with existing platforms
- Reporting requirements and distribution modes

---

## Case Studies

### Task A — ABC/XYZ Analysis (Computer AG)

**Objective:** Optimize stock carrying costs for the spare parts business of Computer AG by classifying 10 materials across 12 months of sales data.

#### ABC Analysis

Classifies materials by **value contribution**:

| Class | Value % | Proportion |
|-------|---------|------------|
| **A** — High-value items | ~80% (70–80%) | ~10% of items |
| **B** — Intermediate items | ~15% (15–20%) | ~20% of items |
| **C** — Low-value items | ~5% (5–10%) | ~70% of items |

**Results:**
- **A-Articles:** M10, M2, M4 → account for ~80% of sales value
- **B-Articles:** M9, M1, M6
- **C-Articles:** M8, M3, M7, M5 → high inventory share, low sales contribution

#### XYZ Analysis

Classifies materials by **demand regularity** using the Variance Coefficient (VC = Standard Deviation / Mean):

| Class | Consumption Pattern | Predictability |
|-------|---------------------|----------------|
| **X** | Constant, rare fluctuations (VC < 30%) | High |
| **Y** | Trend/seasonal fluctuations | Medium |
| **Z** | Completely irregular (VC > 50%) | Low |

**Results:**
- **X-Articles:** M6, M1, M3 — highly predictable demand
- **Y-Articles:** M4, M2, M7, M8
- **Z-Articles:** M9, M10, M5 — highly irregular demand

#### Combined ABC/XYZ Matrix & Material Provisioning

| | X | Y | Z |
|---|---|---|---|
| **A** | — | M2, M4 | M10 |
| **B** | M1, M6 | — | M9 |
| **C** | M3 | M7, M8 | M5 |

**Provisioning strategy:**
- `BX, AY` → M1, M2, M4, M6 = **Just-In-Time (JIT)**
- `CX, BY, CY, CZ` → M3, M5, M7, M8 = **Stock-based provisioning**

> **Outcome:** ABC/XYZ analysis with Power BI enables faster classification, reduces manual effort, and provides clear visual results — helping eliminate material shortages, bottlenecks, and excess inventory.

---

### Task B — Distribution Cost Optimization (Snack Deliveries)

**Objective:** Evaluate four distribution network configurations for Snack Deliveries to minimize total transportation costs.

**Data overview (4 factory locations):**

| Factory | Volume (Cartons) | Customers Served |
|---------|-----------------|-----------------|
| Lorsch | 82,678 | 1,463 |
| Mannheim | 172,159 | 1,709 |
| Mönchengladbach | 276,286 | 1,702 |
| Vechta | 63,154 | 1,699 |
| **Total** | **594,277** | **1,730** |

**Transport assets:** Semitrailers (33 pallets) for factory/central routes; small trucks (500 cartons) for regional delivery.

#### Scenarios Evaluated

**Case A — Direct factory-to-customer supply**
- No intermediate warehouses
- Total cost: **€ 881,956.12**

**Case B — Factory → Central Warehouse (Flammersfeld) → Customers**
- Central warehouse location determined by geographic center of gravity based on factory coordinates
- Central warehouse coordinates: Lat 50.65, Lon 7.51 (Flammersfeld)
- Total cost: **€ 612,219.44** ✅ *(lowest)*

**Case C — Factory → Central Warehouse (customer-based CoG) → Customers**
- Central warehouse location based on customer geographic center of gravity
- Central warehouse coordinates: Lat 50.80, Lon 8.61
- Total cost: **€ 612,879.79**

**Case D — Factory → Central Warehouse → Regional Warehouses → Customers**
- Regional warehouses: Bispingen (53.13°N, 9.98°E), Flammersfeld (50.64°N, 7.53°E), Remseck am Neckar (48.85°N, 9.25°E)
- Total cost: **€ 878,317.65**

#### Cost Comparison

```
Case A:  €881,956.12   ████████████████████████████████
Case B:  €612,219.44   ██████████████████████  ← RECOMMENDED
Case C:  €612,879.79   ██████████████████████
Case D:  €878,317.65   ████████████████████████████████
```

**Key DAX formulas used in Power BI:**

```dax
-- Haversine distance between two geographic coordinates
Distance b/w Factory & Customer =
VAR d = ACOS(
    SIN(Table[Werk Lat(radians)]) * SIN(Table[Kunde Lat(radians)]) +
    COS(Table[Kunde Lat(radians)]) * COS(Table[Werk Lat(radians)]) *
    COS(Table[Werk Lon(radians)] - Table[Kunde Lon(radians)])
)
VAR distance = 6371 * d
RETURN distance

-- Weighted center of gravity (geographic midpoint)
X = DIVIDE(SUM(Data[Lat] * Data[OrderQty]), SUM(Data[OrderQty]))
Y = DIVIDE(SUM(Data[Lon] * Data[OrderQty]), SUM(Data[OrderQty]))
```

> **Recommendation:** Establish a central warehouse at **Flammersfeld (Case B)** — reducing total transportation costs by ~30% compared to direct delivery (Case A).

---

## Future Trends

| Technology | Key Application in Logistics |
|------------|------------------------------|
| **IoT** | Real-time shipment tracking, condition monitoring |
| **AI / ML** | Route optimization, demand forecasting, fraud detection |
| **Blockchain** | Tamper-resistant record-keeping, smart contracts |
| **Autonomous Vehicles** | Last-mile delivery, long-haul transport |
| **Cloud Computing** | Real-time data sharing, scalable platforms |
| **Robotics & Automation** | Warehouse picking, order fulfillment |
| **AR / VR** | Staff training, remote maintenance assistance |
| **Predictive Analytics** | Inventory optimization, risk management |
| **Advanced GPS** | Fleet tracking, precise route optimization |
| **Sustainability Solutions** | Green logistics, eco-friendly packaging |

---

## Limitations

| Challenge | Description |
|-----------|-------------|
| **Data Quality** | Incomplete, inconsistent, or outdated data reduces BI reliability |
| **System Integration** | Merging data from multiple platforms is complex and time-consuming |
| **Real-Time Availability** | Accessing live data from external partners can be difficult |
| **Analytical Complexity** | Logistics data involves many interdependent variables |
| **Predictive Limits** | Traditional BI may need augmentation with advanced ML models |
| **User Adoption** | Training and change management are critical for success |
| **Cost** | Infrastructure investment can be prohibitive for SMEs |

---

## References

1. Sherman, R. (2015). *Business Intelligence Guidebook*. Morgan Kaufmann.
2. Mahama, S. J. (2013). Key Performance Indicators in Supply Chain. *International Journal of Economics, Commerce, and Management*.
3. Shmueli, G., Bruce, P. C., & Yahav, I. (2017). *Data Mining for Business Analytics*. Wiley.
4. Watson, M., Lewis, S., & Cacioppi, P. (2012). *Supply Chain Network Design*. FT Press.
5. Vahdani, M. (2010). A Multi-Criteria Approach for Supplier Selection. *European Journal of Operational Research*.
6. Schlegel, G. L., & Trent, R. J. (2009). *Supply Chain Risk Management: An Emerging Discipline*.
7. Troyansky, O., & Gibson, T. (2015). *QlikView Your Business*. Wiley.
8. Lloyd, C. (2015). *Data-Driven Business Decisions*. Wiley.
9. Kalman, D. V. (2009). *Warehouse Management and Inventory Control*.
10. McNamara, T. (2008). ABC Inventory Analysis. *International Journal of Information Management*.
11. Negash, S. Business Intelligence. *Communications of the Association for Information Systems*, 13. https://doi.org/10.17705/1CAIS.01315
12. Gowthami, K., & Kumar, M. R. P. (2017). Study on business intelligence tools for enterprise dashboard development. *International Research Journal of Engineering and Technology*, 4(4), 2987–2992.
13. Grabińska, A., & Ziora, L. (2019). The Application of Business Intelligence Systems in Logistics. *System Safety: Human - Technical Facility - Environment*, 1(1), 1028–1035. https://doi.org/10.2478/czoto-2019-013

---

*Case Study submitted to the Faculty of Engineering Sciences, Transport System and Logistics, University of Duisburg-Essen — Summer Semester 2023.*
