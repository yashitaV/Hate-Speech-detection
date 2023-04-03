# Hate-Speech-detection:
This project is designed to detect hate speech and classify tweets based on sentiment analysis. The project includes data preprocessing techniques to clean and normalize the data, as well as several machine learning models for classification.

### Description of Dataset
Dataset comprises of three columns : id, label and tweet, each with 10,575 row entries. “Id” is of integer datatype which gives id assigned to a particular tweet and label. Given a training sample of tweets and labels, label ’1’ denotes the hate tweet and label ’0’ denotes the non-hate tweet. Label are of integer datatype and tweets are of object type. Full tweet texts are provided with their labels for training data. Mentioned users’ username is replaced with @user.

### Preprocessing
For better analysis, I originally began by processing the data using natural language processing. I developed a preprocessing function for data processing (tweet) that performs the following functions:
  1. Lowercase letters for all uppercase letters.
  2. Regex-based removal of URLs and hashtags
  3. Eliminating all punctuation.
  4. By tokenizing the tweets and subsequently filtering them,
  all stop words in the English language are eliminated.
  5. Eliminating duplicate records
  
### Visualization :
To explore the data, I observed the distribution of sentiments by plotting a pie-chart showing the percentage of both the labels (hate tweet and non-hate  tweet) additionally I created a two different word clouds, each for hate tweets and non-hate tweets in order to take a look on which words are more frequently used in each type of tweets

### Model Building: 
Preparing the data - I divided the data into X and Y where X is the vector transformed tweet and Y is corresponding label of that tweet. The data is then splitted into 20% test data and 80% training data using train test split() from sklearn.model selection library.
Since the data is categorical and we are working on a classification problem, I used following classification Machine learning models:
  1. Logistic regression
  2. Random forest
  3. Naive Bayes
  4. SVM 
  5. XGBoost 
  
### Results:
By comparing the accuracies of all the models I concluded that XGBoost performed the best. Further, after implementing hyperparameter tuning, Random forest performed better.

### Usage:
The jupyter notebook and the .csv file can be found in **ML project source code** and data folder
