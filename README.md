# bangladesh-health-bulletin-analysis

# Evolving Health Indicators in Bangladesh: Comparative Analysis of 2019 and 2023 Health Bulletins

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-1.3%2B-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.4%2B-blue)
![License](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey)

A comprehensive data science analysis of Bangladesh's healthcare system using official Health Bulletins from 2019 and 2023, supplemented with recent research insights (2020-2025).

## 📖 Overview

This research project analyzes key health indicators in Bangladesh through:
- **Data extraction** and cleaning from DGHS Health Bulletins
- **Comparative analysis** of 2019 vs. 2023 health metrics
- **Statistical modeling** and visualization of healthcare trends
- **Policy recommendations** based on data-driven insights

## 📊 Key Findings

### Maternal and Child Health
- Institutional deliveries increased from 21% to 53% over a decade
- Antenatal care coverage reached 82% (2019), with rural disparities persisting
- Under-5 mortality reduced from 38 to 33 per 1,000 live births (2019-2023)

### Disease Control
- Web-based surveillance expanded from 18 to 25+ diseases
- Malaria incidence shows steady decline with targeted interventions
- DHIS2 implementation improved outbreak response times by 20%

### Healthcare Infrastructure
- Analysis of workforce distribution and infrastructure gaps
- Identification of rural-urban disparities in service delivery
- Assessment of healthcare financing mechanisms

## 🗂️ Project Structure


bangladesh-health-bulletin-analysis/
│
├── data/
│ ├── raw/ # Original datasets from Health Bulletins
│ ├── processed/ # Cleaned and transformed data
│ └── external/ # Supplementary research papers
│
├── notebooks/
│ ├── health_bulletin_2019_and_2023.py # Main analysis notebook
│ ├── data_extraction.ipynb # PDF-to-CSV conversion
│ └── visualization.ipynb # Figure generation
│
├── papers/
│ ├── main_paper.pdf # LNCS formatted research paper
│ └── references.bib # Bibliography
│
├── results/
│ ├── figures/ # Generated visualizations
│ └── tables/ # Statistical summaries
│
└── docs/
├── methodology.md # Research methodology
└── data_dictionary.md # Variable descriptions


## 🛠️ Installation & Usage

### Prerequisites

pip install pandas matplotlib seaborn scikit-learn pdfplumber kagglehub

# Download and process Health Bulletin data
python health_bulletin_2019_and_2023.py

Analysis Pipeline

Data Collection: Automated download from Kaggle/DGHS sources
Preprocessing: Cleaning, normalization, and feature engineering
Exploratory Analysis: Statistical summaries and correlation studies
Visualization: Generation of publication-ready figures
Modeling: Trend analysis and predictive insights

📈 Key Visualizations

The project generates several important figures:

Mortality rate comparisons (2019 vs. 2023)
Healthcare infrastructure distribution
Disease burden timelines
Workforce frequency analysis
Demographic category distributions

📚 Research Outputs

Academic Paper

Title: "Evolving Health Indicators in Bangladesh: A Comparative Analysis of 2019 and 2023 Health Bulletins Using Data Science Tools"
Conference: LNCS format
Contributions: Data-driven policy recommendations, methodological framework for health bulletin analysis

Datasets

Cleaned mortality data (2019, 2023)
Disease statistics with temporal trends
Healthcare infrastructure metrics
Workforce distribution analysis
🤝 Contributing

We welcome contributions in:

Data validation and quality assurance
Additional analysis methodologies
Visualization improvements
Translation of findings into policy briefs

📄 License

This project is licensed under Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0).

👥 Authors

Farjana Yesmin - Independent Researcher (farjanayesmin76@gmail.com)

Nusrat Shirmin - Independent Researcher (shirmin.ns@gmail.com)

🙏 Acknowledgments

Directorate General of Health Services (DGHS), Bangladesh for data access

Kaggle community for dataset hosting infrastructure

Research contributors cited in the bibliography

📫 Contact

For questions or collaborations, please contact:

Farjana Yesmin: farjanayesmin76@gmail.com

Nusrat Shirmin: shirmin.ns@gmail.com

*This research contributes to Sustainable Development Goal 3: Good Health and Well-being*
