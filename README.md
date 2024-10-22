# Well-Logs-Facies-Classification

Facies are the studied from core samples in every half foot and matched with logging data in well location. Facies classification is one of the most important tasks that geoscientists work on development and exploration projects. Sedimentary facies reflect particular physical, chemical, and biological condition that unit experienced during sedimentation process. To study these facies, rock samples are required. In this project, I'll use these log data to train supervised classifiers in order to predict discrete facies groups.

### Laibraries & Python Modules 
* Pandas
* Numpy
* Matplotlip
* Sklearn
* IPython.display
* Seaborn
* Math
* Pydotplus....

### Data

The data set used came from a University of Kansas class exercise on the Hugoton and Panoma gas fields. For more on the origin of the data, see Dubois et al. (2007). This was a  consortium project to use machine learning techniques to create a reservoir model of the largest gas fields in North America, the Hugoton and Panoma Fields.

![text](https://user-images.githubusercontent.com/68614187/106039903-53fba780-609f-11eb-82ea-f28a92de5ddb.png)

![test](https://user-images.githubusercontent.com/68614187/106040457-1e0af300-60a0-11eb-90b1-fdc1e899aef7.png)

Geologically sometimes the boundaries of the facies are not clear and could show some transition, hence following table list the facies, the abreviated labels and approximately next attacching facies.

![test](https://user-images.githubusercontent.com/68614187/106040494-29f6b500-60a0-11eb-9688-6d4e8ec10aec.png)


## Exploratory Data Analysis
A thorough data cleaning, transformation, data exploration and features engineering was performed in order to prepare dataset for testing the classifier models.

### Target Variable Distribution
![text](https://user-images.githubusercontent.com/68614187/106041128-097b2a80-60a1-11eb-98be-0abaa52039cf.png)

### Features Relevancy & Multivariate Analysis

![text](https://user-images.githubusercontent.com/68614187/106041196-1bf56400-60a1-11eb-913f-f2f47a7359b5.png)

![text](https://user-images.githubusercontent.com/68614187/106043439-0a618b80-60a4-11eb-95f6-516152fda865.png)

## Testing Different Classifiers

Different classification models, i.e. Logistic Reggression, Support Vector Machine, KNN, Decision Tree, Random Forest and Gradient Boosting have been tested and compared for the best model selection. The'classification report' and an accuracy of~80.7 % shows 'Gradient Boosting' might be the best choice.

![text](https://user-images.githubusercontent.com/68614187/106046625-1ea78780-60a8-11eb-933b-bfc60968d734.png)

### Performence of Gradient Boosting Model

The diagonal row in confusion metrix represents the true positives, the instances that were correctly classified, rest of the matrix represents the number of instances that were incorrectly classified. Fi Score shows 0.80, which is pretty good. 

![text](https://user-images.githubusercontent.com/68614187/106048683-cfaf2180-60aa-11eb-9d9c-24656de5adb3.png)


### Interpreting the Metrix & Features Importance

Features show the combined effect to predict the log facies. Classification report shows F1 score for individual facies. BS is ~ 95% and PS is ~68% 

![text](https://user-images.githubusercontent.com/68614187/106049815-354fdd80-60ac-11eb-94b4-a738970fec30.png)

![text](https://user-images.githubusercontent.com/68614187/106049884-4567bd00-60ac-11eb-9922-9c69c43cebf0.png)

### Precision - Recall Curve

Precision shows that what proportion of positive predictions are correct and recall tells us what proportion of positives are correctly predicted. Curves exhibit the precision and recall range from 60 to almost 100% of the Facies classes.

![text](https://user-images.githubusercontent.com/68614187/106051086-9926d600-60ad-11eb-9410-ae4d1efd4ac5.png)

### ROC - Receiver Operating Characteristic Curve

Curves showing in top left corner exhibit max true positive and minimizing false positive. Results show that curves tend to be in top left corner, however still counting the false positive. 

![text](https://user-images.githubusercontent.com/68614187/106051265-db501780-60ad-11eb-8b49-c9157f67dd9d.png)

## Origional Facies VS Predictions

![text](https://user-images.githubusercontent.com/68614187/106051516-2702c100-60ae-11eb-9c1d-979f0db51559.png)




