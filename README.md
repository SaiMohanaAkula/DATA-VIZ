# DATA-VIZ
Data Visualization Project

PROJECT PROPOSAL

Project Overview

This project aims to build an interactive IMDb dashboard tailored to fans of specific actors, providing detailed insights into their favorite actor’s career. By selecting an actor, users can explore key information such as top-rated movies, popular characters, genre trends, and rating patterns over time. This intuitive, data-driven experience will empower users to delve into the actor's work and audience reception.

Project Goals

The primary goals of this project are to:

● Enable fans to explore a summary of their favorite actor's career highlights and audience reception.

● Visualize the actor’s top movies, average rating trends, most popular characters, and genre analysis.

● Provide an easy-to-navigate dashboard with filters for actor selection, allowing customization and detailed exploration.


Target User Group

● Primary User: Fans of specific actors who wish to explore the career highlights, most popular roles, and overall audience reception of their favorite actors.

● Secondary Users: Movie enthusiasts and researchers interested in actor-specific insights, genre trends, and audience engagement over time.


User Stories & Needs

● Fan’s Need: "As a fan, I want to explore the top movies and popular characters of my favorite actor, so I can learn more about their most celebrated work."

● Enthusiast’s Need: "As a movie enthusiast, I want to see the ratings of my favorite actor’s movies across different genres and trends over time to understand their career impact."

● Researcher’s Need: "As a researcher, I want to analyze how an actor's movies are rated over time and by genre to observe any trends in their popularity."


Data and Key Columns

Relevant data columns to meet user needs include:

● Actor Details: nconst, primaryName, primaryProfession, knownForTitles (from name.basics.tsv)

● Movie Details: tconst, primaryTitle, startYear, genres, runtimeMinutes, averageRating (from title.basics.tsv and title.ratings.tsv)

● Actor Roles: characters, category (from title.principals.tsv)

● Rating and Popularity Metrics: averageRating, numVotes (from title.ratings.tsv)


Dashboard Components and Design

● Actor Selection: A drop-down menu enabling users to select their favorite actor by name.

● Actor Summary & Leaderboard:

  ○ Top 5 Movies of All Time: A leaderboard table displaying the top 5 highest-rated movies of the actor, including IMDb ratings.
  
  ○ Actor Metrics: Display panels to show:
  
    ■ Average Rating of All Movies: The overall average rating across the actor’s movies.
    
    ■ Most Popular Character: The character that received the highest audience rating, along with the associated movie title.
    
● Genre vs. Ratings Analysis:

  ○ Box Plot Visualization: Genre on the x-axis and IMDb ratings on the y-axis, providing insights into the actor’s performance 
    across various genres.
    
● Popularity and Trend Analysis:

  ○ Weighted Rating Calculation: A new calculated field for weighted ratings based on IMDb ratings and vote count.
  
  ○ Trend Line Plot: A line chart with time (year) on the x-axis and weighted ratings on the y-axis, visualizing popularity trends 
    over the actor’s career.
    

Data Cleaning and Preparation

● Data Cleaning:

  ○ Remove entries with missing or incomplete data in relevant columns (averageRating, primaryTitle, characters).
  
  ○ Standardize genres and category fields to avoid inconsistencies.
  
  ○ Filter for relevant entries (e.g., “actor” in category) and remove any duplicates.
  
● Outlier Detection:

  ○ Address potential outliers in IMDb ratings and vote counts that could skew the weighted rating calculation.
  
  ○ Perform quality checks on character names and genre consistency.
  

Technical Implementation

● Data Processing:

  ○ Use Python (Pandas) for data cleaning, merging datasets on tconst and nconst to integrate actor, movie, and rating information.
  
  ○ Calculate weighted ratings using the formula Weighted rating: The weighted rating balances a movie’s IMDb rating with its vote 
    count, favoring movies with both high ratings and substantial votes for a more reliable measure of popularity and quality.

● Dashboard Tool: Tableau for interactive visualization, enabling real-time filtering and exploration by actor.


Expected Outcome

This dashboard will provide fans and enthusiasts with a comprehensive, actor-centric experience, allowing them to gain insights into their favorite actor’s top movies, character roles, genre strengths, and career trajectory. The tool will be a valuable resource for understanding an actor’s impact and audience reception over time. A visual of the platform is as given below:

![IMG_1631](https://github.com/user-attachments/assets/c92c1797-d7d9-4ad7-aa88-99b378552492)


