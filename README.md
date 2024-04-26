### `PART 1`
### Using ScraperAPI to Fetch Twitter Data:
The provided Python code utilizes the ScraperAPI website to obtain Twitter data related to "Amazon products". Here's a breakdown of the code's functionality:

1. **Fetching Twitter Data**: The code makes an HTTP request to the ScraperAPI endpoint, passing parameters such as the API key, search query ("Amazon products"), date range, and number of tweets to retrieve.

2. **Processing the Data**: Upon receiving the data from the ScraperAPI, the code extracts the relevant tweets from the JSON response and appends them to a list named `twitter_data`.

3. **Creating a DataFrame**: The collected Twitter data is then converted into a pandas DataFrame (`df`) for further analysis and manipulation.

4. **Exporting Data to CSV**: The DataFrame `df` is exported to a CSV file named "tweetsAnalysis11.csv" using the `to_csv()` function for offline analysis or storage.

5. **Data Analysis**: After exporting the data, it is read back into another DataFrame (`df2`) from the CSV file. Unwanted columns such as "link", "displayed_link", and "highlighs" are dropped to streamline the data using the `drop()` function.

6. **Additional Data Export**: The modified DataFrame (`tf2`) is exported to another CSV file named "tweetsSentimentAnalysis11.csv" after dropping the unwanted columns.

7. **Printing Information**: The code prints the total length of the dataset (`len(tf2)`) and displays the first few rows of the DataFrame (`tf2.head()`).

### Conclusion of part 1:
In summary, this Python code demonstrates how to fetch Twitter data using the ScraperAPI website, process it into a structured format using pandas DataFrames, and export it to CSV files for further analysis. It provides a convenient way to gather and analyze Twitter data related to "Amazon products", which can be valuable for market research, sentiment analysis, or trend analysis purposes.


### `PART 2`
### Analyzing Twitter Sentiment with Transformer Models

The provided Python code leverages transformer-based models to perform sentiment analysis on Twitter data related to "Amazon products". Here's an overview of the code's functionality:

1. **Importing Libraries**: The code imports necessary libraries such as `transformers` for downloading the model, `pandas` for data manipulation, `re` for regular expressions, and `matplotlib` for visualization.

2. **Reading Data**: Twitter data is read from a CSV file ("tweetsSentimentAnalysis11.csv") into a pandas DataFrame (`tweets`).

3. **Data Cleaning**: A function `cleanTxt()` is defined to clean the tweet text by removing mentions, hyperlinks, hashtags, retweets, dates, and special characters.

4. **Model Loading**: The sentiment analysis model (`twitter-roberta-base-sentiment`) and tokenizer are loaded using the `AutoModelForSequenceClassification` and `AutoTokenizer` classes from the `transformers` library.

5. **Encoding Text**: Tweets are encoded using the tokenizer to convert them into numerical embeddings understandable by the model.

6. **Sentiment Prediction**: The model predicts sentiment scores (negative, neutral, positive) for each tweet using softmax to convert logits into probabilities.

7. **Data Processing**: The sentiment scores are stored in a dictionary and processed for the entire dataset using a loop.

8. **Visualization**: Word clouds are generated for positive, negative, and neutral sentiments to visualize the most frequent words in each category.

9. **Sentiment Distribution**: The percentages of positive, negative, and neutral tweets are calculated and displayed in a pie chart and bar graph.

### Conclusion of part 2:
Through transformer-based sentiment analysis, the code provides insights into the sentiment distribution of tweets related to Amazon products, facilitating deeper understanding and analysis of public perception on social media platforms.
