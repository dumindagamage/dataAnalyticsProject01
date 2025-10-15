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

## The rationale to map the business requirements to the Data Visualisations --
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used --
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* Data privacy: All analysis used anonymized transaction data—no PII was exposed.
* Adjusted outlier removal to respect business context (e.g., high-value, legitimate sales).

## Dashboard Design --
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Unfixed Bugs
* No currently unfixed bugs all code, data cleaning, and graphs except plotly work as expected for this notebook-based report.
* Skill Gaps: Identified the need to learn vectorized pandas/merge for speed (implemented with guidance).
* Feedback Evidence: Instructor, Peer and LLM feedback helped improve cleaning workflow and documentation clarity. 

## Development Roadmap --
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

Challenges Faced during the Data Cleaning:
* Returns could not be matched to an original sale within the data. It took more time to analyze and identify there is not way to match them and remove. 


## Deployment
* All code and analysis notebooks are runnable in Jupyter Notebook (.ipynb).
* Data cleaning and analysis steps were well documented along with the code for reproducibility.
* All dependencies listed in requirements.txt (pandas, numpy, matplotlib, seaborn, plotly).

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


### Content ---

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media ---

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site


## Acknowledgements (optional)
* Thank you to everyone who supported me throughout this project.
* To my course instructor, for helping me refine my thought process in data cleaning and transformation.
* And to my fellow team members, for their collaboration both when they helped me overcome challenges and when I could return the favor.
