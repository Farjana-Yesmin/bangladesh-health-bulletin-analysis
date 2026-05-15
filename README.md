# Evolving Health Indicators in Bangladesh: A Comparative Analysis of 2019 and 2023 Health Bulletins Using Data Science Tools

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/)
[![Dataset: Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF.svg)](https://www.kaggle.com/datasets/farjanayesmin/bangladesh-health-bulletin-2019-dataset)
[![Data: DGHS Bangladesh](https://img.shields.io/badge/Data-DGHS%20Bangladesh-green.svg)](http://www.dghs.gov.bd/)

---

## 📋 Overview

Bangladesh has made significant strides in improving its healthcare system over the past decade, yet persistent structural challenges — rural–urban disparities, workforce shortages, and out-of-pocket financing dominance — continue to limit equitable service delivery.

This project provides a **comprehensive, data-driven assessment** of Bangladesh's health system using publicly available government data from the DGHS **Health Bulletins 2019 and 2023**, supplemented by 25 recent studies (2020–2025). It covers seven healthcare domains:

Demographics · Maternal & Child Health · Disease Control · Healthcare Infrastructure · Workforce · Financing · Health Education & Services

### Key Contributions

1. A **data extraction and preprocessing pipeline** handling structured CSV (2019) and unstructured PDF (2023, 331 pages) sources across seven domains
2. **Statistical and visual analysis** with quantified metrics — correlation coefficients above 0.85 for key health-infrastructure relationships
3. **Validated machine learning models** (92% accuracy, R² = 0.87) demonstrating the potential of AI for healthcare planning in resource-limited settings
4. Integration and contextualisation of **25 recent studies (2020–2025)**
5. **Evidence-based, domain-specific policy recommendations** for digital health expansion, workforce retention, financing reform, and infrastructure equity

---

## 📊 Key Findings

### Progress Between 2019 and 2023

| Indicator | 2019 | 2023 | Change |
|---|---|---|---|
| Crude Death Rate (per 1,000) | 5.26 | 5.01 | ▼ 4.7% (p=0.032) |
| Under-5 Mortality (per 1,000 live births) | 38 | 33 | ▼ 13.2% |
| Maternal Mortality (per 100,000 live births) | 153 | 136 | ▼ 11.1% |
| Life Expectancy (years) | 72.3 | 73.7 | ▲ 1.9% |
| Institutional Deliveries | 53% | 59% | ▲ 11.3% |
| Antenatal Care Coverage | 47% | 52% | ▲ 10.6% |
| Childhood Vaccination Coverage | 82% | 85% | ▲ 3.7% |
| Malaria Cases | 12,521 | 7,289 | ▼ 42% |
| TB Case Detection | 62% | 68% | ▲ 9.7% |
| Stunting Prevalence | 31% | 24% | ▼ 7pp |
| Wasting | 9.7% | 7.8% | ▼ 1.9pp |
| Disease Surveillance Coverage | 18 diseases | 25+ diseases | ▲ 39% |
| DHIS2 Outbreak Response Time | 7 days lag | 2 days lag | ▼ 71% |
| Community Clinics | 13,800 | 14,200 | ▲ 2.9% |
| Workforce Vacancy Rate | 18% | 21.4% | ▲ 3.4pp ⚠️ |

### Critical Gaps Requiring Urgent Attention

| Challenge | Metric |
|---|---|
| Rural–urban ANC gap | Urban 68% vs. rural 43% (25pp gap) |
| Infrastructure quality gap | Urban 78% vs. rural 43% meeting standards (35pp gap) |
| Doctor-to-population ratio | Urban 1:1,850 vs. rural 1:4,200 |
| Rural workforce retention | 64% vs. 91% urban |
| Out-of-pocket expenditure | **67.2%** — highest in South Asia |
| Health expenditure as % of GDP | 2.8% vs. WHO-recommended 5% |

### Machine Learning Results

| Metric | Score |
|---|---|
| Classification Accuracy | **92%** |
| Precision | 0.89 |
| Recall | 0.91 |
| F1-Score | 0.90 |
| R² (regression) | 0.87 |
| Cross-validation | 90.5% ± 1.8% (5-fold) |

**Top Random Forest feature importance scores:** Infrastructure quality (0.28) · Doctor-to-population ratio (0.23) · Distance to nearest facility (0.19) · Household income (0.17) · Education level (0.13)

---

## 🏗️ Methodology Pipeline

```
Data Sources
├── Health Bulletin 2019: 7 structured CSV datasets (Kaggle)
└── Health Bulletin 2023: 331-page PDF (DGHS) → pdfplumber extraction

        │
        ▼
Preprocessing
├── Missing value handling (12.3% missing): mean/mode/forward-fill
├── Text normalisation, numerical formatting, date parsing
├── IQR-based outlier detection (287 duplicates removed)
└── Quality validation: 96.2% completeness · 98.7% consistency · 91% extraction accuracy

        │
        ▼
Analysis
├── Descriptive statistics (mean, median, std)
├── Inferential statistics (Pearson/Spearman correlation, t-tests, α=0.05)
├── Temporal trend analysis (2019 vs. 2023)
├── Machine learning:
│   ├── Random Forest (disease burden prediction, high-risk zone identification)
│   ├── Linear Regression (health outcome projection)
│   └── K-means Clustering (regional health profile segmentation)
└── 5-fold cross-validation for all ML models

        │
        ▼
Outputs
├── 9 publication-ready figures (300 DPI, matplotlib/seaborn)
├── Validated metrics with 95% confidence intervals
└── Evidence-based policy recommendations
```

---

## 🗂️ Data Sources

| Source | Format | Coverage |
|---|---|---|
| [DGHS Health Bulletin 2019](https://www.kaggle.com/datasets/farjanayesmin/bangladesh-health-bulletin-2019-dataset) | 7 structured CSVs | Demographics, disease, infrastructure, financing, workforce, education, services |
| [DGHS Health Bulletin 2023](http://www.dghs.gov.bd/) | 331-page PDF | Same 7 domains, extracted via pdfplumber |

All data are publicly available government publications containing no individual-level identifiable information.

---

## 🚀 Quick Start

### Installation

```bash
git clone https://github.com/Farjana-Yesmin/bangladesh-health-bulletin-analysis.git
cd bangladesh-health-bulletin-analysis

pip install pandas matplotlib seaborn scikit-learn pdfplumber kagglehub numpy scipy
```

### Run the Analysis

```bash
python health_bulletin_2019_and_2023.py
```

The script downloads the 2019 dataset from Kaggle automatically via `kagglehub`. Place the DGHS Health Bulletin 2023 PDF in the project directory before running.

---

## 📈 Figures Generated

| Figure | Description |
|---|---|
| Fig 1 | Distribution of categories in Demographics dataset |
| Fig 2 | Mortality rate comparisons (2019 vs. 2023) with 95% CI |
| Fig 3 | Distribution of service types (Health Services Utilization) |
| Fig 4 | Frequency distribution from Health Workforce dataset |
| Fig 5 | Malaria burden over years with program intervention timelines |
| Fig 6 | Malaria burden decline trend |
| Fig 7 | Top 10 categories in Health Education and Training dataset |
| Fig 8 | Top 10 categories in Healthcare Infrastructure dataset |
| Fig 9 | Comparison of mortality rates |

---

## 💡 Evidence-Based Policy Recommendations

**1. Digital Health Expansion**
Extend DHIS2 surveillance nationally to 25+ diseases; deploy telemedicine in underserved rural sub-districts (projected 40% improvement in care access); implement AI-driven early warning systems.

**2. Workforce Retention**
Rural incentive packages (salary supplements, housing, career pathways); scale digital CPD modules from 42% to 60% training coverage target; develop community health worker cadres for last-mile delivery.

**3. Financing Reform**
Pilot public health insurance in five districts by 2026; reduce OOP from 67.2% to 50% by 2030; explore blockchain-based claims processing.

**4. Infrastructure Equity**
Prioritise capital investment in the 50 lowest-performing rural facilities; deploy 100 mobile health units by 2027; expand public-private partnerships for diagnostic services.

**5. Governance and Accountability**
Real-time analytics dashboard integrating DHIS2 and HMIS; mandate quarterly machine-readable bulletin releases; establish an open national health data portal.

---

## 📁 Repository Structure

```
├── health_bulletin_2019_and_2023.py              # Full analysis pipeline
├── Fig 1 Distribution of Categories in Demographics Data.JPEG
├── Fig 2 Distribution of Role in Healthcare Financing Dataset.JPEG
├── Fig 3 Distribution of Service Types.JPEG
├── Fig 4 Frequency Distribution of Extracted Numbers from Health Workforce Data.JPEG
├── Fig 5 Malaria Burden Over the Years with Program Timelines.JPEG
├── Fig 6 Malaria Burden Over the Years.JPEG
├── Fig 7 Top 10 Most Common Categories in Health Education and Training Data.JPEG
├── Fig 8 Top 10 Most Common Categories in Healthcare Infrastructure Data.JPEG
├── Fig 9 Comparison of Mortality Rates.JPEG
├── Distribution of Demographic Values (2023).png
├── mortality_comparison.png
└── LICENSE
```

---

## 🔮 Future Work

- Extended time-series analysis (2015–2025) using ARIMA and Prophet forecasting
- GIS-based spatial analysis and union-level health equity heat mapping
- Expansion of disease prediction models to 10+ conditions
- Mixed-methods integration combining quantitative findings with patient-centred qualitative research
- Real-time monitoring dashboards with NLP-based extraction from unstructured health reports
- SAARC-level benchmarking against comparable LMICs (Vietnam, Ethiopia, Kenya)
- Health economic modelling of digital intervention return on investment

---

## 📝 Citation

```bibtex
@inproceedings{yesmin2026bangladesh,
  title     = {Evolving Health Indicators in Bangladesh: A Comparative Analysis of 2019 and 2023 Health Bulletins Using Data Science Tools},
  author    = {Farjana Yesmin and Nusrat Shirmin},
  booktitle = {Lecture Notes in Computer Science},
  publisher = {Springer},
  year      = {2025}
}
```

---

## 👥 Authors

- **Farjana Yesmin** — Independent Researcher, Boston, USA · farjanayesmin76@gmail.com · [ORCID: 0000-0003-0650-5133](https://orcid.org/0000-0003-0650-5133)
- **Nusrat Shirmin** — SSLCOMMERZ, Dhaka, Bangladesh · shirmin.ns@gmail.com · [ORCID: 0009-0003-7620-1204](https://orcid.org/0009-0003-7620-1204)

---

## 🙏 Acknowledgments

The Directorate General of Health Services (DGHS), Government of Bangladesh, for making Health Bulletins 2019 and 2023 publicly available. The anonymous reviewers for their constructive feedback.

---

## 📄 License

This project is licensed under Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) — see the [LICENSE](LICENSE) file for details.

> This research contributes to **Sustainable Development Goal 3: Good Health and Well-being**
