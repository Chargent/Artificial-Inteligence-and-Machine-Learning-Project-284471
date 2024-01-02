# **Trains - Artificial Intelligence and Machine Learning Project**🚆
## Group Members

Pierpaolo Ceccarelli 284451

Andrea Contino 284471

Piergiorgio Zannella 284951

## Introduction🚅🚝🚆🚂

Our project aims at augmenting the prediction of customer satisfaction for the ThomasTrain Company by integrating machine learinig and data science techniques with customer service insights. Our project dives into the "trains.csv" dataset, which encompasses a variety of variables including demographic details, travel information, and service ratings. The primary objective is to deduce customer satisfaction levels indirectly through analysis of the data, as opposed to relying solely on direct customer feedback, to effectively target users with promotions and making the retention higher.

In the initial phase, we conducted an exploratory data analysis (EDA) to unearth trends and interconnections within the data. To prepare the dataset for effective machine learning modeling, we undertook several preprocessing steps such as filling in missing values, converting categorical data into a usable format, and eliminating data outliers. 

Our aim was to construct machine learning models that could accurately categorize customers into "satisfied" or "unsatisfied" groups, to grasp the nuanced factors influencing customer satisfaction. This was achieved through a combination of data preprocessing, analysis, and the application of machine learning techniques.

## Methods 🔍

Describe your proposed ideas (e.g., features, algorithm(s), 
training overview, design choices, etc.) and your environment so that: 
• A reader can understand why you made your design decisions and the 
reasons behind any other choice related to the project 
• A reader should be able to recreate your environment (e.g., conda list, 
conda envexport, etc.) 
• It may help to include a figure illustrating your ideas, e.g., a flowchart 
illustrating the steps in your machine learning system(s)

----------------------------

In this section, we outline the methods used for our project. Our approach involved a blend of data handling, visualization, and machine learning techniques.

First we conducted Exploratory Data Analysis (EDA) to take a look at our data features and properties. We started with the basics, utilizing Pandas for managing our dataset, for visualization we turned to Matplotlib and Seaborn, essential  for designing plots and statistical graphs. After loading our dataset into a Pandas DataFrame, we took a look into its structure. This step was crucial for setting up our subsequent analysis and to have a general understanding of the distributions. 

![Alt text](Images/distribution_histograms.png)

We graphed the distribution of numerical features and the target variable “Satisfied” through histograms and pie charts gave us insights into the skewness and spread of our data. 

![Alt text](Images/pie_chart.png)

We dove into the dataset by looking at its shape, data types, missing values, and unique values. This comprehensive overview helped us in tailoring our preprocessing strategies, for instance in the decision to remove or integrate the Nan values.

The categorical 'Satisfied' column was encoded into numerical values (0 and 1), a necessary step for the classification models we intended to use. 
 
Then we plotted a correlation heatmap to get the most correlated features to our target variable. It helped us pinpoint which variables might be key players. 

<img width="829" alt="m1" src="https://github.com/acagnucci/AI-Project/assets/150381254/eac4e97c-7e3e-4c0b-9024-80a069a751b2">

 
 
Data Preprocessing and Pipeline Construction: 
 
Feature Selection and Splitting: Post-EDA, we separated our target variable “Satisfied” and identified key numerical and categorical columns for modeling. 
 
Pipeline Setup: We built a machine learning pipeline using Scikit-learn's “Pipeline” and “ColumnTransformer”. This helped us neatly bundle our preprocessing steps, handling numerical and categorical data separately but in parallel. 
 
For numerical data, we used “SimpleImputer” for missing values and “StandardScaler” for normalization. 
For categorical data, “SimpleImputer” and “OneHotEncoder” took care of missing values and transformation, respectively. 
 
Training and Test Split: We split our dataset into training and test sets (80-20 split), and further partitioned the training data to create a validation set. This setup was essential for unbiased model evaluation. 
 
 
Further EDA and Machine Learning Warnings: 
Deeper Dive into Data: We revisited our numerical data, plotting histograms to catch any nuances we might have missed initially. The correlation matrix also got a second look, helping us refine our feature selection. 
   
Handling Machine Learning Warnings: We encountered convergence warnings with logistic regression, which we addressed by adjusting the number of iterations and ensuring proper data scaling. 


 <img width="1185" alt="h2" src="https://github.com/acagnucci/AI-Project/assets/150381254/08d9de25-48f6-4a31-9a7d-cf9455c5df8a">


<img width="765" alt="m2" src="https://github.com/acagnucci/AI-Project/assets/150381254/04cafc52-5c13-4744-a913-ab1cf6ed2c4b">


 
Model Training and Hyperparameter Tuning: 
 
Model Selection: We chose Logistic Regression, Decision Tree, and Random Forest for our classification task. Each brought a unique perspective to the table. 
 
Training and Initial Evaluation: We trained each model on our dataset, evaluating their performance using a validation set. This was our first checkpoint to see how our models fared with the default settings. 
 
Tuning Hyperparameters: Using “RandomizedSearchCV”, we fine-tuned our models. For example, we adjusted the Decision Tree's depth, sample splits, leaf samples, and criterion based on accuracy. 
 
Learning Curves and Performance Evaluation: We plotted learning curves to understand our models' behavior with increasing data. The final performance was evaluated on the test set using metrics like accuracy, precision, recall, F1-score, and ROC-AUC score. 

## Experimental Design ✒️

Describe any experiments you conducted to 
demonstrate/validate the target contribution(s) of your project; indicate the 
following for each experiment: 
• The main purpose: 1-2 sentence high-level explanation 
• Baseline(s): describe the method(s) that you used to compare your work 
to 
• Evaluation Metrics(s): which ones did you use and why?


## Results 📑

Describe the following: 
• Main finding(s): report your final results and what you might conclude 
from your work 
• Include at least one placeholder figure and/or table for communicating 
your findings 
• All the figures containing results should be generated from the code


## Conclusions 💡

List some concluding remarks. In particular: 
• Summarize in one paragraph the take-away point from your work. 
• Include one paragraph to explain what questions may not be fully 
answered by your work as well as natural next steps for this direction of 
future work

