# Tech Properties: August 2023 Sales Performance Analysis

An Excel-based analysis of lead conversion for Tech Properties, a real estate company specializing in land and property sales across Nigeria.

## Table of Contents

- [Background](#background)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [Known Data Notes](#known-data-notes)
- [Tools Used](#tools-used)
- [Repository Structure](#repository-structure)

## Background

Tech Properties monitors its monthly sales to understand growth trends and market responsiveness. The business was concerned about an apparent **decline in property and land sales in August 2023**. This project analyzes August's lead and sales data to identify patterns, anomalies, and drivers of conversion.

The dataset showed **no recorded sales in June or July**, so a true month-over-month decline could not be confirmed. The analysis focuses on explaining August performance.

## Objectives

Assess how the following factors affect **conversion rate (CR)**:

1. Date (week of the month)
2. Location (state)
3. Product type
4. Client gender
5. Property inspection attendance

## Dataset

| Item | Detail |
|---|---|
| File | `sales_dataset.xlsx` |
| Period | 1 August 2023 to 31 August 2023 |
| Records | 225 leads, 100 paid sales |
| Dimensions | Salesperson, state, product type, client gender, inspection status, week of month |

**Conversion rate** = Paid sales ÷ Total leads

## Methodology

1. **Load and clean** the data using Power Query in Excel.
2. **Add missing fields**: a sales status column and a week-of-the-month column.
3. **Fix inconsistencies**:
   - Removed the client phone number column (inaccurate and not relevant).
   - Standardized "PH" to "Port Harcourt" in the state column.
4. **Analyze** conversion rate across each dimension (primary analysis).
5. **Correlate** salesperson-level conversion with client gender, product mix, and inspection attendance (secondary analysis).

## Key Findings

**Overall:** 225 leads, 100 paid sales, **44.44% conversion rate**. Conversion efficiency is strong, but total sales volume is low, which points to lead volume rather than closing ability as the main constraint.

### Inspections
| Inspected | Leads | Paid Sales | CR |
|---|---|---|---|
| Yes | 171 | 94 | 54.97% |
| No | 54 | 6 | 11.11% |

### Location
| State | Leads | Paid Sales | CR |
|---|---|---|---|
| Lagos | 132 | 67 | 50.76% |
| Port Harcourt | 93 | 33 | 35.48% |

### Product Type
| Type | Leads | Paid Sales | CR |
|---|---|---|---|
| Residential | 99 | 64 | 64.65% |
| Commercial | 104 | 36 | 34.62% |
| Industrial | 22 | 0 | 0% |

### Client Gender
| Gender | Leads | CR |
|---|---|---|
| Male | 101 | 72.28% |
| Female | 124 | 21.77% |

### Salesperson Performance
| Salesperson | Paid | Leads | CR |
|---|---|---|---|
| Ngozi | 15 | 21 | 71.4% |
| Funmi | 28 | 49 | 57.1% |
| Chukwudi | 18 | 43 | 41.9% |
| Chioma | 20 | 48 | 41.7% |
| Olumide | 14 | 42 | 33.3% |
| Ahmed | 5 | 22 | 22.7% |

### Timing
- Week 1 had the highest conversion rate (**51.72%**), with conversion trending lower later in the month.
- **Week 4 shows a 0% conversion rate across all salespersons**, which needs investigation (operational issue or data recording gap).

### Correlation Highlights (salesperson level)
- Inspections and conversion: strong positive correlation (about +0.88).
- Residential share and conversion: positive (about +0.77); commercial (about -0.60) and industrial (about -0.67) are negative.
- Male client share and conversion: strong positive; female client share: strong negative.

## Recommendations

1. **Clarify the data discrepancy** for June and July with the Senior Business Analyst and set sales benchmarks.
2. **Grow lead volume** through new channels (digital marketing, partnerships, referrals) and added team capacity.
3. **Optimize the inspection funnel** with flexible scheduling, pre-inspection materials, and virtual inspections.
4. **Tailor sales strategy for female clients** through research, targeted messaging, and best-practice workshops.
5. **Replicate Lagos success** in Port Harcourt; provide targeted support and consider lead reallocation by salesperson strength.
6. **Focus on Residential**, diagnose Commercial challenges, and review the viability of Industrial.
7. **Coach low performers** (Ahmed, Olumide) and set up peer learning with top performers (Funmi, Ngozi).
8. **Investigate the Week 4 anomaly** immediately.

## Limitations

- Data covers August only, so no true decline analysis is possible.
- No data on marketing campaigns, economic conditions, competitors, or detailed customer inquiries.
- No price information, so price-range analysis was not possible.
- Revenue was assumed to be one unit per paid sale.
- Correlations are calculated across only six salespeople, so they are indicative rather than conclusive.

## Known Data Notes

Minor inconsistencies in the source report worth reconciling before publishing:

- Lagos CR appears as both 50.79% and 50.76% (67 ÷ 132 = 50.76%).
- Gender correlation is quoted as ±0.80 in the text but ±0.89 in the table.
- The recommendation citing Ngozi as strong with female clients is not supported by a gender-by-salesperson breakdown in the analysis.
- The Week 4 summary and weekly CR table are not included in the report; add them to support the 0% finding.

## Tools Used

- Microsoft Excel (analysis, pivot tables, correlation)
- Power Query (data loading and cleaning)

## Repository Structure

```
Tech-Properties/
├── README.md
├── data/
│   └── sales_dataset.xlsx
├── analysis/
│   └── tech_properties_analysis.xlsx
└── report/
    └── tech_properties_report.docx
```

*Adjust the structure above to match your actual files.*
