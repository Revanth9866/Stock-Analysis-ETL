# 📈 Stock Analysis --ETL--

I built this project because I wanted to see if I could take messy, real-world financial data and turn it into a system that actually tells a story. It’s one thing to look at a stock price on a website, but it’s another to build a full pipeline that cleans, stores, and analyzes that data from scratch.

This project is a complete end-to-end workflow using **Python, MySQL, and Git** to handle everything from the first "dirty" CSV to the final visual report.



---

###  The Problem I Solved
Raw data is almost always a mess. When I started with the daily files for AAPL, GOOG, and MSFT, I ran into duplicates, missing values, and even logical errors where high prices were lower than low prices. 

Using **Pandas and NumPy**, I built a cleaning pipeline that:
* **Fixed the gaps:** I used median imputation for prices and zero-filling for volume so the analysis wouldn't break.
* **Enforced Logic:** I created validation rules to ensure every "High" and "Low" price made sense.
* **Added Context:** I calculated daily returns and tagged every single day as an **UP, DOWN, or NO_CHANGE** day to make trend tracking instant.

---

###  Deep Diving with SQL
Once the data was "Gold Standard" quality, I moved it into a **MySQL database**. This is where I performed the heavy lifting using SQL aggregations and window functions. My goal was to move past simple totals and look at the actual behavior of the market.



---

###  Business Goals & Insights
By the end of the project, I successfully hit these specific analytical goals:

* **Performance Tracking:** Identified which stock actually had the best average daily returns.
* **Risk Evaluation:** Measured volatility levels to see which companies were the "riskiest" for investors.
* **Trend Smoothing:** Calculated 7-day and 30-day moving averages to filter out the daily "noise."
* **Anomaly Detection:** Spotted abnormal spikes in trading volume that usually signal a major news event.
* **Correlation:** Analyzed how volume changes actually impact price movement.
* **Data Integrity:** Implemented strict business validation rules so the database never accepts "bad" data.

---

###  The Tech Stack
* **Python:** The "Engine" (Pandas, NumPy, Matplotlib)
* **MySQL:** The "Brain" (Complex joins, Aggregations, Window Functions)
* **Git:** The "Safety Net" (Version control and project organization)



---

###  How to Explore
If you want to see the results, head over to the **reports/** folder to see the visualizations, or check out **notebooks/** to see the logic I used to clean the data. 

To run it yourself:
1. Clone the repo.
2. Run `pip install -r requirements.txt`.
3. Use the scripts in the notebooks to generate your own "Good data" file!
