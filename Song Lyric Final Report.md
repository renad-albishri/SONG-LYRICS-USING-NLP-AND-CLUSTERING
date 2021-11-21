# Song Lyrics Using NLP and Clustering Final Report
## Abstract
The main focus of this project is break down and analyze the under meaning of song lyrics using Natrual Langauge Processing and Clustering 
as part of machine learning algorithms and to devide them into topics for further investigation..

## Data Description
The chosen dataset is from [Kaggle](https://www.kaggle.com/neisse/scrapped-lyrics-from-6-genres?select=lyrics-data.csv) which contains two seperate dataset
one is meant for the artists and the other one is for the song lyrics which is the main point of this project's intrest.<br>
The data includes songs from 6 different genres of all time:
- Rock
- Hip Hop
- Pop music
- Sertanejo (Basically the Brazilian version of Country Music)
- Funk Carioca (Originated 60s US Funk, a completely different genre in Brazil nowadays)
- Samba (Typical Brazilian music)

The whole data contains up to **209,523** rows and **5** columns. But all non-english songs will be excluded which leaves the new dataset with
**114,723** rows and **5** columns.
## Algorithms
1. Exploratory Data Analysis was done to the dataset.
  - Cleaning
    - Checked for missing values (doesn't have null values).
    - Checked for duplicates and removed them.
    - Drew EDA visiualizations for better understanding of the data.
    - Chose a sample of 20,000 documents.
    - Limitted to English songs.
    - Introduced a new column to the dataset called **'Length'** that calculates the number of characters per song.
    - Limitted to songs that have more than 20 characters.
    - Romoved unneeded columns.
  - Visualization
  - Merging 2 datasets
    - one about Lyrics and another one about Artists
2. Natural Language Processing
 - Text Cleaning
   - Tokenization.
   - Vectorization
   - Lemmatization.
   - Removed digits from texts.
   - Made all text lowercase.
   - Added to the original stop words (that fitted along with songs).
   - Got rid of all non-english characters.
   - Removed all punctuations.
 - Topic Modeling
   - 6 Topics were chosen for each model **(Reality, Friendship, Home , Coming of age/Growing up , Heartbreak and Desire)**
   - Non-Negative Matrix Factorization (NMF).
   - Latent Semantic Analysis (LSA).
   - Latent Dirichlet Allocation (LDA).
 - Scatter Text
   - We have 6 topics but here in Scatter Text we choose 2 topics to perform scatter text on it ,which is ( Coming of age/Growing up ,Reality )
 - Corex
3. Classification 
   - 5 classification models were built:
   - Models | Training score | Validation score
     ------ | ---------------| ----------------
     LogisticRegression  | 0.9945 | 0.9271
     DecisionTreeClassifier  | 1.0 | 0.7895
     RandomForestClassifier | 1.0 | 0.8667
     GradientBoosting | 0.9282 | 0.81130
     MultinomialNB | 0.8658 | 0.6649 
     
     as we see, LogisticRegression model gives us the highest score in both training and validation **0.9945**, and ** 0.9271** respectively;
     so we choose it so we need to calculates the Accuracy ,Test Score and The Error Rate
     
     Models | Test Score | Accuracy | Error Rate
     ------- | -----------| ---------| ----------
     LogisticRegression | 0.9271 | 0.93 | 0.0728
     
 4. Clustering
   -  We calculates the inertia for 1 to 10 clusters, and we plot the inertia to determine what the optimium number of clusters.
      the optimium number of clusters is **5**
   - PCA to easily visualize clustering 
   - DBSCAN 
   - TSNE 
   
## Tools
Here the basic tools that will be used: <br/>
Technologies: python, and Jupyter Notebook with python libraries:
- For Exploratory Data Analysis:
  - pandas
  - matplotlib
  - numpy
  - seaborn
- For Natrual Language Processing:
  - scikit-learn
  - NLTK
  - Regular Expression
  - WordCloud
  - Gensim
  - Corextopic
  - ScatterText
- For Clustering:
  - K-means
  - Scipy
- For Saving
  - Pickle 
  - Sqlite3
  
## Conclusion
The major goal of this project is to break down and evaluate the hidden meanings of song lyrics using natural language processing and clustering as part of machine learning techniques, and then divide them into topics for further research.
