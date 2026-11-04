# Nobel Prize Historical Data Analysis (1901 - 2020)

This project presents a comprehensive, interactive, and chronological exploratory data analysis (EDA) of Nobel Prize laureates from 1901 to 2020 using the Python data science ecosystem.

## Project Overview

The Nobel Prize has been rewarding outstanding achievements in physics, chemistry, physiology or medicine, literature, and peace since 1901, with the addition of economic sciences in 1969. This project cleans, explores, structures, and visualizes historical datasets to extract trends about global research distribution, prize sharing, demographics, gender representation, and laureate age progressions.

## Tech Stack & Libraries Used
- **Data Manipulation:** `pandas`, `numpy`
- **Static Visualizations & Trendlines:** `seaborn`, `matplotlib`
- **Interactive Visualizations:** `plotly.express` (Donut, Sunburst, Choropleth, Line & Bar Charts)

## Key Features & Analyses

### 1. Data Processing and Cleaning
- Resolved type conversions by parsing the unstructured `birth_date` columns into proper `datetime` formats.
- Processed fractional shares (e.g., "1/4", "1/2") into floating-point numerical percentages (`share_pct`) to accurately study reward division over time.
- Analyzed missing records, confirming that null fields for birth info correlate natively to organization-based laureates (e.g., Red Cross, WFP).

### 2. Gender Demographics
- Generated a Plotly Donut Chart indicating historical gender representation (identifying that women hold only ~6% of all awarded prizes).
- Segmented gender counts across all 6 individual fields, highlighting specific areas with larger historical gender imbalances.
- Isolated and highlighted earliest historic female pioneers such as Marie Curie, Baroness Bertha von Suttner, and Selma Lagerlöf.

### 3. Chronological Tracking & Repeat Winners
- Filtered out and identified the 6 unique repeating laureates (individuals and organizations) who achieved the distinguished feat of winning more than once.
- Calculated 5-year rolling averages to visualize how the frequency of awards and sharing formats have shifted from the early 20th century to modern times.

### 4. Geographical & Institutional Dominance
- Visualized the top 20 most successful birth countries of laureates using horizontal bar charts.
- Plotted an interactive **Choropleth World Map** depicting winner concentrations globally.
- Analyzed cumulative growth trends per country over decades, displaying shifts in geopolitical scientific dominance.
- Mapped institution hierarchies (Country ➔ City ➔ Organization) using a multi-level **Sunburst Chart**.

### 5. Age Analytics & Trends
- Constructed custom logic to calculate the age of laureates at the time they received their prizes (`winning_age`).
- Isolated the youngest (Malala Yousafzai, age 17) and oldest (John B. Goodenough, age 97) Nobel laureates.
- Plotted distributions and tracked shifting age profiles across categories using boxplots and multi-faceted regression modeling (`lmplot`), indicating a steady increase in the average age of laureates in science fields.
  
