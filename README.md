# Machine Learning Burning Man Events Data

- The original notebooks on Burning Man Events EDA and Classification were performed with data from 2015-2017 collected by Justin Klein
- But this preprocessed dataset only contained data for the years 2015-2017
- Data for previous years, as far back as 2009, exists at playaevents.burningman.org, but is not accessible through the Burning Man API
- So, I scraped and cleaned this older dataset with the BeautifulSoup python package
- On this larger dataset I extracted new statistical insights, particularly about long-term trends and certain data quality issues
- And I trained various event-type classifiers, comparing simple rule-based systems against complex feature engineering and NLP systems
- I found that machine learning can provide a substantial increase in performance (as measured by both the F1 score and ROC-AUC)

In terms of actionable insights, I found:

- That there is strong evidence that, contrary to the raw data, events cannot be classified into exclusive types, and that users should be given the option to choose multiple event types
- That there are numerous events with negative event lengths, arising from inconsistencies in how users specify all-day-long events and the inability for users to clearly specify an event that starts on one day, and ends on another
- That there are large inconsistencies between how different members of the same camp enter their camp name, which cannot be reliably corrected with machine-learning-based approaches
- That how event locations are specified varies widely, and cannot be easily corrected with machine-learning
- And that there's still a lot of room for improvement on event classification accuracy
