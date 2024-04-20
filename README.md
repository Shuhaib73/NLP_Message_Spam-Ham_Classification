<p align="center" style="font-size: larger; font-weight: bold;">
  <strong>A Machine Learning Classifier for Mail/SMS Spam Detection using Natural Language Processing (NLP)</strong>
</p>

<p align="center">
  <img src='https://img.hotimg.com/Untitled-design-2.gif' width='500' height='250' />
</p>
You can access the web application[Message_Classifier] by following this link: https://


## <br>**➲ Project description**
In response to the escalating challenge of unwanted commercial bulk emails, or spam, which severely impacts email servers and user productivity,  I have developed a Spam-Ham Classification model. This model leverages machine learning and Natural Language Processing (NLP) techniques to effectively discern between legitimate and spam SMS messages. By accurately distinguishing between the two.

## <br>**➲ The Dataset**
The dataset consists of 5,572 entries and two columns:

* Label: This column indicates whether the message is classified as "ham" (legitimate) or "spam" (unwanted commercial bulk email).

* Message: This column contains the actual text content of the messages.

## <br>**➲ Reading and Exploring Dataset**
While reading data, we get data in the structured or unstructured format. A structured format has a well-defined pattern whereas unstructured data has no proper structure. In between the 2 structures, we have a semi-structured format which is a comparably better structured than unstructured format.

## <br>**➲ Data Pre-Processing**
Cleaning up text data is crucial for preparing it for analysis and machine learning tasks. This process involves several steps to enhance the quality and relevance of the text data. These steps typically include:


  **1. Removing Noise:**
  Eliminate irrelevant characters, symbols, or formatting that may not contribute to the analysis, such as special characters, punctuation, and HTML tags.
  
  **2. Tokenization:**
  Splitting the text into individual words or tokens to facilitate further analysis and feature extraction.
  
  **3. Removing Stopwords:**
  Filter out common words (e.g., "and", "the", "is") that do not carry significant meaning and are unlikely to contribute to the analysis.
  
  **4. Lowercasing:**
  Convert all text to lowercase to ensure uniformity and prevent redundancy in the analysis caused by different cases of the same word.
  
  **5. Stemming or Lemmatization:**
  Reduce words to their base or root form to consolidate variations of the same word and improve the accuracy of analysis.
  
  **6. Vectorizing:**
  Convert cleaned text data into numerical representations, typically using techniques like TF-IDF (Term Frequency-Inverse Document Frequency) or Bag-of-Words, 
  to enable machine learning algorithms to process the data effectively.

## <br>**➲ Exploratory Data Analysis (EDA)**
<details>
       <summary>
              <strong>​✒️<Click here to see :</strong> Distribution of Text Length in Messages
       </summary>
                     <p align='center'>
                            <img src='https://github.com/Shuhaib73/NLP_Message-Spam-Ham_Classification/blob/main/Text_Distribution.png' style='width: 70%;' />
                     </p>
</details>

<details>
       <summary>
              <strong>​✒️<Click here to see :</strong> Distribution of Text Length in Ham Messages
       </summary>
                     <p align='center'>
                            <img src='https://github.com/Shuhaib73/NLP_Message-Spam-Ham_Classification/blob/main/Ham_dirstribution.png' style='width: 70%;' />
                     </p>
</details>

<details>
       <summary>
              <strong>​✒️<Click here to see :</strong> Distribution of Text Length in Spam Messages
       </summary>
                     <p align='center'>
                            <img src='https://github.com/Shuhaib73/NLP_Message-Spam-Ham_Classification/blob/main/spam_distribution.png' style='width: 70%;' />
                     </p>
</details>

<details>
       <summary>
              <strong>​✒️<Click here to see :</strong> Distribution of Ham & Spam Messages in the Dataset
       </summary>
                     <p align='center'>
                            <img src='https://github.com/Shuhaib73/NLP_Message-Spam-Ham_Classification/blob/main/Ham_spam_dis.png' style='width: 50%;' />
                     </p>
</details>

<details>
       <summary>
              <strong>​✒️<Click here to see :</strong> WordCloud of Ham Message
       </summary>
                     <p align='center'>
                            <img src='https://github.com/Shuhaib73/NLP_Message-Spam-Ham_Classification/blob/main/ham_wordcloud.png' style='width: 70%;' />
                     </p>
</details>

<details>
       <summary>
              <strong>​✒️<Click here to see :</strong> WordCloud of Spam Message
       </summary>
                     <p align='center'>
                            <img src='https://github.com/Shuhaib73/NLP_Message-Spam-Ham_Classification/blob/main/spam_wordcloud.png' style='width: 70%;' />
                     </p>
</details>


## <br>**➲ Model Building**

In the model building phase, I've employed several machine learning algorithms to classify messages into spam or ham categories. The algorithms used include Logistic Regression, XGBoost, Multinomial Naive Bayes, Random Forest and SVC.

The process involved the following steps:

**Data Preparation:** *Preprocessed the text data by cleaning and vectorizing it, ensuring that it's in a suitable format for model training.*

**Model Training:** *Trained each of the selected algorithms on the preprocessed data. This involved splitting the dataset into training and testing sets, fitting the models to the training data, and evaluating their performance using the testing data.*

**Performance Evaluation:** *Assessed the performance of each model using various evaluation metrics such as accuracy, precision, recall, and F1-score. This step helped in determining which model performed best in classifying spam and ham messages.*

**Model Selection:** *Identified the Support Vector classifier as the best-performing model based on its superior performance compared to other algorithms.*

**Model Deployment:** *Deployed the SVC model for real-world use cases, enabling it to classify incoming Mail/SMS messages into spam or ham categories effectively.*

**Classification Report for Training and Testing**
<p align='center'>
      <img src='https://github.com/Shuhaib73/NLP_Message_Spam-Ham_Classification/blob/main/images/Report1.png' style='width: 58%;' />
</p>


**Confusion Matrix for Training and Testing**
<p align='center'>
      <img src='https://github.com/Shuhaib73/NLP_Message_Spam-Ham_Classification/blob/main/images/testing_cls1.png' style='width: 58%;' />
</p>


## <br>**➲ Conclusion:**

* **The Support Vector Machine classifier** demonstrates superior performance, achieving a high training accuracy of **99%** and a commendable testing accuracy of **98%**. Furthermore, its precision, recall, and F1-scores for both classes on both the training and testing datasets are consistently high, indicating robust performance across the board. Therefore, based on these evaluation metrics, we can confidently conclude that the SVC classifier outperforms other models and is the best choice for this classification task.*

**Classification Report**

-  The SVC model demonstrates excellent performance in classifying ham messages, achieving high precision, recall, and F1-score. However, it shows slightly lower recall for spam messages, indicating that there is room for improvement in identifying all spam messages correctly. Overall, with an accuracy of 98%, the SVC model effectively distinguishes between ham and spam messages, making it a reliable choice for spam detection tasks.

**Confusion Matrix**

- SVC model is performing well in correctly identifying ham messages (class 0), with 947 instances correctly classified as ham and none incorrectly classified as spam. However, for spam messages (class 1), there are 21 instances incorrectly classified as ham and 147 instances correctly classified as spam.

- From this confusion matrix, we can see that the model is not failing to identify spam messages correctly (i.e., it is not classifying ham as spam). Instead, it is missing some spam messages, leading to false negatives. The model is performing well in identifying ham messages.
