# Customer-Segment-Identification

## Project Overview
In this project, Bertelsmann partners AZ Direct and Arvato Financial Solutions have provided two datasets one with demographic information about the people of Germany, and one with that same information for customers of a mail-order sales company. It attempts to look at the relationships between demographics features, organize the population into clusters, and see how prevalent customers are in each of the segments obtained using unsupervised learning techniques and PCA (Principal Component Analysis).

## Set Up
The dataset might not be publicly available and subject to terms and conditions of usage by Udacity and Arvato. The clustering was conducted with scikit learn and seaborn for visualization.

## Steps in the Project

### Step 0: The Data
The files available for the project are:

    Udacity_AZDIAS_Subset.csv: Demographic data for the general population of Germany; 891211 persons (rows) x 85 features (columns).
    Udacity_CUSTOMERS_Subset.csv: Demographic data for customers of a mail-order company; 191652 persons (rows) x 85 features (columns).
    Data_Dictionary.md: Information file about the features in the provided datasets.
    AZDIAS_Feature_Summary.csv: Summary of feature attributes for demographic data.
    Identify_Customer_Segments.ipynb: Jupyter Notebook divided into sections and guidelines for completing the project. The notebook provides more details and tips than the outline given here.

### Step 1: Exploratory Data Analysis

The analysis was done to familiarize ourselves with the dataset. A few key points:

    How are missing or unknown values encoded in the data? Are there certain features (columns) that should be removed from the analysis because of missing data? Are there certain data points (rows) that should be treated separately from the rest?
    Consider the level of measurement for each feature in the dataset (e.g. categorical, ordinal, numeric). What assumptions must be made in order to use each feature in the final analysis? Are there features that need to be re-encoded before they can be used? Are there additional features that can be dropped at this stage?
    
A cleaning function was written to preprocess the data easily.

### Step 2: Feature Transformation

The features are transformed to reduce the compelxity of computation, while attending to the following points:

    The first technique that you should perform on your data is feature scaling. What might happen if we don’t perform feature scaling before applying later techniques you’ll be using?
    Once you’ve scaled your features, you can then apply principal component analysis (PCA) to find the vectors of maximal variability. How much variability in the data does each principal component capture? Can you interpret associations between original features in your dataset based on the weights given on the strongest components? How many components will you keep as part of the dimensionality reduction process?

### Step 3: Clustering

The unsupervised technique utilized was K-means clustering algorithm with the following points in mind :

    Use the k-means method to cluster the demographic data into groups. How should you make a decision on how many clusters to use?
    Apply the techniques and models that you fit on the demographic data to the customers data: data cleaning, feature scaling, PCA, and k-means clustering. Compare the distribution of people by cluster for the customer data to that of the general population. Can you say anything about which types of people are likely consumers for the mail-order sales company?
    
The HTML file serve as markdown version of the report, detailing findings after clustering.
