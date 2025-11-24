# Sustainable AI Emissions Forecasting & Green Cloud Analysis
By Avinaash Devasena Ganesh<br>
(Data Science | Sustainable Technology | Responsible AI)

This project explores the environmental impact of AI and cloud workloads using hardware lifecycle emissions, energy consumption data, and grid-level electricity demand.
Using the Boavizta Environmental Footprint dataset and Our World In Data (OWID) Electricity Demand dataset, I analyzed:

• Lifecycle greenhouse gas emissions of datacenter hardware<br>
• Manufacturing vs. use-phase carbon contributions<br>
• Annual energy use per server<br>
• 5-year emissions forecast for AI workloads<br>
• Electricity demand of a hypothetical 10-million-server cloud provider<br>
• Comparison of cloud energy demand to Europe’s electricity grid<br>

The final outcome includes insights, visualizations, forecasting models, and high-impact sustainability recommendations for AI/Cloud companies.

## Data Sources

<a href="https://github.com/Boavizta/environmental-footprint-data" target="_blank">Boavizta Project – Environmental Footprint Data</a><br>
<a href="https://ourworldindata.org/energy" target="_blank">OWID Electricity Demand Dataset</a>

## Methodology
1. Data Cleaning<br>
Converted inconsistent date formats<br>
Imputed missing values using median by category and subcategory<br>
Removed high-null columns (>60%)<br>
Standardized units and formats<br>

2. Feature Engineering<br>
Created additional features like:<br>
annual_lifecycle (gCO₂e per hardware per year)<br>
gwp_use (use-phase emissions)<br>
gwp_manufacturing<br>
Ratio shares of use-phase vs manufacturing<br>

3. Time-Series Modeling<br>
Used linear and exponential regression to forecast emissions from 2022–2026, using cleaned 2019–2021 values as baseline.<br>
Result: Model predicts emissions rising from ~2.2 tCO₂e → ~2.7 tCO₂e per server by 2026.

4. Cloud Energy Footprint Modeling<br>
Built a hypothetical scenario for a cloud provider with 10 million servers:<br>
Calculated aggregate electricity use using median Boavizta values<br>
Compared against Europe’s overall grid consumption<br>
Used log-scale charts + pie charts for visibility<br>
