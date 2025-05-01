 Heart Disease Classification using Tree-Based Models

Dataset
This project uses the [Heart Disease Dataset](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset) from Kaggle. The dataset contains information about patients, including medical attributes such as age, cholesterol level, chest pain type, etc., and a target variable indicating the presence of heart disease.

- Rows: 303
- Features: 13
- Target: `target` (1 = heart disease, 0 = no heart disease)



 Objectives

1. Train a Decision Tree Classifier and visualize the tree.
2. Analyze overfitting and control tree depth.
3. Train a Random Forest and compare its accuracy.
4. Interpret feature importances using the Random Forest model.
5. Evaluate both models using cross-validation.



Tools & Libraries
- Python
- Pandas, NumPy
- Scikit-learn (`DecisionTreeClassifier`, `RandomForestClassifier`)
- Matplotlib
- Graphviz (optional for advanced tree visualization)



Steps Performed

 1. Data Loading & Preparation
- Read the dataset from `heart.csv`.
- Separated features and target column.
- Performed train/test split (80/20).

 2. Decision Tree Classifier
- Trained a `DecisionTreeClassifier` on the training data.
- Evaluated performance on the test set.
- Visualized the tree using `plot_tree()` from scikit-learn.

 3. Overfitting Analysis
- Trained multiple decision trees with varying `max_depth` from 1 to 15.
- Plotted training and testing accuracy to understand overfitting behavior.

 4. Random Forest Classifier
- Trained a `RandomForestClassifier` with 100 trees.
- Compared its accuracy and classification report with the decision tree.
- Random Forest showed improved generalization.

 5. Feature Importance
- Extracted and plotted feature importances from the random forest.
- Visualized which features contributed most to the model’s decisions.

 6. Cross-Validation
- Performed 5-fold cross-validation on both models.
- Reported average accuracy for both the decision tree and random forest.



Results

| Model              Test Accuracy   CV Accuracy (5-fold) 
| Decision Tree      81%             79%                 
| Random Forest      88%             84%                 

- The Random Forest performed better overall, both on the test set and under cross-validation.
