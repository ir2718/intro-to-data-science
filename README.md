# intro-to-data-science

Repository for the project in introduction to data science.

The project consists of 2 parts:
  - replicating the article: https://www.sciencedirect.com/science/article/pii/S1877050918308548
  - improving on the results from the article

The dataset used is the PIMA Indians dataset which can be found here: https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database

## Project notes

### Article replication
- histograms of features, scatter plots, box plots
- 3 classifiers: SVM, naive Bayes, decision tree
- hyperparameter optimization done using grid search
- evaluation done using 100 random train test splits instead of fixing the seed
- results on the test set:
 
|                      |  Precision | Recall    | F1 score | Accuracy   | AUC      | Hyperparameters used                                 |
| -------------------- | ---------- | --------- | -------- | ---------- | -------- | ---------------------------------------------------- |
| SVM                  | 0.517      | **0.734** | 0.603    | **0.768**  | **0.757**| ```{'C': 0.71, 'gamma': 'scale', 'kernel': 'poly'}```|
| Naive Bayes          | **0.600**  | 0.654     | **0.623**| 0.750      | 0.725    | ```{'var_smoothing': 0.0001}```|
| Decision tree        | 0.520      |0.648      |0.566     | 0.728      | 0.707    | ```{'ccp_alpha': 0, 'criterion': 'entropy', 'max_depth': 6, 'splitter': 'random'}```|

                 
