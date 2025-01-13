### **NLP Ham or Spam Classifier**  
The **NLP Ham or Spam Classifier** is a machine learning project aimed at automating the categorization of SMS messages into "ham" (legitimate) or "spam" (unwanted). This project demonstrates the integration of data preprocessing, feature engineering, and supervised learning to solve a real-world problem in text classification.

---

### **Objective**  
To develop a robust machine learning model capable of distinguishing between spam and ham messages based on textual content, aiding in automated communication filtering systems.

---

### **Dataset Overview**  
- **Dataset**: The project utilized a publicly available dataset consisting of **5,572 SMS messages**, labeled as "ham" or "spam."  
- **Structure**: Each record included:  
  - `Label`: The classification ("ham" or "spam").  
  - `Message`: The SMS text content.  

---

### **Steps Involved**  

#### **1. Data Exploration**  
- Conducted an initial analysis of the dataset using **Pandas** to understand its structure, size, and content distribution.  
- Explored the imbalance between classes (`ham`: 4,825 messages, `spam`: 747 messages).  
- Generated basic statistics on message lengths to identify potential differences between spam and ham texts.

#### **2. Text Preprocessing**  
Prepared the raw SMS messages for analysis using a series of text-cleaning steps:  
1. **Tokenization**: Split each message into individual words or tokens.  
2. **Punctuation Removal**: Removed special characters to focus on meaningful words.  
3. **Stopword Removal**: Eliminated common words like "and," "the," and "is" using the **NLTK stopword list**, as they don't contribute to spam/ham classification.  
4. **Lowercasing**: Converted all text to lowercase to maintain uniformity.

#### **3. Feature Engineering**  
- **Message Length**: Extracted and analyzed message lengths, observing that spam messages tend to be longer than ham messages.  
- **Bag-of-Words (BoW)**: Transformed text data into a numerical matrix representing word occurrences.  
- **TF-IDF Vectorization**: Applied Term Frequency-Inverse Document Frequency to weigh words based on their importance within and across messages.

#### **4. Model Building**  
- Selected **Multinomial Naive Bayes**, a probabilistic algorithm well-suited for text classification tasks.  
- Divided the dataset into training and testing sets using an **80-20 split** to evaluate the model’s performance.  

#### **5. Pipeline Creation**  
- Built a **scikit-learn Pipeline** to automate the sequence of data preprocessing, feature extraction, and model training steps, ensuring scalability and consistency for new datasets.

---

### **Evaluation and Results**  
- **Metrics Used**: Precision, recall, F1-score, and accuracy.  
- Achieved an overall accuracy of **96%** on the test set, with a precision of **100%** for spam detection.  
- Detailed breakdown:  
  - **Ham**: High recall (1.00), ensuring legitimate messages are rarely misclassified.  
  - **Spam**: Precision of 1.00 indicated no false positives (legitimate messages misclassified as spam).

---

### **Visualization and Insights**  
- Used **Matplotlib** and **Seaborn** for data visualization:  
  - Histogram of message lengths showed clear differences between ham and spam texts.  
  - Plotted message length distributions by class to identify it as a useful feature for classification.  

---

### **Technical Stack**  
- **Languages**: Python  
- **Libraries**: NLTK, Pandas, Matplotlib, Seaborn, scikit-learn  
- **Techniques**: Text preprocessing, feature engineering (BoW, TF-IDF), supervised learning (Naive Bayes), pipeline creation  

---

### **Impact and Applications**  
This project showcases the practical application of Natural Language Processing and machine learning in detecting spam messages. It is highly scalable and can be extended to filter email spam, detect phishing content, or moderate online platforms.  

