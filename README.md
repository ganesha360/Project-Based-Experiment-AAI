<H3>ENTER YOUR NAME : GANESH R</H3>
<H3>ENTER YOUR REGISTER NO: 212222240029 </H3>
<H3>DATE:06.05.2024</H3>

<H1 Align="center">Project Based Experiment<H1>
  
### Objective:
Perform sentiment analysis using your Facebook data and count the number of Occurrences of iyyanar in the extracted text for the code given in the following link.
  
### Program:
```
import pandas as pd
from textblob import TextBlob

# Read data from Excel file
data = pd.read_csv("fb_sentiment.csv")  # Replace "facebook_data.xlsx" with your file path

# Given name to count occurrences
given_name = "Iyyanar"

# Initialize counters for sentiment analysis and name occurrences
sentiment_counts = {'positive': 0, 'negative': 0, 'neutral': 0}
name_occurrences = 0

# Perform sentiment analysis and count occurrences of the given name
for index, row in data.iterrows():
    # Perform sentiment analysis
    blob = TextBlob(row['FBPost'])
    polarity = blob.sentiment.polarity
    if polarity > 0:
        sentiment_counts['positive'] += 1
    elif polarity < 0:
        sentiment_counts['negative'] += 1
    else:
        sentiment_counts['neutral'] += 1

    # Count occurrences of the given name
    name_occurrences += row['FBPost'].lower().count(given_name.lower())

# Print sentiment analysis results
print("Sentiment Analysis Results:")


# Print occurrences of the given name
print(f"Occurrences of '{given_name}': {name_occurrences}")
```

### Output:
![image](https://github.com/Iyyanar22009120/Project-Based-Experiment-AAI/assets/118680259/7ca66941-77f1-413f-b2ac-b8f8cd858444)


### Inference:

Thus the sentiment analysis using your Facebook data  is performed and the number of Occurrences of Krishna in the extracted text for the code is counted.
