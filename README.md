# The Green Divide  
### Europe’s Two-Speed Transition to 2030

![Project Cover](report/cover_image.png)

## About the Project
**The Green Divide** is a data analysis and visualization project exploring the uneven pace of the energy transition across Europe.

Going beyond EU averages, the project highlights:
- Structural differences between European regions  
- The gap between **Electricity** and **Transport** sector transitions  
- Energy vulnerability revealed by the 2022 geopolitical crisis  

📄 **[Read the Final Report (PDF)](report/final_report.pdf)**

---

## Repository Structure

```text
The-Green-Divide/
├── data/
│   ├── raw/          # Original data (Eurostat, UNECE, OWID)
│   └── output/       # Cleaned CSVs for visualization
├── notebooks/
│   └── my_project.ipynb
├── report/
│   ├── report_finale.pdf
│   └── cover_image.png
├── .gitignore
└── requirements.txt
```

## How to Reproduce the Analysis

```bash
git clone https://github.com/lolluz01/The-Green-Divide.git
cd The-Green-Divide
pip install -r requirements.txt
jupyter notebook notebooks/my_project.ipynb
```

All data processing steps are fully reproducible using the provided notebook.

## Data & Methodology
Data sources include **Eurostat** (official EU statistics), **UNECE** (SDG indicators), and **Our World in Data**.

### Processing Pipeline
The analysis is automated via Python (`pandas`, `requests`). The workflow includes:
* **Automated Extraction:** Scripts fetch the latest data directly from Eurostat APIs.
* **Regional Grouping:** Countries are aggregated into macro-regions (Nordics, Western, Southern, Eastern Europe) to identify geographical trends.
* **Sector Analysis:** Disaggregation of renewable shares into Electricity, Heating, and Transport.
* **Resilience Metrics:** Merging renewable data with import dependency ratios to assess energy security.

---

## Visualizations
The clean datasets in the `data/output/` folder are optimized for tools like **Flourish**, or **Datawrapper**.
| Output File | Recommended Viz | Description |
| :--- | :--- | :--- |
| `eurostat_sector_gap_flourish.csv` | **Line Chart Race** | Comparing the speed of transition between Electricity and Transport sectors. |
| `eurostat_regional_trends.csv` | **Line Chart (Small Multiples)** | Trends comparison across the 4 European macro-regions. |
| `war_impact_scatter.csv` | **Scatter Plot** | Correlation between % Renewables (Axis X) and Import Dependency (Axis Y). |
| `race_to_zero_growth.csv` | **Slope Chart / Dumbbell** | Growth of renewable share from 2012 to 2022 by country. |

---

## License

This project is licensed under the  
**Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

You are free to:
- **Share** — copy and redistribute the material in any medium or format  
- **Adapt** — remix, transform, and build upon the material  

Under the following terms:
- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made.

🔗 https://creativecommons.org/licenses/by/4.0/


---

### Author
**Lorenzo Lecci**

*Data Science Student*
