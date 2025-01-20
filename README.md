## 4. DATANVI Project: Data Investigation and Insights

### Introduction
This project focuses on analyzing traffic and flooding data in Manila using advanced spatial and temporal data analysis. It incorporates dynamic visualizations and a web-based dashboard built with Dash and Plotly.

### Prerequisites
Before running the project, ensure you have the following installed:

- Python 3.7+
- Dash (`pip install dash`)
- Plotly (`pip install plotly`)
- Pandas (`pip install pandas`)
- Geopy (`pip install geopy`)
- Scipy (`pip install scipy`)
- Dash Bootstrap Components (`pip install dash-bootstrap-components`)

Additionally, ensure access to the required datasets:
1. [MMDA Traffic Incident Data](https://www.kaggle.com/datasets/esparko/mmda-traffic-incident-data)
2. [AEGIS Dataset](https://www.kaggle.com/datasets/giologicx/aegisdataset)

The notebook uses `.parquet` versions of these datasets:
- `data_mmda_traffic_spatial.parquet`
- `AEGISDataset.parquet`

Ensure these files are available in the working directory.

### Features
1. **Data Loading and Preprocessing:**
   - Cleans and formats traffic and flood data.
   - Filters for valid geolocations.
   - Supports proximity analysis between flood points and traffic incidents.

2. **Interactive Dashboard:**
   - Filters for city, date range, traffic direction, and flood height.
   - Dynamic visualizations include:
     - **Map:** Displays traffic incidents and flood points.
     - **Bar Charts:**
       - Accidents by city and year.
       - Total incidents by city.
     - **Donut Chart:** Proportion of traffic incidents per city.
     - **Line Chart:** Monthly trends of traffic incidents.

3. **Advanced Insights:**
   - Spatial clustering using proximity analysis.
   - Advanced visualization capabilities for actionable insights.

### How to Run
1. Clone the repository and navigate to the project directory.
2. Ensure the required `.parquet` datasets are in the working directory.
3. Install dependencies by running:
   ```bash
   pip install dash plotly pandas geopy scipy dash-bootstrap-components
   ```
4. Run the notebook or execute the dashboard script by entering:
   ```bash
   python app.py
   ```
5. Open the dashboard in your browser (usually at `http://127.0.0.1:8050`).

### Notes
- The clustering functionality is implemented but currently commented out in the notebook. Uncomment and adjust parameters as needed to enable clustering.
- Ensure the dataset file paths are correctly specified.

### Limitations
- The notebook does not include automated profiling (e.g., `pandas_profiling`) as initially described.
- Predictive modeling and deeper segmentation analyses are not implemented but can be extended in future iterations.

### Credits
- Traffic incident data from the MMDA Traffic Incident dataset.
- Flood data from the AEGIS Dataset on Kaggle.

For any questions or collaboration opportunities, please contact Matthew Cuaresma at matthew_cuaresma@dlsu.edu.ph
