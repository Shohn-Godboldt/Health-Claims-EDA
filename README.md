
# Health-Claims-EDA

This project demonstrates a complete exploratory data analysis (EDA) workflow using **R**, **Quarto**, and the **openFDA API** to examine adverse event reports for pharmaceutical drugs.  
The goal of this personal project was to automate data extraction, normalization, visualization, and summary reporting — all reproducible through a single Quarto render command.

---

##  Overview
- **Language & Tools:** R, Quarto, ggplot2, dplyr, lubridate, janitor, tidyverse  
- **Data Source:** [openFDA Drug Event API](https://open.fda.gov/apis/drug/event/)  
- **Output:** Interactive Quarto report with plots, tables, and markdown summaries  
- **Purpose:** Demonstrate end-to-end data wrangling, trend analysis, and visualization automation.

---

##  Key Features
- Pulls real-world FDA adverse event data dynamically
- Normalizes nested JSON data into tidy tabular format
- Performs grouped analyses by **reaction type**, **age**, and **sex**
- Generates multiple visual outputs:
  - Pareto chart of top adverse reactions  
  - Demographic distributions (age × sex patterns)  
  - Serious vs non-serious outcome ratios  
  - Monthly trend visualization of reported events
- Saves results as clean `.png` outputs and markdown summaries.

---

##  How to Run
To reproduce this analysis locally:

```bash
# Clone the repository
git clone https://github.com/Shohn-Godboldt/Health-Claims-EDA.git
cd Health-Claims-EDA

# Render the report (example: Metformin data)
quarto render index.qmd -P drug:metformin -P start_date:2024-01-01 -P end_date:2024-03-31
