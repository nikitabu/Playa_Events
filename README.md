# Machine Learning Burning Man Events Data

- The original notebooks on Burning Man Events EDA and Classification used datasets collected via API by Justin Klein
- Unfortunately, Justin's preprocessed dataset only contained data for the years 2015-2017
- Data for previous years, as far back as 2009, exists online but isn't accessible through the official API
- My solution was to scraping and cleaning with the BeautifulSoup python package
- On this larger dataset I discovered new statistical insights regarding long-term trends and data quality problems
- I trained event-type classifiers, comparing simple rule-based systems against more complex features
- I found that machine learning provide a substantial performance increase (as measured by both F1 score and ROC-AUC)

In terms of actionable insights:

- There is strong evidence that, contrary to the raw data, events can't be classified into exclusive types, and that users should be given the option to choose multiple event types
- There are numerous events with negative event lengths, arising from inconsistencies in how users specify all-day-long events and the inability for users to clearly specify an event that starts on one day, and ends on another
- There are large inconsistencies between how camp name entries, that can't be reliably corrected with machine-learning-based approaches
- Event location conventions vary widely and can't be easily corrected
