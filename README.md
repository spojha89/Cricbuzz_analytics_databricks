🏏 Cricbuzz Analytics on Databricks

Real-time cricket insights using Databricks, PySpark, and dashboards

This project extracts and analyzes live cricket data (latest matches, top scorers, and top bowlers) from Cricbuzz and visualizes it using Databricks dashboards.
It demonstrates an end-to-end data engineering and analytics workflow using Databricks notebooks and Delta Lake.

🚀 Features
✅ 1. Live Match Data Ingestion

Fetches latest matches from Cricbuzz (fixtures, ongoing, and completed).

Captures match metadata: teams, venue, match type, start time, result, etc.

✅ 2. Batting Analytics

Identifies top scorers across matches.

Extracts runs, balls faced, strike rate, 4s, 6s, and batting position.

Aggregates per match + cross-match leaderboard.

✅ 3. Bowling Analytics

Extracts top bowlers based on wickets, economy rate, overs, runs conceded.

Highlights best bowling performance per match.

Leaderboard for ongoing series.

✅ 4. Data Engineering in Databricks

End-to-end workflow using PySpark.

Raw → Bronze → Silver → Gold layers using Delta Lake.

Notebook-based pipelines for exploration, transformation, and analytics. This project does not include DLT implementation. 

✅ 5. Interactive Databricks Dashboards

Includes the following dashboards:

Latest Matches Dashboard → Match status, scores, key highlights

Top Scorers Dashboard → Player performance leaderboard

Top Bowlers Dashboard → Bowling performance summary

Dashboards refresh automatically based on notebook schedules.

🧱 Project Architecture
Cricbuzz Website → Databricks Notebook → Delta Lake → PySpark Transformations → Dashboards

Components:

Data Extraction: Python requests/BeautifulSoup/REST API scraping

Data Processing: PySpark transformations

Storage: Databricks File System (DBFS) or Delta tables

Visualization: Databricks SQL + Dashboard

📁 Repository Structure
/notebooks
    ├── Batsman_Bowlers_Scores.ipynb
    ├── Cricbuzz_Matches_Info.ipynb
    ├── Cricbuzz_Report.ipynb
    ├── Match_Details.ipynb


🔧 Technologies Used
Category	Technologies
Platform	Databricks
Languages	Python, PySpark
Storage	DBFS, Delta Lake
Visualization	Databricks Dashboards
API used- unofficial-cricbuzz.p.rapidapi.com
🏗️ How to Run
1. Import the notebooks into Databricks

Clone or upload /notebooks into your workspace.

2. Read API unofficial-cricbuzz.p.rapidapi.com

3. Run the extraction notebooks

These notebooks fetch raw data and write it to raw/bronze tables.

4. Run processing/transformation notebook

Creates silver/gold tables with structured bat/bowl stats.

5. Open Databricks SQL → Create dashboards

Use the prepared queries to generate visualizations.

📊 Sample Dashboards


<img width="833" height="511" alt="image" src="https://github.com/user-attachments/assets/c40e9673-d8c0-4906-a1ea-20be15959781" />

<img width="833" height="507" alt="image" src="https://github.com/user-attachments/assets/b6d0c6cd-bd95-4b77-8e6f-8aac6be47082" />



📌 Future Enhancements possible-

Add match prediction using MLflow

Add trending players analytics

Include ball-by-ball insights

Add REST API endpoints using Databricks Serverless
