

## Intro: 

In this project, I extract movie data from SensCritique, refining it for analytical clarity, and employing machine learning algorithms like Random Forest and XGBoost to predict film ratings.

This project contains three main components:
1. **Web Scraping**: Extraction of data from web pages, including titles, directors, ratings, publication years, etc.
2. **Data Cleaning**: Enhancement of data quality and structure, as well as preparation of categorical data for machine learning applications.
3. **Prediction Model**: Implementation of Random Forest and XGBoost algorithms to predict movie ratings, with Grid Search employed to optimize model parameters.

Additionally, I have created [a basic tutorial](https://www.notion.so/fengyu23/SensCritique-Project-Basic-Tutorial-756d6801d0664c7eb71e95ab383848a7#d9ddea4ecb5249b5a413f5867d78f713) aimed at assisting classmates with understanding and completing the assignment. This tutorial is designed to guide without providing direct code solutions.

## Key Takeaways:

1. Reviewing online projects related to this subject matter is beneficial. They help me to gain insights into selecting relevant features, appropriate prediction models, and effective data cleaning methods.
2. For specific technical issues, resources like Stack Overflow can be invaluable. During a particular challenge with debugging the web driver, despite browsing official documentation and seeking assistance from ChatGPT, the solution ultimately pertained to network connectivity rather than the code itself.
3. Coding Insights:
   1. To handle different data types with a single function, consider using `isinstance` or using a parameter like `is_url=True` to adapt the function's processing logic.
   2. In web scraping, it's crucial to account for potential `None` values. This can be managed gracefully in the return statement, for example: `return found_element.text if found_element else None`.
   3. The `soup.find` method is versatile and can be applied to a range of scenarios, including searching by attributes, text content, or using regular expressions.
   4. When manipulating dataframes:
      1. To extract the initial segment of a split string, use `.str.split('.').str.get(0)`.
      2. Exercise caution with numerical values when using `groupby`.
      3. The label dataframe should always match the feature dataframe in length, indicating that simply dropping missing values (`dropna`) may not always be appropriate.


## Reference Materials:
1. [Udacity Data Analyst Nanodegree Flight Delay Forecast Project](https://github.com/fengyu20/udacity_data_analyst_nanodegree_projects/blob/master/CN_flight_delay_forecast_master/FlightDelayForecast.ipynb): A past project that provided insights on data cleaning and machine learning techniques.
2. [Movie Popularity Prediction Full Project on Kaggle](https://www.kaggle.com/code/huntermitchell/movie-popularity-prediction-full-project/notebook): This resource informed my feature selection and helped structure the code effectively.
3. Online materials: As I was navigating unfamiliar subject with Beautifulsoup and Selenium, I used ChatGPT, official documentation, and Stackoverflow to complete the web driver segment.