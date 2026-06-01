# London-Airbnb-Spatial-Analysis
A visual and spatial analysis of London's Airbnb market using t-SNE, K-Means clustering and Geographically Weighted Regression (GWR).

## Description
This project investigates the structural segmentation and spatial dynamics of the Airbnb market in London. Using K-Means clustering and Geographically Weighted Regression (GWR), the research identifies how host types and geographical location influence pricing, proving that spatially-aware models significantly outperform standard global OLS regressions in predicting urban market trends.

## Data Availability & Replication
Due to file size restrictions, the raw, uncompressed `listings.csv` dataset from the accompanying London Airbnb spatial analysis workflow is not hosted directly within this repository. 

To replicate the companion spatial pipelines, econometric models, and machine learning workflows:
1. Download the historical web-scraped archive directly from the open-source provider: [Inside Airbnb - London Data Archive](http://insideairbnb.com/get-the-data/)
2. Select the **December 2019** dataset compilation for the Airbnb data modeling.
3. For the public health analysis, utilize the ONS life expectancy records filtered specifically to the **2017 to 2019** period. This establishes a clean, pre-pandemic cross-sectional baseline that avoids COVID-19 structural anomalies and perfectly aligns with the timeline of the Indices of Deprivation (IMD 2019) predictors.
4. Place the raw files into your local directory before running the processing notebooks.

## Methodology
The analysis follows a professional data science pipeline, as detailed in the included research report:

* **Data Preparation & Cleaning (Python):** Processed raw listings using `Pandas` and `GeoPandas`, including coordinate transformations and spatial subsetting for London boroughs.
* **Market Segmentation:** Applied **K-Means Clustering** to distinguish commercial operators from private hosts based on listing density and pricing behaviour.
* **Spatial Econometrics:** Implemented **Geographically Weighted Regression (GWR)** via the `mgwr` library to model "spatial non-stationarity"—revealing how price determinants (like reputation and room type) change across the city.
* **Visual Analytics:** Developed interactive dashboards in **Tableau** and static spatial plots in **Python** using `Matplotlib` to map local pricing drivers and cluster regimes.

## Technical Process & AI Transparency
In line with academic integrity and professional transparency, this project utilised AI assistance (ChatGPT/Gemini) as a technical co-pilot:
* **Troubleshooting:** Used to resolve complex 'Singular Matrix' errors in the GWR model by explaining the mathematical causes of local multicollinearity in specific London subsets.
* **Optimisation:** Used to improve the efficiency of `Matplotlib` plotting loops and vectorising Python logic for better performance.
* **Verification:** Used to cross-reference econometric definitions and ensure the final analysis addressed all requirements of the project mark scheme.
* **Author's Role:** All spatial interpretations, policy implications, and final model selections are the original work of the author.

## Technologies Used
* **Python:**  `Pandas`, `Numpy`, `mgwr`, `libpysal`, `geopandas`, `scikit-learn`, `Matplotlib`, `Seaborn`.
* **Visualisation:** `Tableau Desktop`.
* **Licence:** `Apache License 2.0`.

## Repository Structure
* `London_Airbnb_Research_Report.pdf`: Full technical report and visual analysis.
* `london_airbnb_spatial_analysis.ipynb`: Complete Python implementation with saved outputs and visualisations.
