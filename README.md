# IBM Data Science Capstone: SpaceX Falcon 9 Landing Prediction

This repository contains my capstone project for the IBM Data Science Professional Certificate (Coursera, completed March 2026). The project follows a complete data science workflow: collecting data, cleaning it, exploring it, visualising it, building an interactive dashboard and training machine learning models to predict whether a SpaceX Falcon 9 first stage will land successfully.

## Project Background

SpaceX advertises Falcon 9 launches at a much lower cost than its competitors, largely because the first stage can be reused after a successful landing. If we can predict whether the first stage will land, we can estimate the cost of a launch. That information is useful to any company bidding against SpaceX for a rocket launch.

**Goal:** Predict the outcome of a Falcon 9 first-stage landing from launch data such as payload mass, orbit, launch site and booster details.

## Project Workflow

The notebooks are designed to be run in this order:

| **Step** | **File** | **What it does** |
|:--------:|:--------:|:----------------:|
| 1 | [Data collection api](https://github.com/yolandawalingo/IBM_Data_Science_Final_Project/blob/main/jupyter-labs-spacex-data-collection-api%20(5).ipynb) | Collects launch data from the SpaceX API |
| 2 | [jupytper labs webscraping](https://github.com/yolandawalingo/IBM_Data_Science_Final_Project/blob/main/jupyter-labs-webscraping%20(2).ipynb) | Collects additional launch records by web scraping |
| 3 | [Data wrangling](https://github.com/yolandawalingo/IBM_Data_Science_Final_Project/blob/main/labs-jupyter-spacex-Data%20wrangling%20(2).ipynb) |Cleans the data, handles missing values and creates the landing outcome label |
| 4 | [jupyter-labs-eda-sql-coursera_sqlite (1).ipynb](https://github.com/yolandawalingo/IBM_Data_Science_Final_Project/blob/main/jupyter-labs-eda-sql-coursera_sqllite%20(1).ipynb) | Exploratory data analysis using SQL queries (SQLite) |
| 5 | [edadataviz (2).ipynb](https://github.com/yolandawalingo/IBM_Data_Science_Final_Project/blob/main/edadataviz%20(2).ipynb) | Exploratory data analysis and visualisations of the relationships between variables and landing success |
| 6 | [lab_jupyter_launch_site_location(5).ipynb](https://github.com/yolandawalingo/IBM_Data_Science_Final_Project/blob/main/lab_jupyter_launch_site_location%20(5).ipynb) | Interactive map of launch sites and their surroundings |
| 7 | [spacex-dash-app (1).py](https://github.com/yolandawalingo/IBM_Data_Science_Final_Project/blob/main/spacex-dash-app%20(1).py) | Interative dashboard of launch results |
| 8 | [SpaceX_Machine Learning Prediction_Part_5 (4).ipynb](https://github.com/yolandawalingo/IBM_Data_Science_Final_Project/blob/main/SpaceX_Machine%20Learning%20Prediction_Part_5%20(4).ipynb) | Trains and compares classification models to predict landing success |

## Tools and Technologies

- **Language:** Python
- **Data Handling:** Pandas, Numpy
- **Data Collection:** SpaceX REST API, web scraping
- **Database:** SQL(SQLite)
- **Visualisation:** Matplotlib, Seaborn, Folium (interactive maps), Plotly Dash (dashboard)
- **Machine Learning:** Scikit-learn
- **Environment:** Jupyter Notebook

## Key Findings

- **Launch success over time:** Landing success improved sharply from 2013 onwards. Early launches (2010-2013) had a 0% landing success rate, and by 2018-2020 the success rate had levelled off at a very high level.
- **Launch sites:** KSCLC-39A had the highest concentration of successful landings. CCAFS SLC-40 was the busiest site and shows a mix of early failures and later successes.
- **Payload and orbit:** Payload mass and target orbit both influence landing outcomes. Lighter payloads generally had higher success rates, and heavier payloads were highly successful in Very Low Earth Orbit(VLEO), which needs less fuel and leaves more for the booster's return.
- **Model performance:** Logistic Regression, SVM, Decision Tree and KNN were all tuned with GridSearchCV. The best models reached a test accuracy of about **83.3%** with Logistic Regression, SVM and KNN outperforming the Decision Tree. I used KNN for the confusion matrix.
- **Errors:** The main error type was false positives (predicting a successful landing that actually failed), which matters in practice because overestimating success can mean losing expensive hardware.
- **Limitations:** This is a relatively small dataset, so the test accuracy is only a rough estimate.
  
## Interactive Dashboard

The [dashboard](https://github.com/yolandawalingo/IBM_Data_Science_Final_Project/blob/main/spacex-dash-app%20(1).py) lets you explore launch results interactively. To run it locally:

```
pip install pandas plotly dash
python "spacex-dash-app (1).py"
```
Then open the local address shown in the terminal in your browser.

## How to Run the Notebooks

1. Clone the repository:
```
git clone https://github.com/yolandawalingo/IBM_Data_Science_Final_Project.git
cd IBM_Data_Science_Final_Project
```
2. Install the main libraries
```
pip install pandas numpy matplotlib seaborn scikit-learn folium jupyter
```
3. Start Jupyter and open the notebooks in the order shown above:
```
jupyter notebook
```

## What I learned

- Collecting data from APIs and by web scraping
- Cleaning and preparing messy real-world data
- Writing SQL queries to explore a dataset
- Creating visualisations and an interactive dashboard to communicate findings
- Building, tuning and comparing classification models with Scikit-learn

## Author
**Yolanda Walingo** Computer Science and Statistics graduate, University of KwaZulu-Natal [GitHub](https://github.com/yolandawalingo) | [LinkedIn](linkedin.com/in/yolanda-walingo-0190442a6)
