# ML_model_analysis
Apply and evaluate different ML models on a cardiovascular disease dataset and understand their performance

------------------------------------------------------------------------------------------------------------------------

##  **1. Decision Tree Classifier (ID3 Algorithm)**

### -> Definition
A Decision Tree is a flowchart-like structure used for classification and regression. The ID3 (Iterative Dichotomiser 3) algorithm uses entropy and information gain to decide which attribute to split at each node.

### -> How It Works
- Uses entropy to measure impurity.
- Selects features based on highest information gain.
- Builds a tree structure recursively.

### -> Requirements
- Supervised dataset
- Clean, labeled data
- Categorical or numerical features

### -> Real-Life Applications
- Disease risk prediction
- Credit risk scoring
- Customer segmentation
- Student performance prediction

### -> In This Project
- Used `DecisionTreeClassifier` with `criterion='entropy'`
- Trained on 80% data
- Converted age from days to years

### -> Performance
- **Accuracy**: 63.6%
- **Precision**: 63.78%
- **Recall**: 63.14%

### -> Pros
- Easy to interpret
- Supports both types of features
- Visualizable

### -> Cons
- Prone to overfitting
- Sensitive to small changes

------------------------------------------------------------------------------------------------------------------------

##  **2. Linear Regression**

### -> Definition
Linear Regression models the relationship between a dependent variable and one or more independent variables using a straight-line fit.

### -> How It Works
- Minimizes squared differences between predicted and actual values
- Outputs continuous values

### -> Requirements
- Linear relationship between features and output
- Continuous dependent variable
- Low multicollinearity

### -> Real-Life Applications
- Predicting housing prices
- Sales forecasting
- Stock price estimation
- Insurance risk pricing

### -> In This Project
- Trained to predict `cardio` (binary — not ideal)
- Used same data and preprocessing

### -> Performance
- **R² Score**: 0.116
- **MSE**: 0.2209

### -> Pros
- Simple and fast
- Interpretable coefficients

### -> Cons
- Not suitable for classification
- Sensitive to outliers

------------------------------------------------------------------------------------------------------------------------

##  **3. Support Vector Machine (SVM)**

### -> Definition
SVMs are supervised learning models that separate classes using an optimal hyperplane with maximum margin.

### -> How It Works
- Finds boundary with largest margin
- Supports kernels for non-linear data
- Can output probabilities with proper settings

### -> Requirements
- Clean, numeric features
- Well-labeled classification data
- Often requires scaling

### -> Real-Life Applications
- Face detection
- Spam filtering
- Disease classification
- Gene prediction

### -> In This Project
- Evaluation metrics used: ROC, PR curve, confusion matrix
- Training part not shown

### -> Performance (Demo-based)
- Not trained in code, but metrics visualized

### -> Pros
- Effective for high-dimensional data
- Good accuracy when tuned
- Supports non-linear classification

### -> Cons
- Slow with large datasets
- Hard to interpret
- Needs careful tuning

------------------------------------------------------------------------------------------------------------------------


##  Model Comparison

| Aspect                  | Decision Tree (ID3)        | Linear Regression        | SVM                       |
|-------------------------|----------------------------|---------------------------|---------------------------|
| Model Type              | Classification             | Regression                | Classification            |
| Data Suitability        | Categorical output         | Continuous output         | Categorical output        |
| Output Type             | Binary (0/1)               | Continuous                | Binary (0/1)              |
| Interpretability        | High                       | High                      | Medium                    |
| Performance in Project  | Moderate (~63% accuracy)   | Low (~11% R²)             | Not trained (demo eval)   |
| Training Complexity     | Low                        | Very low                  | Medium to High            |
| Best Use Case           | Decision-based systems     | Numeric prediction        | Complex classification    |
| Pros                    | Visual & interpretable     | Fast, simple              | Accurate, flexible        |
| Cons                    | Overfitting                | Not for binary tasks      | Requires tuning, slow     |
| Real-Life Use           | Medical, finance, retail   | Forecasting, pricing      | Image, NLP, bioinformatics|


------------------------------------------------------------------------------------------------------------------------

##  Conclusion

Each model has its strengths:
- **ID3 Decision Trees** offer good interpretability with moderate performance.
- **Linear Regression** is not suited for classification problems.
- **SVM**, though not implemented here, is highly capable for classification if trained properly.

This comparison helps choose the right model based on dataset type, goals, and complexity.

------------------------------------------------------------------------------------------------------------------------

##  Resources & Links

Here are the related notebooks from where you can directly access the code :

- 🌳 [ID3 Decision Tree - Google Colab](https://colab.research.google.com/drive/1ZvQ8nxuMbwScnxqXMixDNK5mvvA8RJud?usp=sharing)
- 📉 [Linear Regression - Google Colab](https://colab.research.google.com/drive/1ug_NENw9Uq93gZHB9jp6OjElCDsCqwUu?usp=sharing)

------------------------------------------------------------------------------------------------------------------------

##  Dataset & Running the Code

The dataset provided in the main section in the one I’ve used in my code.  
You’re encouraged to rerun the notebooks and explore the models yourself!  
However, before executing any code, please **make sure to upload the dataset** (as it is required by the code cells).

You can either:
- Download the dataset from the **"Files" section** in this repository and upload it to your Colab environment manually, **or**
- Get the dataset directly from [Kaggle](https://www.kaggle.com/) by searching for “cardiovascular disease dataset” and uploading it before execution.
