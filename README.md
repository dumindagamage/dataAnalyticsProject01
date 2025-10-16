# Project Online Retail Transaction Analysis

This project analyzes online retail transaction data to understand customer behavior, identify popular products, and optimize business strategies. The analysis provides actionable insights for improving sales, marketing effectiveness, and customer retention.

**Project Duration**: 2-day individual project  
**Analysis Type**: Descriptive Analytics & Customer Segmentation  
**Tools Used**: Python, Pandas, Matplotlib, Seaborn, Plotly

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
**Source**: [Online Retail Transactions Dataset from Kaggle](https://www.kaggle.com/datasets/abhishekrp1517/online-retail-transactions-dataset)

**Original Size**: 541,909 transactions  
**Time Period**: December 2010 - December 2011  
**Geography**: Multinational, primarily United Kingdom

**Key Columns**:
- `InvoiceNo`: Unique transaction identifier
- `StockCode`: Product code
- `Description`: Product description
- `Quantity`: Number of items purchased
- `InvoiceDate`: Date and time of transaction
- `UnitPrice`: Price per unit
- `CustomerID`: Unique customer identifier
- `Country`: Customer country


## Business Requirements
* The requirement is to uncovers customer buying habits and popular products. These insights should help to refine pricing, tailor marketing, and boost sales by delivering what customers want.


## Hypothesis and how to validate?
Removing unmatchable returns will minimally affect the validity of the sales analysis, given their small quantity relative to total records. Manually removing the largest unmatched return/sale pairs will further limit their influence on key business metrics. Focused on business-driven cleaning, meaning high-value items were kept untouched as they are not ourliers.

Validation:
* Attempted to find all matching returns and sales using business logic. When matching failed, counted total remaining returns and confirmed they represented a small percentage of the dataset.
* Checked impact by comparing total sales and statistics before and after removing returns.
* Manually checked and removed the largest two return quantities and corresponding sales to ensure top outliers were not misrepresented while reducing the bais in the data set. 

## Project Plan
* High-Level Steps Taken:
1. Data Collection: Downloaded the Online Retail Transactions dataset from Kaggle as a .csv file and imported it into Jupyter Notebook using Pandas
2. Data Processing: Implemented ETL pipeline to clean data, handle missing values, and create new features like revenue calculations and transaction types
3. Data Analysis & Interpretation: Visualized sales trends, customer segments, product performance, and transaction patterns over time using descriptive statistics and interactive charts

* Data Management:
1. Data was managed using Pandas DataFrames throughout the entire process
2. Cleaning and transformation steps were organized in structured functions within Jupyter Notebook for transparency and reproducibility
3. Each analysis step included immediate visualization to validate results and ensure data quality

*Research Methodologies Used:
1. Exploratory Data Analysis (EDA)
2. Descriptive Statistics 
3. RFM Analysis
4. Data Visualization techniques 

## The rationale to map the business requirements to the Data Visualisations
The goal of this project was to support business decisions by transforming raw transaction data into actionable insights. I tried to design  data visualisation with a specific business question or requirement in mind to make the analysis relevant and valuable as possible.

1. Understanding Business Performance
- Key Business Metrics
- Monthly Sales vs Returns Trend

2. Customer Behavior Analysis
- Customer Segmentation
- RFM Analysis

3. Product Strategy Optimization
- Top Products by Revenue
- Products by Return Value
- Revenue by Product Category

4. Sales & Marketing Planning
- Sales by Day of Week
- Monthly Sales Pattern
- Country Performance

## Analysis techniques used
1. Data Cleaning & Preparation:
- Techniques: Handled duplicates, filled missing product descriptions, categorized data set into (sales, returns), and created new features like Revenue and date components.
- Approach: Used business context rather than pure statistical methods treated negative quantities as returns and capped extreme values instead of complete removal.

2. Descriptive Analysis:
- Techniques: Used Pandas to calculate key business metrics - total revenue, average transaction value, return rates, and customer/product counts.
- Context: All metrics calculated separately for sales vs returns to provide accurate business picture.
- Challenges: Initially attempted to remove return transactions along with their corresponding original sales by matching invoice numbers and product details. However, technical limitations in identifying these pairs accurately due to inconsistent invoice numbering and product matching complexities required extensive time and advanced pandas techniques. The final approach separated the dataset into distinct sales and returns analyses.

3. Exploratory Data Analysis (EDA):
- Techniques: Combined Matplotlib/Seaborn for static charts and Plotly for interactive visualizations to uncover patterns in sales trends, customer behavior, and product performance.
- Visualizations: Line charts for trends, bar charts for rankings and scatter plots for segmentation.
- GenAI Usage: Utilized Perplexity AI for brainstorming data analytics approaches and identifying how to address the business questions with the available dataset.

4. Customer Segmentation:
- Techniques: Implemented RFM (Recency, Frequency, Monetary) analysis using business-defined thresholds rather than statistical clustering.
- Segmentation: Created four customer groups (VIP, Loyal, Regular, At-Risk) based on purchasing patterns for targeted marketing.

5. Outlier Management:
- Approach: Used business context and manual capping instead of statistical methods like IQR, preserving important bulk purchases while reducing skew.
- Rationale: Maintained business-relevant transactions that statistical methods might incorrectly flag as outliers. (This approach was guided by instructor feedback emphasizing the importance of business context over rigid statistical rules.)


## Findings and Conclusion

1. Business Performance:
The analysis revealed a healthy online retail business with £10.3M in gross sales revenue and a manageable 6.2% return rate. The customer base of 4,371 unique customers demonstrates solid market penetration, while the product portfolio of 4,069 items shows significant variety.

2. Customer Behavior Insights:  Customer segmentation identified four distinct groups with clear behavioral patterns with the RFM analysis

- VIP Customers (28% of customers, 77% of revenue): High-value segment spending £6,190 on average with frequent purchases (134 transactions) and high engagement (16 days recency). Critical for premium retention strategies.
- Loyal Customers (32% of customers, 16% of revenue): Consistent purchasers with £1,182 average spend and regular activity (49 transactions, 55 days recency). Represent stable revenue streams.
- Regular Customers (13% of customers, 5% of revenue): Moderate buyers with £881 average spend and 34 transactions. Show significant growth potential with proper engagement.
- At-Risk Customers (26% of customers, 5% of revenue): Low-engagement segment with £463 average spend and infrequent purchases (207 days since last order). Require immediate reactivation efforts.

3. Product Performance: The product analysis revealed
- Significant revenue concentration in top products (15 products generating 12% of total revenue)
- Strong performance in Home Decor and Lighting categories
- High-return products requiring investigation

4. Temporal Patterns: Clear seasonal and weekly patterns emerged
- Consistent sales growth throughout the 2011 analysis period
- November peak aligning with holiday shopping season preparation
- Weekend purchasing patterns indicating consumer shopping habits
- Stable monthly performance with identifiable seasonal trends

5. Key Finding & Conclusion:
- The VIP customers driving majority revenue, highlighting the importance of customer retention over acquisition. 


## Ethical considerations
* Data privacy: No PII data was found in the data set.
* Adjusted outlier removal to respect business context (e.g., high-quantities).

## Dashboard Design
* Most visualizations are available within the notebooks.
* The only interactive graph can be found in the repository under /insights.

## Unfixed Bugs
* No currently unfixed bugs all code, data cleaning, and graphs except plotly work as expected for this notebook-based report.
* Skill Gaps: Identified the need to learn vectorized pandas/merge for speed (implemented with guidance).
* Feedback Evidence: Instructor, Peer and LLM feedback helped improve cleaning workflow and documentation clarity. 

## Development Roadmap
1. Challenges Faced:
* During the Data Cleaning, Returns could not be matched to their original sales within the dataset. It took considerable time to analyze and confirm that there was no reliable way to link them. I spent longer than expected exploring this before realizing it was beyond the scope of a two-day project. Although it was a valuable learning experience, it affected my time management as I dedicated more effort to this task than planned.
2. Lessons Learned:
* Iterative Approach: Data cleaning and analysis often requires multiple passes as understanding deepens
* Business Context is Crucial: Technical analysis must be grounded in real-world business understanding
* Visualization Simplicity: Clear, simple visualizations often communicate insights more effectively than complex charts
* Documentation as You Go: Maintaining notes and comments throughout the process saves time later
* After cleaning up data (removing duplicates, filtering rows), always reset the index. Otherwise, it will end up with gaps that break things later.
* When working with categories (like weekdays or product types), comparisons can be tricky. Sometimes asking for 'Sunday' returns nothing because pandas sees categories differently than regular text. The fix? Either convert to text first or set up categories properly from the start.
3. New skills or tools planning to learn:
* Develop the ability to interpret the story behind the data, as datasets alone are not sufficient for making effective ETL and analysis decisions.
* Gain a deeper understanding of pandas and various data visualization libraries and tools.
* Enhance proficiency with GitHub Copilot and Generative AI tools to support brainstorming and accelerate development.

## Deployment
* All notebooks are executable in Jupyter Notebook (.ipynb).
* Data cleaning and analysis steps are clearly documented.
* Run the ETL notebook first to generate the processed dataset.
* Then, use the analysis notebook with the processed data to produce insights.
* All required dependencies (pandas, numpy, matplotlib, seaborn, plotly) are listed in requirements.txt.

## Main Data Analysis Libraries
* pandas: Data loading, cleaning, transformation (pd.read_csv, .groupby, .merge)
* numpy: Some numeric operations for quantiles or absolute values
* matplotlib: Basic static charts and labels
* seaborn: Enhanced summary plots and distributions
* plotly: Interactive customer segmentation/product charts

## Credits 
* The dataset used in this project was sourced from Kaggle.
* I developed the analysis using the Code Institute Project Template 
* Referred to Code Institute learning materials to review data visualization techniques.
* Perplexity AI supported idea generation and clarification, while GitHub Copilot assisted with code review and optimization.

### Content
- Some sections of README were refined using ChatGPT.

### Media ---
- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site

## Acknowledgements
* Thank you to everyone who supported me in neumerous ways throughout this project.
* To my course instructor, for helping me refine my thought process in data cleaning and transformation.
* And to my fellow team members, for their collaboration both when they helped me overcome challenges and when I could return the favor.
