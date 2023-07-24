# Employee-Network-Analysis-Project

Libraries:
- **NetworkX, Scikit-learn, Pandas, & Numpy**

1. Graphs read in using **NetworkX**
2. Graph types determined using various graph features (**distance measurements, centrality, etc.**) among number of potential choices (**Barabasi-Albert preferential attachment graphs, Watts-Strogatz small world network models, etc.**)
3. Goal: identify the people in the network with missing values for the node attribute `ManagementSalary` and predict whether or not these individuals are receiving a managment position salary through ML-based value imputation
    -  Feature extraction performed using graph **node-wise** features (**clustering coefficient, betweenness, degree, eigenvector, and closeness centrality, page rank, HITS algorithm hub and authority scores**)
    - Training and test data prepared by segmenting feature values by presence of target variable
    - **Random Forest Classifier** fit (**Scikit-learn**) on available data to produce model
    - Model metrics determined through Coursera autograder and **ROC-curve AUC** of > **0.85** achieved
4. Goal: using partially missing data on upcoming employee connections, predict future connections between all employees of the network.
    - Feature extraction on **edge-wise** features (**common neighbor coefficient, resource allocation index, jaccard coefficient, preferential attachment score, common neighbor soundarajan hopcroft score**)
    - Data split into training and test sets for prediction on missing data
    - **Gradient Boosting Classifier** fit (**Scikit-learn**) on non-missing data to create model
    - Model run against witheld missing data on Coursera autograder and **ROC-curve AUC** > **0.85** achieved.
