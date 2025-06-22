# Background
School group project for "SkyWings Airline" to develop sentiment analysis and present solutions for data driven decision making. 

### Questions we wanted to answer were:
1. What was not working well for the airline? 
2. How was the sales pattern over the past 2 years? 
3. What aspect of the airline could be improve?

### Tools that were used
- KNIME: Low code data management system to perform data cleaning and transformation.
- Tableau: Data visualisation to create dashboard and storytelling. 

# Data Cleaning & Transformation
1. Start with "Excel Reader" node to import the data (you may use "CSV Reader" if your file is a CSV) and convert the strings to document with "Strings to Document" node. 
2. Remove duplicates, puctuation, numbers, stop words.
3. Convert to lower case and words to root with the "Case Converter" and "Kuhlen Stemmer" nodes. 
4. Using "Dictionary Tagger" node, perform tagging with [MPQA Opinion Corpus](https://mpqa.cs.pitt.edu/corpora/mpqa_corpus/) and "Document Viewer" to ensure that you are able to see sentiment tags.
5. Add "Bag of Words Creator" node to extract all the words and "TF" node to count the frequency of each word. 
6. With the "Tags to Strings" node, extract the sentiment associate to each word and remove missing values with "Row Filter". Remove sentiment tags using "Term to Strings" node and group by the column "TF abs", aggregating with sum. 
7. Add row filter nodes for positive and negative sentiments. Export using "Excel Writer" node.
8. Add the "Tag Cloud (Javascript)" node to create the word cloud.

# Dashboarding & Storytelling
1. With the exported XLSX file from KNIME, import the dataset into Tableau. Import the relevant transactions. 
2. Create a dashboard by putting together multiple charts that are related. Make sure it is well-structured with user interactivity, and appropriate colours to allow for easy interpretation. 
3. Lastly, propose solutions to address identified issues with visuals to support recommendations. 

# Insights
### Sentiment Analysis
- Negative sentiments for the period were constantly more than positive sentiments. 
- Top 3 positive sentiments of **"friend", "comfortable", and "nice"** are due to the airline's staff.
- Top 3 negative sentiments of **"try, "bad", and "worse"** are results of service inefficiencies and communication despite the fact that employees were friendly. 

### Trends
- Bookings per month were **decreasing from January 2024**.
- Returning customers are **84%** of the airline's customers with low recency and high frequency. 
- Total price paid regardless of using promo codes were similar, suggesting ineffient use of promotions. 
- Returning customers are **not aware or do not use** promo codes despite high frequency. 

### Recommendations
- SOP reviews, customer feedback reviews, and refresher training to improve customer satisfaction and brand image.
- Make use of historical booking data to implement promotional code during non-peak seasons with meaningful discounts and marketing campaigns. 

# Closing Thoughts
Throughout this module and project, I manage to gain some experience in using data to drive decision making. Being a strong believer of data, this project allows me to gain better understanding of how data should be presented. 
