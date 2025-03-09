# Starbucks Capstone Challenge: Brewing Insights from Customer Data ☕📊

Welcome to the **Starbucks Capstone Challenge**! This project dives into Starbucks' customer and offer data to uncover insights that can help improve their marketing strategies. Whether you're a data science enthusiast, a coffee lover, or just someone who enjoys a good analysis, this project has something for you. Let's get brewing!

---

## **Motivation**
Starbucks wants to understand how customers interact with their offers. Are some offers more effective than others? Do certain groups of customers respond better to specific types of offers? By analyzing customer demographics, offer details, and transaction data, we aim to uncover patterns that can help Starbucks tailor their offers to the right customers and improve their marketing strategies.

---

## **Libraries Used**
Here are the key Python libraries used in this project:
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical computations.
- **Matplotlib** and **Seaborn**: For data visualization.
- **Scikit-learn**: For machine learning (RandomForestRegressor, RandomForestClassifier, and hyperparameter tuning with RandomizedSearchCV).
- **JSON**: For reading and processing JSON files.

To install these libraries, run:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```
## Files in the Repository

Here’s what you’ll find in this project:

- **Starbucks_Capstone.ipynb:** The main Jupyter notebook containing the entire analysis, from data cleaning to visualization and insights.
- **portfolio.json:** Contains details about Starbucks' offers, such as offer type, difficulty, reward, and duration.
- **profile.json:** Contains demographic data about Starbucks customers, including age, gender, income, and membership start date.
- **transcript.zip:** Zipped json file, needs to be extracted to obtain transcript.json. Records customer interactions, such as offers received, viewed, completed, and transactions.
- **README.md:** This file! It provides an overview of the project, the libraries used, the files in the repository, and a summary of the results.

 ## Project Workflow
 
**1. Data Loading:**
- Load portfolio.json, profile.json, and transcript.json into Pandas DataFrames.

**2. Data Cleaning:**
- Handle missing values (e.g., replace age 118 with the median, fill missing income with the median, and encode unknown genders as 'U').
- Convert became_member_on to datetime format.
- Extract offer_id and amount from the value column in the transcript data.

**3. Data Merging:**

- Merge the portfolio, profile, and transcript datasets into a single DataFrame for analysis.

**4. Feature Engineering:**

- Create new features such as:
- Age Groups: Binned into categories (e.g., 0-18, 19-35, 36-50, 51-65, 66-100).
- Income Groups: Binned into categories (e.g., 0-30k, 30k-60k, 60k-90k, 90k-120k).
- Gender Groups: Consolidated into 'M', 'F', and 'Other'.

**5. Exploratory Data Analysis (EDA):**

- Visualize customer demographics (age, income, and gender distributions).
- Analyze offer performance by demographic groups and offer types.
- Explore transaction patterns and offer completion rates.

**6. Data Preparation for Modeling:**
  
- Prepare data for regression (predicting transaction amounts) and classification (predicting offer completion).
- One-hot encode categorical variables and handle missing/infinite values.

**7. Machine Learning Modeling:**

- Regression: Use RandomForestRegressor with RandomizedSearchCV to predict transaction amounts.
- Classification: Use RandomForestClassifier with RandomizedSearchCV to predict offer completion.
- Evaluate models using metrics like Mean Squared Error (MSE), R² Score, Mean Absolute Error (MAE), and classification accuracy.

**8. Insights and Recommendations:**
- Summarize key findings and provide actionable recommendations for Starbucks.
- 
# Summary of Results

Here's a quick summary of what we discovered:

## Customer Demographics

- **Age**: Most Starbucks app users are middle-aged (30-50 years old).
- **Income**: The majority of customers earn between $50k and $100k annually.
- **Gender**: The gender distribution is fairly balanced, with slightly more female users.

## Offer Performance

- **BOGO (Buy One Get One)** and **discount** offers are the most popular, with high completion rates.
- Middle-aged, medium-income females are the most likely to complete offers.

## Customer Behavior

- Customers tend to spend consistently over time, with no clear spikes or dips in transaction amounts.
- Most offers are received and viewed, but not all are completed, suggesting room for improvement in offer design or targeting.

## Key Insights

- **Demographics Matter**: Middle-aged, medium-income females are the most responsive to offers.
- **Offer Type Matters**: BOGO and discount offers perform better than informational offers.
- **Engagement is Key**: Many customers view offers but don't complete them, indicating a need for better targeting or incentives.

---

# Acknowledgements

This project was inspired by the **Udacity Data Scientist Nanodegree Capstone Challenge**. Special thanks to:

- **Starbucks** for providing the data.
- **Udacity** for the guidance and learning resources.

---

# How to Run This Project

Want to dive into the data yourself? Here's how:

- **Clone the Repo:**

```bash
git clone https://github.com/CDJulius/CapStone-StarbucksProject
```
- **Install Dependencies:**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

- **Run the Jupyter Notebook:**

- **Open Starbucks_Capstone.ipynb in Jupyter Notebook or JupyterLab.**

- **Execute the cells to perform the analysis step-by-step.**
  
# Blog Post
  
  For more insights and detailed analysis, check out my medium article about the Starbucks Capstone Challenge project.
  [Starbucks Capstone Challenge project](https://medium.com/@craig.julius/unveiling-customer-behavior-with-data-insights-from-starbucks-capstone-challenge-f287f010b3f2)

# Let's Connect!

Got questions, feedback, or just want to chat about data (or coffee)? Feel free to reach out:

- **Email**: <craig.julius@vodacom.co.za>
- **GitHub**: [CDJulius](https://github.com/CDJulius)

---

Thanks for stopping by! Now go grab a coffee and start exploring the data. ☕✨
