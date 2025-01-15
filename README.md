### **Exercise: Sentiment Analysis and Key Insights Extraction from Ford Car Reviews**

### **Problem Statement:**
You have been provided with a dataset containing Ford car reviews. Your task is to use LangChain and the concepts you’ve learned to perform the following tasks:

1. **Sentiment Analysis**: Analyze the sentiment of each review, categorize it as positive, neutral, or negative, and store the result.
2. **Key Insights Extraction**: Extract key pieces of information from each review, such as the pros and cons mentioned, and the specific features the reviewer liked or disliked (e.g., vehicle performance, comfort, price).

You will build a LangChain-based solution that leverages language models to automatically extract this information and provide a structured summary of the reviews. 

---
### **Steps to Solve:**

#### **Step 1: Load the Dataset**
- The dataset file is named `ford_car_reviews.csv` and is sourced from Kaggle: [Edmunds Consumer Car Ratings and Reviews](https://www.kaggle.com/datasets/ankkur13/edmundsconsumer-car-ratings-and-reviews).
- For this exercise, **limit the data to the first 25 records**. This can be achieved by using `df.head(25)` or `df.iloc[:25]` when loading the data into a DataFrame.

#### **Step 2: Define the Sentiment Analysis Task**
- Use LangChain to create a pipeline to classify the sentiment of each review.
- Define prompts that can guide the model to evaluate the sentiment. For example:
  - "Given the following car review, classify the sentiment as positive, neutral, or negative."

#### **Step 3: Key Insights Extraction**
- Use LangChain to create a pipeline to extract pros, cons, and notable features from each review. Define prompts such as:
  - "What are the pros and cons of the vehicle described in the following review?"
  - "What specific features of the vehicle does the reviewer like or dislike?"

#### **Step 4: Update the DataFrame with New Information**
- Run the pipeline for each review and collect the sentiment and insights.
- Once the analysis and extraction are complete, update the original DataFrame with additional columns to include:
  - Sentiment (positive, neutral, negative)
  - Pros
  - Cons
  - Liked_Features
  - Disliked_Features

---

### **Example Output:**

```json
{
  "Review_Date": "03/07/13",
  "Vehicle_Title": "2006 Ford Mustang Coupe",
  "Review_Text": "With the expected arrival of our 6th child...",
  "Rating": 4.125,
  "Sentiment": "Positive",
  "Pros": "Good driving experience, Large seating capacity, Great options",
  "Cons": "None mentioned",
  "Liked_Features": ["Driving experience", "Seating capacity", "Options available"],
  "Disliked_Features": []
}
```
