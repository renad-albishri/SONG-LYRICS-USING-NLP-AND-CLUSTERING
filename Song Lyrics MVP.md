# Song Lyrics Using NLP and Clustering MVP

### 
#### Goal of the project
The main focus of this project is break down and analyze the under meaning of song lyrics using Natrual Langauge Processing and Clustering as part of 
machine learning algorithms and to devide them into topics for further investigation.

#### Exploratory data analysis
After performing the initial EDA which included:
1. Checked for missing values (doesn't have null values).
2. Checked for duplicates and removed them.
3. Drew EDA visiualizations for better understanding of the data.
4. Chose a sample of 20,000 documents.
5. Limitted to English songs.
6. Introduced a new column to the dataset called **'Length'** that calculates the number of characters per song.
7. Limitted to songs that have more than 20 characters.
8. Romoved unneeded columns.

#### Natrual Langauge Processing
The NLP process included:
1. Performed text cleaning
  - Tokenization.
  - Vectorization
  - Lemmatization.
  - Removed digits from texts.
  - Made all text lowercase.
  - Added to the original stop words (that fitted along with songs).
  - Got rid of all non-english characters.
  - Removed all punctuations.
2. NLP Models:
   4 topics were chosen for each model **(Reality, Relationship, Home and Desire)**
  - NMF. 
  - LSA.
  - LDA.
  
The number of columns and rows before cleaning & NLP were **5 and 209,523**
After cleaning up the data the number of columns and rows are **3 and 20,000**
After NLP the data the number of columns and rows are **36,000 and 4**


#### Classification
Two classification models were built:
Given the fact that 4 classes (topics) were established, the OnevsRest model was used.
1. Logistic Regression.
 - **Score for Training:** 1
 - **Score for Validation:** 0.937
 - **Score for f1:** 0 -> 0.94 , 1 -> 0.93 , 2 -> 0.94 , 3 -> 0.93
 - **Score for Accurecy:** 0.94
 - **Score for Precision:** 0 -> 0.94 , 1 -> 0.93 , 2 -> 0.94 , 3 -> 0.93
 - **Score for Recall:** 0 -> 0.95 , 1 -> 0.93 , 2 -> 0.93 , 3 -> 0.92

3. Multinomial.
 - **Score for Training:** 0.894
 - **Score for Validation:** 0.766
 - **Score for f1:** 0 -> 0.82 , 1 -> 0.59 , 2 -> 0.77 , 3 -> 0.70
 - **Score for Accurecy:** 0.77
 - **Score for Precision:** 0 -> 0.78 , 1 -> 0.76 , 2 -> 0.79 , 3 -> 0.70
 - **Score for Recall:** 0 -> 0.86 , 1 -> 0.48 , 2 -> 0.76 , 3 -> 0.69
Logistic Regression was chosen for further classification of topics. 
<br><br>

<img src="https://github.com/renad-albishri/SONG-LYRICS-USING-NLP-AND-CLUSTERING/blob/main/images/word%20frequency%20per%20topic.png" width="800"/><br>

As shown in the figure above, the topics were devided into **4** . And these are the most common words in each topic. For example. in **Relationship topic** the word 
_dear_ is the most freuquent word.

#### Futrue Work
- Introducing clustering into the project.






