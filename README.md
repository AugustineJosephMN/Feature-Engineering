# Feature-Engineering
## Different types of Missing Data.
### Missing Completely at Random, MCAR:
A variable is missing completely at random (MCAR) if the probability of being missing is the same for all the observations. When data is MCAR, there is absolutely no relationship between the data missing and any other values, observed or missing, within the dataset. In other words, those missing data points are a random subset of the data.
There is nothing systematic going on that makes some data more likely to be missing than other.
### Missing Data Not At Random(MNAR): Systematic missing Values
There is absolutely some relationship between the data missing and any other values, observed or missing, within the dataset.
### Missing At Random(MAR)
#### Mean/ MEdian /Mode imputation
Mean/median imputation has the assumption that the data are missing completely at random(MCAR).
We solve this by replacing the NAN with the most frequent occurance of the variables
##### Advantages
Easy to implement(Robust to outliers)
Faster way to obtain the complete dataset
##### Disadvantages
Change or Distortion in the original variance
Impacts Correlation
#### Random Sample Imputation
Aim: Random sample imputation consists of taking random observation from the dataset and we use this observation to replace the nan values
When should it be used? It assumes that the data are missing completely at random(MCAR)
##### Advantages
Easy To implement
There is less distortion in variance
##### Disadvantage
Every situation randomness wont work
#### Capturing NAN values with a new feature
It works well if the data are not missing completely at random
##### Advantages
Easy to implement
Captures the importance of missing values
##### Disadvantages
Creating Additional Features(Curse of Dimensionality)
#### Arbitrary Value Imputation
This technique was derived from kaggle competition It consists of replacing NAN by an arbitrary value.
##### Advantages
Easy to implement
Captures the importance of missingess if there is one
##### Disadvantages
Distorts the original distribution of the variable
If missingess is not important, it may mask the predictive power of the original variable by distorting its distribution
Hard to decide which value to use
### How To Handle Categroical Missing Values
#### Frequent Category Imputation
##### Compute the frequency with every feature
##### Advantages
Easy To implement
Fater way to implement
##### Disadvantages
Since we are using the more frequent labels, it may use them in an over respresented way, if there are many nan's
It distorts the relation of the most frequent label
#### Adding a variable to capture NAN
