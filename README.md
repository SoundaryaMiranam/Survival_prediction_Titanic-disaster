# Survival_prediction_Titanic-disaster
About: From the kaggle dataset: https://www.kaggle.com/c/titanic

The sinking of the Titanic is one of the most infamous shipwrecks in history.On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew. While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

# Column details:

PassengerId: Unique Passenger ID

survived: Survival (0 = No; 1 = Yes)

Pclass: Passenger Class (1 = 1st; 2 = 2nd; 3 = 3rd)

Name: name

Sex: sex

Age: age

sibsp: Number of siblings/spouses aboard

parch: Number of parents/children aboard

Ticket: Unique ticket ID number of the passenger

Fare: Passenger fare (British pound)

embarked: Port of embarkation (C = Cherbourg; Q = Queenstown; S = Southampton)

# Purpose: 
To create a model that predicts which passengers survived the Titanic shipwreck.

# Exploratory Data Analysis:

Data visualization:

1. Few people have survived when compared to non-survived.

2. Trend shows that more females survived than males.

3. Passengers belonging to class 3 died the most.

4. Maximum people didn't have siblings and spouse along with them which is denoted with 0 value.Value 1, nearly 200 people were traveling with spouse.

5. People have 0 parents or children on board are not likely to survive.

6. People embarked from Southampton (S) are not likely to survive.

Data cleaning:

1. Passenger class and age are 36% related to each other.So, use Pclass to find the average age of the people.

2. Drop the cabin column as there are many missing values in it.

Data Processing:

1. Label Encoding for Embarked based on uniques values.

2. Create dummies for Sex column (male,female).

3. Combine SibSp and Parch as FamilySize and then to Isalone or not category.

4. Create bin for Age features['Children','Teenage','Adult','Elder'].

5. Create new feature based on Name feature by replace many titles with a more common name or classify them as Rare and then convert the categorical titles.

# Machine Learning:

The LogisticRegression model gave an accurate on the training data was of 76.40 %.Further feature engineering techniques are required to apply on it.

