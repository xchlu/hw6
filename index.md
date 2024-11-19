---
layout: default
title: Visualizations of Building Inventory Data
---

# Visualizations of Building Inventory Data

## Chart 1: Building Count by Decade and Usage
This chart visualizes the number of buildings constructed in each decade, categorized by their usage description. The x-axis represents the construction decade, grouped into 10-year intervals, while the y-axis shows the total number of buildings constructed during that time. Different usage categories are represented by distinct colors to allow comparisons across categories. 
<iframe src="docs/chart1.html" width="800" height="600" frameborder="0" style="border: 1px solid black;"></iframe>

### Design Choices
- **Encoding Types**: 
  - X-axis uses ordinal encoding for grouped decades.
  - Y-axis uses quantitative encoding for the number of buildings.
  - Color uses nominal encoding to differentiate `Usage Description` categories. A categorical palette was chosen for clear visual separation.
- **Color Scheme**: Each category is assigned a distinct color, emphasizing differences in building usage over time.
- **Data Transformations**: In the Python notebook, missing values in `Year Constructed` and `Usage Description` columns were removed. The years were grouped into 10-year intervals for better readability and reduced axis clutter.

### Interactivity
Although this chart does not have explicit interactivity beyond Altair's default pan and zoom capabilities, grouping years into decades improves readability and allows for easier comparison across time periods.

---

## Chart 2: Total Building Square Footage by County
This chart highlights the total building square footage for the top 20 counties with the largest building areas. The x-axis represents the counties, sorted in descending order of their total square footage, and the y-axis displays the summed area for each county. A gradient color scale is used to indicate the magnitude of total square footage.
<iframe src="docs/chart2.html" width="800" height="600" frameborder="0" style="border: 1px solid black;"></iframe>

### Design Choices
- **Encoding Types**:
  - X-axis uses nominal encoding for county names, sorted by descending total square footage.
  - Y-axis uses quantitative encoding for the summed square footage.
  - Color uses quantitative encoding with a gradient scale to emphasize differences in building square footage.
- **Color Scheme**: The gradient scale ("blues") was chosen to provide a visually intuitive sense of magnitude, with darker blue representing larger total square footage.
- **Data Transformations**: In the Python notebook, rows with missing values in `County` or `Square Footage` columns were removed. Data was aggregated by county, and the top 20 counties with the highest total square footage were selected for visualization.

### Interactivity
Tooltips were added to allow users to hover over bars and view detailed information about the county name and total square footage. This feature provides clarity and enables users to explore individual counties more deeply.

---

## Links
- [The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)
- [The Analysis Notebook](https://github.com/xchlu/hw6/blob/main/Workbook.ipynb)
