# BreastCancer

ABSTRACT

Breast cancer is the second leading cause of death and first leading cancer in women.  The initial phase of breast cancer detection methods are ultrasound and mammogram.  A biopsy sample is necessary to definitively tell whether a patient has breast cancer.  Pathologists look under the microscope and analyze physical characteristics of the cells.  Normal cells are round and have similar size.  Cancer cells have higher copies of DNA, therefore the cell nucleus is larger.  Cancer cells also have irregular shape or higher architecture.  The larger size and higher architecture are characteristics we can use to determine whether a tumor is benign or malignant.  

The data of my study is taken from Kaggle Breast Cancer (Diagnostic) Dataset.  I wanted to know, can we classify benign and malignant cells of a new patient?  This is my first Kaggle Jupyter Notebook submission -- so I am open to comments -- I am new to Data Science and Python.  I looked into six algorithms: Logistic Regression, Naive Bayes’, k-Nearest Neighbors, Random Forest, Support Vector Machine, and Super Learner.  With a combination of balancing data and resampling, replacing outliers with group means, test harness and cross validation bootstrapping, and this nice dataset, Random Forest gave an accuracy of 99.44%.  SVM and Super Learner give similar results.  Such extraordinary accuracy suggests that we can apply data science along with doctors’ expertise to study cells from many patients.  In the future, it would be exciting to apply data science and proactively monitor a vast number of women’s breast health so that we can have early intervention should it be helpful. 



Formulate the Project Research Framework

(A) Brest Cancer Dataset

The data of this project is taken from Kaggle Breast Cancer Wisconsin (Diagnostic) Data Set https://www.kaggle.com/uciml/breast-cancer-wisconsin-data. The goal is to Predict whether the cancer is benign or malignant. Another goal is to increase prediction accuracy. The same data is also found in UC Irvine Machine Learning Repository https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29. Data was donated in 1995.

There are 569 patients. Features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei present in the image. There are 32 attributes and no missing value. Below is a description of the attributes. There are three sets of (a)-(j). For example, attribute 3 is radius_mean, attribute 13 is radius_se (standard error), and attribute 23 is radius_worst.

Attribute Information:

1) ID number

2) Diagnosis (M = malignant, B = benign)

3-32)

Ten real-valued features are computed for each cell nucleus:

a) radius (mean of distances from center to points on the perimeter)

b) texture (standard deviation of gray-scale values)

c) perimeter

d) area

e) smoothness (local variation in radius lengths)

f) compactness (perimeter^2 / area - 1.0)

g) concavity (severity of concave portions of the contour)

h) concave points (number of concave portions of the contour)

i) symmetry

j) fractal dimension ("coastline approximation" - 1)
Research Questions¶

    Can we separate two kinds of tumor, malignant and benign?
    What are the most important features of the cell in determining a cancerous tumor?
    How accurate is the prediction?

(B) Scientific Method

The research questions are: Can we classify benign and malignant cells of a new patient? Can data science be applied as a tool for doctors to make breast cancer diagnosis? Can data science give insights in conjunction with doctors expertise to study characteristics of cancer cells? We will train our data science models using the data above. They are nucleus features of cells from breast mass and their diagnosis.

We hypothesize that H1: the nucleus of a malignant cell is larger and has more architecture than that of a benign cell. The null hypothesis H0 would be malignant and benign cells are the same.

We predict that our machine learning algorithms can predict if a new patient is likely to have cancer.

The hypothesis will be tested by a statistical analysis t-test. We first assume the null hypothesis is true: malignant and benign cells are the same. We build a partial sampling distribution of the null hypothesis. If the p-value is less than the alpha/2, we reject H0 and H1 is statistically true.

If H1 is true, malignant cells are larger and have more architecture than benign cells, the next steps would be: 1. to predict pre-cancer cells, 2. to use our machine learning models in more clinical data, and compare our prediction with doctor's diagnosis and validate our models.
