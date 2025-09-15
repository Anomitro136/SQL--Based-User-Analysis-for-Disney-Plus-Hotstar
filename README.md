# SQL--Based-User-Analysis-for-Disney-Plus-Hotstar
📊 Disney+ Hotstar SQL Data Analysis

This project explores Disney+ Hotstar content data (movies, shows, genres, actors, production countries, etc.) using SQL queries.
The dataset (Disney hotstar data.csv) contains details such as titles, credits, genres, runtime, release year, and more.

📁 Project Structure

Disney hotstar data.csv → Dataset containing Disney+ Hotstar titles and credits
queries.sql → SQL queries used for analysis

🔍 SQL Analysis Queries

1️⃣ --- Content Types on Disney+ ---
select type, count(type) as content_type 
from Disneyplushotstar..titles
where type is not null
group by type;

1B️) Content Types in Recent Years (2015 onwards)

select release_year, type, count(type) as content_type 
from Disneyplushotstar..titles
group by release_year, type
having release_year >= 2015
order by content_type desc;

2️⃣ --- Age Certifications ---

select age_certification, type, count(type) as content_type 
from Disneyplushotstar..titles
group by age_certification, type
order by content_type asc;

3️⃣ --- Top 10 Production Countries ---

select top 10 production_countries, count(production_countries) as disney_production_house
from Disneyplushotstar..titles
group by production_countries
order by disney_production_house desc;

4️⃣ --- Content Duration by Type ---

Movies:

select runtime, count(runtime) as no_of_movies 
from Disneyplushotstar..titles
group by runtime
order by no_of_movies desc;


Shows:

select seasons, count(seasons) as no_of_series 
from Disneyplushotstar..titles
group by seasons
order by no_of_series;

5️⃣ --- Top Movies & TV Show Genres ---

select genre1 as genre, count(genre1) as no_of_genres 
from Disneyplushotstar..titles
group by genre1
order by no_of_genres desc;

6️⃣--- Top 8 Common Actors in Disney+ Content ---

select top 8 a.name, a.role, b.id 
from Disneyplushotstar..credits a
inner join Disneyplushotstar..titles b 
on a.id = b.id;

🛠️ Tech Stack

SQL (Data Analysis)
CSV Dataset (Disney+ Hotstar data)

👨‍💻 Author

Anomitro Chatterjee
Data Analyst | SQL | Power BI | Excel
