# U.S. Flight Delay Patterns

An exploratory and explanatory visualization project using 538,837 U.S. domestic flights reported to the Bureau of Transportation Statistics for January 2023.

This project was completed for the **Data Visualization with Matplotlib and Seaborn** course in the Data Analyst Nanodegree. Part I systematically explores delay distributions and relationships; Part II turns the strongest result into a concise visual story.

## Project Highlights

- Reduced the official 100+ column monthly file to a documented 16-variable analysis extract without sampling rows.
- Built seven exploratory visualizations across univariate, bivariate, and multivariate analysis.
- Used a histogram, count plot, scatter plots, box plot, heatmap, and carrier facets.
- Separated canceled flights from arrival-delay calculations while retaining them in the source extract.
- Produced three polished explanatory visualizations around the morning-flight advantage.
- Exported both fully executed notebooks as standalone HTML reports.

## Key Findings

- About 22.1% of operated flights arrived at least 15 minutes late.
- Flights scheduled from 5–10 a.m. had a 16.8% delay rate, compared with 27.2% for flights scheduled from 5–10 p.m.
- The morning advantage appeared across the four largest carriers and most weekdays.
- Route distance had little standalone monotonic relationship with positive arrival-delay minutes; departure delay was much more closely related.

## Dataset

The analysis uses the January 2023 [Reporting Carrier On-Time Performance dataset](https://www.transtats.bts.gov/Fields.asp?gnoyr_VQ=FGJ) from the U.S. Bureau of Transportation Statistics. `data/flights_2023_01.csv` contains all rows from the official monthly archive with only the variables needed by the notebooks.

## Run Locally

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m jupyter lab
```

Open either notebook and choose **Restart Kernel and Run All Cells**. Both use the included relative path `data/flights_2023_01.csv`.

## Repository Structure

```text
.
├── data
│   └── flights_2023_01.csv
├── Part_I_exploration_template.ipynb
├── Part_I_exploration_template.html
├── Part_II_explanatory_template.ipynb
├── Part_II_explanatory_template.html
├── requirements.txt
└── README.md
```

## Limitations

One winter month cannot represent seasonal or long-run carrier performance. Arrival-delay rates exclude cancellations and do not control for airport, route, weather, or schedule-padding differences. The results are descriptive, not causal or predictive.
