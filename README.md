## Wrangle and Analyze Data from Twitter

## Business Problem

Social media platforms like Twitter generate vast amounts of unstructured data daily, offering rich insights into public sentiment, trends, and user behavior. However, this data is often messy, inconsistent, and spread across various formats, making it challenging to extract meaningful information. Businesses and researchers face the critical task of transforming this raw, real-world data into a clean, structured, and analyzable format to support data-driven decision-making and gain a competitive edge.

## Solution Overview

This project implements a comprehensive data wrangling and analysis pipeline to process real-world data from Twitter, specifically focusing on the @dog_rates (WeRateDogs) archive. The solution involves gathering data from multiple sources (including programmatic downloads and API calls), rigorously assessing its quality and tidiness, and then performing extensive cleaning. The cleaned data is subsequently analyzed and visualized to uncover interesting patterns and insights related to dog ratings, popular breeds, and tweet characteristics. This project demonstrates robust skills in data acquisition, cleaning, and exploratory data analysis.

## Solution Architecture

The data wrangling and analysis architecture follows a typical Extract, Assess, Clean, Analyze, and Visualize (EACAV) workflow. Data is extracted from various sources, including a provided Twitter archive and external APIs. It is then systematically assessed for quality and tidiness issues. A cleaning phase addresses identified problems, leading to a refined dataset. Finally, the cleaned data is used for exploratory analysis and visualization to derive insights.

![Data Wrangling Workflow](https://github.com/ShireenTalaat/Wrangle-and-Analyze-Data-Twitter/blob/1dafb82016e2d4b4d614a55797783a2fe6289a5f/Twitter.jpg)

## Technologies Used

-   **Programming Language:** Python
-   **Libraries:**
    -   **Data Manipulation:** Pandas, NumPy
    -   **Data Acquisition:** Requests, Tweepy (or similar for Twitter API interaction)
    -   **Data Visualization:** Matplotlib, Seaborn
-   **Tools:** Jupyter Notebook (for iterative development and documentation)

## Data Pipeline / Workflow

1.  **Data Gathering:**
    -   **Tweet Archive:** Download a provided CSV file containing basic tweet data (tweet ID, timestamp, text) for over 5000 tweets.
    -   **Image Predictions:** Programmatically download a TSV file containing image predictions (dog breeds, confidence levels) from a URL.
    -   **Twitter API:** Use the Twitter API to query additional data (e.g., retweet count, favorite count) for each tweet ID, storing it in a JSON file.
2.  **Data Assessment:** Systematically identify data quality issues (e.g., missing values, incorrect data types, inconsistent entries, outliers) and tidiness issues (e.g., variables stored as values, multiple variables in one column, multiple types of observational units in one table).
3.  **Data Cleaning:** Implement a series of cleaning steps to address all identified issues. This includes:
    -   Handling missing data appropriately.
    -   Correcting data types.
    -   Extracting relevant information from text (e.g., dog names, dog stages, numerical ratings).
    -   Merging datasets based on common identifiers.
    -   Removing irrelevant or duplicate entries.
4.  **Data Storage:** Store the cleaned, master dataset in a persistent format (e.g., CSV or SQLite database) for future analysis.
5.  **Data Analysis & Visualization:** Perform exploratory data analysis to uncover trends and patterns. Create visualizations (e.g., histograms, bar charts, scatter plots) to communicate key findings, such as:
    -   Distribution of dog ratings.
    -   Most popular dog breeds.
    -   Correlation between rating and engagement (retweets, favorites).
    -   Impact of dog stage (pupper, doggo, floofer, puppo) on ratings.

## Dataset

The primary dataset is the tweet archive of the Twitter user @dog_rates (WeRateDogs), which includes over 5000 tweets up to August 2017. This is supplemented by image prediction data (dog breeds) and additional tweet metrics obtained via the Twitter API. The combined dataset provides a rich source for analyzing dog ratings and associated tweet characteristics.

## Key Features

-   **Multi-Source Data Acquisition:** Demonstrates proficiency in gathering data from diverse sources, including files and APIs.
-   **Robust Data Quality Assessment:** Systematic identification of data quality and tidiness issues.
-   **Comprehensive Data Cleaning:** Implementation of advanced data cleaning techniques to prepare real-world data for analysis.
-   **Exploratory Data Analysis:** Uncovering meaningful insights and patterns from complex datasets.
-   **Effective Data Visualization:** Communicating findings through clear and informative visual representations.

## Results & Insights

This project successfully transformed raw, messy Twitter data into a clean, analyzable dataset, revealing several key insights. The analysis showed that @dog_rates frequently assigns ratings above 10/10, indicating a humorous and positive approach. Certain dog breeds appeared more frequently and received higher average ratings. Furthermore, a positive correlation was observed between higher ratings and increased tweet engagement (retweets and likes), suggesting that well-rated dogs resonate more with the audience. The project highlighted the importance of thorough data wrangling in extracting valuable insights from unstructured social media data.

## Engineering Decisions

-   **Python for End-to-End Workflow:** Python was chosen as the primary language due to its extensive ecosystem of libraries (Pandas for data manipulation, Requests/Tweepy for API interaction, Matplotlib/Seaborn for visualization), making it ideal for an end-to-end data wrangling and analysis pipeline.
-   **Iterative Assessment and Cleaning:** An iterative approach to data assessment and cleaning was adopted, documenting each step in a Jupyter Notebook. This ensures transparency, reproducibility, and allows for systematic refinement of the data.
-   **Modular Data Acquisition:** Data was acquired from different sources in a modular fashion, demonstrating adaptability to various data formats and access methods.

## Future Improvements

Future enhancements could include integrating this pipeline with a real-time streaming solution (e.g., Apache Kafka) to continuously ingest and analyze live Twitter data. Implementing natural language processing (NLP) techniques to analyze the sentiment of tweet comments or extract more nuanced information about dog characteristics would add further value. Deploying the analysis as an interactive web application (e.g., using Flask or Streamlit) would allow broader access to the insights generated.
