# Netflix Content Analysis Project

## Overview
This project performs comprehensive data analysis on Netflix's content library using the "Netflix Shows" dataset from Kaggle. It explores content distribution, regional production patterns, release trends, and genre popularity through data visualization and statistical analysis.

## Features
- **Content Distribution Analysis**: Examines the balance between Movies and TV Shows
- **Temporal Analysis**: Tracks content addition patterns over time
- **Geographic Analysis**: Identifies top content-producing countries
- **Genre Analysis**: Explores popular content categories and regional preferences
- **Rating Distribution**: Analyzes content rating patterns across different types
- **Release-to-Availability Gap**: Measures the time between content release and Netflix availability
- **A/B Testing**: Compares metrics between pre-2015 and post-2015 content

## Prerequisites
- Python 3.x
- pip package manager

## Installation

```bash
# Install the kagglehub library
pip install kagglehub

# Install additional dependencies
pip install pandas matplotlib seaborn scipy numpy sqlite3
```

## Data Source
The project uses the "Netflix Shows" dataset from Kaggle, which contains information about movies and TV shows available on Netflix. The dataset is loaded using the kagglehub library.

```python
import kagglehub
from kagglehub import KaggleDatasetAdapter

df = kagglehub.load_dataset(
    KaggleDatasetAdapter.PANDAS,
    "shivamb/netflix-shows",
    "netflix_titles.csv",
)
```

## Key Analyses

### 1. Basic Dataset Exploration
- Dataset dimensions and structure
- Column data types
- Missing value identification
- Summary statistics

### 2. Content Type Distribution
- Movies vs. TV Shows proportion analysis
- Visualization using countplots

### 3. Temporal Analysis
- Content addition trends by year
- Release year distribution
- Release-to-availability lag analysis

### 4. Geographic Analysis
- Top content-producing countries
- Country-specific visualizations
- SQL integration for geographic queries

### 5. Genre Analysis
- Top genres identification
- Genre distribution visualizations
- Country-specific genre preferences (e.g., United States)

### 6. Content Metrics
- Movie duration analysis
- TV show season count analysis
- Rating distribution by content type

### 7. Statistical Testing
- A/B testing between pre-2015 and post-2015 content
- Rating and engagement metrics comparison
- Statistical significance testing

## Visualizations
The project includes various data visualizations:
- Bar charts for categorical comparisons
- Histograms for distribution analysis
- Line charts for temporal trends
- Box plots for statistical comparisons

## Database Integration
The project demonstrates SQLite database integration for persistent data storage and SQL querying capabilities.

```python
import sqlite3

conn = sqlite3.connect('netflix.db')
df.to_sql('netflix', conn, if_exists='replace', index=False)

# Example SQL query
query = """
SELECT country, COUNT(*) as total
FROM netflix
WHERE country IS NOT NULL
GROUP BY country
ORDER BY total DESC
LIMIT 5;
"""

pd.read_sql_query(query, conn)
```

## A/B Testing Framework
The project implements an A/B testing framework to compare content performance metrics:
- Group A: Content released before 2015
- Group B: Content released in 2015 or later
- Metrics analyzed: User ratings and seasons watched
- Statistical significance testing using t-tests

## Results Highlights
- Content distribution shows a higher proportion of movies compared to TV shows
- United States is the leading content producer, followed by other major countries
- Genre preferences vary significantly by region
- Statistical comparison between older and newer content reveals significant differences in user engagement metrics

## Next Steps
- Implement sentiment analysis on content descriptions
- Explore recommendation algorithm based on content patterns
- Investigate correlation between content attributes and popularity
- Analyze seasonal patterns in content additions

## License
This project uses data from Kaggle that is subject to Kaggle's terms of use.

## Acknowledgments
- Kaggle and the dataset provider (shivamb)
- Netflix for the content data
