# CA03 – Decision Tree Algorithm 
## Data Source and Contents 

The dataset is obtained from the Census Bureau and represents salaries of people along with seven demographic variables. The following is a description of our dataset: 

• **Number of target classes**: 2 ('>50K' and '<=50K') [ Labels: 1, 0 ]

• **Number of attributes (Columns)**: 7 

• **Number of instances (Rows)**: 48,842 

The data is provided in a .csv file at "https://github.com/ArinB/MSBA-CA-Data/blob/main/CA03/census_data.csv?raw=true”, a Github location. Use the GitHub link in 
your Python code to “read” the data into a Data-frame. 

        url = "https://github.com/ArinB/MSBA-CA-Data/blob/main/CA03/census_data.csv?raw=true”
        data = pd.read_csv(url, encoding = "ISO-8859-1") 

Other content includes: 

1. Tree Tuning Cases.csv -> to help with automation of performance tuning 

2. CA03 -- Decision Trees Questions -> a Word Document with answers to questions throughout the case


----------------------------------------------------------------------------------------- 
## Computer Assignment Road Map

**Part 1:** Data Quality Analysis and Exploratory Data Analysis

    1. DQA: Find missing values, if any, outliers, descriptive statistics and perform necessary data cleansing. 
    2. EDA: Ensure that data is binned correctly.  Then, create stacked bar charts for each variable based on the 'y' column.  

**Part 2:** Build Decision Tree Classifier Models 

    1. Our variables are currently type=object, so we must make them type=category in order to encode them in the next step
    2. Check that column types converted correctly
    3. Use encoding to change values to an integer
    4. Split data into test and train datasets based on flag column
    5. Create our test and train variables
    6. Build the model and visualize using GraphViz
    7. Output the model performance indicators (AUC, confusion matrix, classification report, accuracy)

**Part 3:** Tune Decision Tree Performance

    1. Vary (hard-code) the following hyperparameters: 
      a. Split Criteria – ‘Entropy’ or ‘Gini Impurity'
      b. Minimum Sample Split – Minimum number of records required in any node for a further split to be attempted
      c. Minimum Sample Leaf – Minimum of samples in a leaf node to stop further splitting (becomes a leaf node)
      d. Maximum Depth – Maximum depth of the tree allowed
     2. Manually input the model performance indicators into the Tree Tuning Cases.xlsx file
     3. Indicate the best performing model 

**Part 4:** Automation of Performance Tuning

    Read in 'Tree Tuning Cases.csv' and create a function that allows the model performance vales to be fed in with one click.  

**Part 5:** Prediction using your trained Decision Tree Model.  

    1. Create a new record in the same format as our census data. 
    2. Create a mock dataframe based on this record, while making the necessary adjustments needed to run it through our best model. 
    3. Use the best model and the function predict_proba to obtain the probability array. 

-----------------------------------------------------------------------------------------
## Additional Comments 
Google Colab File has been linked to this repository.  However, should you make any adjustments, create a copy of your own to edit. 

