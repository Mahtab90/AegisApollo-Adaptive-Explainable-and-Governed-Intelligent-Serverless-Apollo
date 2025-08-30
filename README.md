# EU MRV Emissions Analytics

This repository provides tools and scripts to process the **EU MRV (Monitoring, Reporting and Verification)** emissions datasets published by EMSA.  
The goal is to extract, analyze, and visualize **annual CO₂ emissions** for ships operating in European waters (2018–2024).

---

## Overview
- Process official EMSA MRV Excel files (2018–2024).
- Compute **annual total CO₂ emissions** across all reported ships.
- Save results in clean CSV format for reproducibility.
- Generate publication-quality visualizations for academic papers.
- Designed with **large-scale Excel handling** in mind (memory-efficient).

---

## Structure
EU-MRV-Analytics/
│
├── data/ # Raw EMSA MRV Excel files (2018–2024)
├── results/ # CSV outputs and plots
├── scripts/compute_mrv_co2.py # Main analysis script
├── requirements.txt # Python dependencies
└── README.md # Documentation


---

## Installation
1. Clone the repository:
  
   git clone https://github.com/<your-username>/EU-MRV-Analytics.git
   cd EU-MRV-Analytics
Install dependencies:

bash

pip install -r requirements.txt
▶️ Usage
Place your EMSA MRV Excel files (2018–2024) into the data/ folder.
Example filenames:

2018-v272-05072025-EU MRV Publication of information.xlsx

2019-v227-28052025-EU MRV Publication of information.xlsx

...

2024-v55-30082025-EU MRV Publication of information.xlsx

Run the analysis script:


python scripts/compute_mrv_co2.py
Check the results/ folder for:

EU_MRV_CO2_Totals.csv → clean CSV file with Year & Total Emissions.

EU_MRV_CO2_Trends.png → line chart of annual emissions.

📊 Example Output
Console output:


Processing 2018 ...
  ✔ 2018: 145.35 Mt CO₂
Processing 2019 ...
  ✔ 2019: 141.20 Mt CO₂
...
Results saved to:
  - results/EU_MRV_CO2_Totals.csv
  - results/EU_MRV_CO2_Trends.png
CSV file (EU_MRV_CO2_Totals.csv):


Year,Total_CO2_Mt
2018,145.35
2019,141.20
2020,118.00
2021,124.00
2022,131.00
2023,134.00
2024,137.00
📦 Dependencies
Python 3.9+

openpyxl

matplotlib

Install via:


pip install -r requirements.txt
🔬 Research Context
This repository is part of the AegisApollo framework:

Adaptive data workflows for maritime analytics.

Explainable rules (Association Rule Mining) for interpretability.

Governed ingestion pipelines with compliance-ready design.

The results support academic studies on maritime decarbonization and compliance with EU Fit for 55 and IMO 2030/2050 targets.
