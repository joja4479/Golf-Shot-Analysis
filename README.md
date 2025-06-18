# Golf Shot Analysis

This project analyzes personal golf shot data collected using the Rapsodo MLM2Pro mobile launch monitor and the Awesome Golf iPad app. The purpose is to identify areas of improvement in the user's golf performance and verify club-specific carry distances to ensure consistent gapping.

## 📌 Project Goals

Determine which aspects of the user's golf game need the most improvement.

Analyze average carry distances by club.

Compare personal performance metrics to professional benchmarks.

Ensure consistent gapping between clubs (ideally ~10 yards apart).

## 📊 Data Collection

Data is captured using Rapsodo MLM2Pro with radar and high-speed camera measurements.

The Awesome Golf app processes shot data and exports .csv files after each training session.

Data includes: swing speed, ball speed, launch angle, spin rate, spin axis, carry distance, shot shape, etc.

## 🧰 Technologies Used

Python

pandas, numpy — for data wrangling

matplotlib, mplcursors — for visualization

statsmodels, scikit-learn — for statistical modeling and regression

BeautifulSoup, requests — for optional web scraping (e.g., pro comparison data)

glob, os — for batch file loading

## 🗂️ Project Structure

golf_shot_analysis.ipynb — main notebook for data loading, analysis, and visualization

/shot_csvs/ — directory where your session .csv files should be stored

golf_sim.PNG — sample visual of the simulator view used during training

## 🧪 How It Works

All .csv files in the specified directory are read into a single DataFrame.

Exploratory Data Analysis (EDA) is conducted to observe trends, outliers, and performance metrics.

Visualizations are created to assess:

- Shot dispersion
- Club averages
- Spin vs distance
- Launch conditions
- Linear and statistical models may be used to forecast or compare metrics to professional standards.

## 🧼 Data Cleaning Notes
- The project handles inconsistent column names, missing values, and filters unrealistic measurements (e.g., misreads).
- Only valid, confirmed shots are kept for analysis.

## 📁 Usage

To run the notebook:

- Set up your Python environment (e.g., with virtualenv or conda)
- pip install pandas matplotlib numpy mplcursors scikit-learn statsmodels beautifulsoup4 requests

Then open the notebook:

- jupyter notebook golf_shot_analysis.ipynb

Make sure your CSV files are placed inside the shot_csvs/ directory.
