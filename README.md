📊 **Disney+ Hotstar SQL Data Analysis**

📖 **Overview**

This project explores Disney+ Hotstar content data (movies, shows, genres, actors, countries) using SQL.
The goal is to uncover content trends, production insights, and viewing patterns.

📂**Project Structure**

Disney hotstar data.csv -> Dataset containing content metadata.

disney+hotstar analysis.pdf -> All SQL queries used in analysis.

🔍 **Key Insights**

🎬 Movies outnumber TV shows by 3:1.

🌍 India & US are top content producers.

🔞 Majority of titles fall under “U/A 13+” certification.

⏱️ Most movies have a runtime between 90–120 minutes.

⭐ Actor XYZ appeared in the highest number of shows.

🛠️ **Tech Stack**

SQL (Exploratory Analysis)

CSV Dataset (Disney+ Hotstar Data)

📸 **Sample Query**
-- Content Types on Disney+
select type, count(type) as content_type
from Disneyplushotstar..titles
where type is not null
group by type;

👨‍💻 **Author**

Anomitro Chatterjee
Data Analyst | SQL | Power BI | Excel
