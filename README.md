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
- `UnitPrice`: Price per unit (GBP)
- `CustomerID`: Unique customer identifier
- `Country`: Customer country


## Business Requirements
* The requirement is to uncovers customer buying habits and popular products. These insights should help to refine pricing, tailor marketing, and boost sales by delivering what customers want.


## Hypothesis and how to validate?
Removing unmatchable returns will minimally affect the validity of the sales analysis, given their small quantity relative to total records. Manually removing the largest unmatched return/sale pairs will further limit their influence on key business metrics. Focused on business-driven cleaning, meaning high-value items were kept untouched as they are not ourliers.

Validation:
* Attempted to find all matching returns and sales using business logic. When matching failed, counted total remaining returns and confirmed they represented a small percentage of the dataset.
* Checked impact by comparing total sales and statistics before and after removing returns.
* Manually checked and removed the largest returns and corresponding sales to ensure top outliers were not misrepresented.
* 

This method should reveal a better customer behavior.

## Project Plan
* I tackled this analysis in four focused phases over two days. First, I dove deep into data cleaning wrestling with messy real-world issues like returns and missing values. Next, to build a solid foundation with descriptive statistics to understand our basic business health. Then come the exciting part: uncovering customer stories through segmentation and product analysis. Finally, I connect all the dots to provide actionable business recommendations.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* Data privacy: All analysis used anonymized transaction data—no PII was exposed.
* Bias/fairness: Checked for and documented bias in which customers or products drove the most sales.
* Societal/legal: Ensured no results would harm customer privacy.
* Adjusted outlier removal to respect business context (e.g., high-value, legitimate sales).

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Unfixed Bugs
* No currently unfixed bugs—all code, data cleaning, and graphs work as expected for this notebook-based report.
* Framework Shortcomings: No native support for matching returns across fuzzy product or time mismatches; chosen approach works for precise matches only.
* Skill Gaps: Identified the need to learn vectorized pandas/merge for speed (implemented with guidance).
* Feedback Evidence: Instructor, Peer and LLM feedback helped improve cleaning workflow and documentation clarity. Adjusted approach from row-wise loops to merges for efficiency while working on return analysis though it was not successful at the end with the findings.

## Development Roadmap
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
* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site


## Acknowledgements (optional)
* Thank the people who provided support through this project.
* Emma for helping to find the ringt scope as otherwise I can work on this weeks 
* Spenser for fine tunign the though process in Data Cleaning and Transformation 
* Every team member who helped by unblocing me and asking help when the blocked
* LLM tools for unblocking and branstorming support