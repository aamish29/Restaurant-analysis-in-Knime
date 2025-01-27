# Restaurant-analysis-in-Knime
Restaurant market analysis using Knime based on yelp dataset

This project explores the factors contributing to high restaurant ratings and provides insights for restaurant owners to improve their reviews. By analyzing restaurant data, this project identifies trends, patterns, and actionable recommendations to enhance customer satisfaction.

## Project Overview

The project uses restaurant data stored in MongoDB (originally the Yelp dataset of user reviews and restaurant ratings) to extract insights about:

- **Most reviewed categories and cities**
- **Factors influencing high or low ratings**
- **Relationship between review counts and star ratings**
- **Top-rated and highly reviewed restaurants**

## Workflow

The workflow consists of the following steps:

### 1. Data Extraction and Filtering

- **MongoDB Connector & Reader**: Connects to the MongoDB database and reads restaurant data.
- **Row Filter**: Filters restaurants with at least 50 reviews to ensure statistical significance.
- **Column Filter**: Focuses on key columns like Restaurant Name, Review Count, Stars, and Category.

### 2. Analysis and Insights Generation

- **Analysis 1: Most Reviewed Categories**
  - Group data by category and sort by descending review count.
  - Visualize the top categories with the highest number of reviews (Bar Chart).
  
- **Analysis 2: Low-Rated Restaurants by City**
  - Filter restaurants with ratings < 2.5 stars.
  - Group data to identify cities with the most low-rated restaurants.
  - Visualize cities with the lowest-rated restaurants (Pie Chart).
  
- **Analysis 3: Relationship Between Reviews and Ratings**
  - Analyze the correlation between the number of reviews and star ratings (Scatter Plot).
  
- **Analysis 4: Disparity in Reviews by City**
  - Group data and visualize review disparities across cities (Bar Chart).
  
- **Analysis 5: Top Restaurants Analysis**
  - Filter for top-rated restaurants (ratings > 4.6 stars).
  - Identify the top 10 highly rated restaurants.
  - Visualize cities hosting top-rated restaurants (Pie Chart).

### 3. Visualization

All insights are visualized using various types of charts to convey actionable findings clearly, including:
- **Bar charts**
- **Scatter plots**
- **Pie charts**

## Key Insights

- **Most Reviewed Categories**:  
  Top categories include **Bars**, **Wine**, **Nightlife**, and **Spanish/Mexican** restaurants.
  
- **Low-Rated Restaurants**:  
  Cities like **Boston** dominate the low-rating category with many poorly-rated establishments.
  
- **Review and Rating Correlation**:  
  Restaurants with a large number of reviews tend to have a broader range of ratings (both high and low).
  
- **Review Disparity**:  
  **Boston** leads with the highest disparity in review counts—some restaurants have a huge volume of reviews while others have far fewer.
  
- **Top Restaurants**:  
  **Orlando** stands out with a significant number of top-rated restaurants (ratings > 4.6).

## Technologies Used

- **MongoDB**: For data storage and extraction.
- **Python**: Used for data processing, including filtering, grouping, and analysis.
- **Visualization Libraries**: Matplotlib, Seaborn, and Plotly for visualizing insights.

## How to Use

1. Clone the repository.
2. Set up MongoDB and import the dataset.
3. Run the analysis workflow using knime.
4. View generated visualizations for insights.
