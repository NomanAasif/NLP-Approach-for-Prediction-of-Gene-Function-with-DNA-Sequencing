# NLP Approach for Prediction of Gene Function with DNA Sequencing using Python

In this Project, I applied a classification model with Machine Learning, that can predict a gene’s function based on the DNA sequencing of the coding sequence alone. The flow of steps used in the creation of this project are as follows.

# 1. Importing required packages and libraries.
Necessary packages and libraries of python are imported (installed if not present previously). The necessary packages for this project are:

i. Numpy - To perfor mathematical operations on the data.

ii. Pandas - To read the data from the dataset.

iii. Matplotlib - To visualize data after performing operations on it. Visualization includes bar chart, pie chart, histogram etc in general.

iv. SkLearn - To import the NLP tool "CountVectorizer".


# 2. DataSet
The dataset of this project is of text type. Data of human, dog and chimpanzee gene are collected as dataset. The data for human has human DNA sequence coding regions and a class labe. Similarly for Chimpanzee and the dog also. 

# 3. Data Pre-Processing
DNA sequence is treated as a “language”, otherwise known as k-mer counting. DNA and protein sequences can be viewed metaphorically as the language of life. The language encodes instructions as well as function for the molecules that are found in all life forms. Here hexamer “words” are used but that is arbitrary and word length can be tuned to suit the particular situation. The word length and amount of overlap need to be determined empirically for any given application. In genomics, we refer to these types of manipulations as “k-mer counting”, or counting the occurrences of each possible k-mer sequence. There are specialized tools for this, but the Python natural language processing tools make it super easy. 

Conversion of training data sequences into short overlapping k-mers of legth 6 is done in this stage. Same is done for each species of data we have using our getKmers function. The coding sequence data is changed to lowercase, split up into all possible k-mer words of length 6. Then, the conversion of the lists of k-mers for each gene into string sentences of words that the count vectorizer can use, is done.
          
 # 4. Visualizing the Dataset - Balanced
Upon the pre-processing of the data, the datset becomes relatively balanced than previous and hence will be compatible to perform the gene function prediction with better accuracy over it. This visualization is done using the Matplotlib library.
             
# 5. Splitting the data
The balanced dataset obtained above is splitted into train and test data so as to perform the training of the model over the training data and the testing data would be unkonwn for the model which helps in improving the accuracy of the model. 
              
# 6. Model Design
A multinomial naive Bayes classifier is created. Parameter tuning is done (previously) and found the ngram size of 4 (reflected in the Countvectorizer() instance) and a model alpha of 0.1 suits the model well.
     
# 7. Model Performance metrics
Here, 4 kinds of model performance metrics are involved. The metrics applied and the values obtained for them were as follows: 

i. Accuracy = 98.402 

ii. Precision = 98.429 

iii. Recall = 98.402 

iv. f1 score = 98.403
