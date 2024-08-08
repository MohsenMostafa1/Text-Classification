# Text-Classification


<figure>
        <img src="https://thepythoncode.com/media/articles/text-classification-using-tensorflow-in-python.PNG" alt ="Audio Art" style='width:800px;height:500px;'>
        <figcaption>


Text Classification is a fundamental task in Natural Language Processing (NLP) that involves categorizing text into predefined classes. This task is crucial in applications such as sentiment analysis, spam detection, and topic categorization. Text classification typically involves preprocessing text data, encoding it into a numerical format, and then using machine learning models to predict the class of the text.

Key Components of Text Classification:

Text Preprocessing: Involves cleaning and preparing text data for model input, including tokenization, removing stopwords, and stemming or lemmatization.
Text Encoding: Converting text into numerical representations. Common methods include one-hot encoding, word embeddings, and subword tokenization.
Modeling: Using machine learning models like logistic regression, SVM, or deep learning models like LSTMs, CNNs, or Transformers to classify the text.
Evaluation: Assessing the model's performance using metrics like accuracy, precision, recall, F1-score, and confusion matrices.

The goal of this task was to perform sentiment analysis on a subset of the IMDB dataset using three different text encoding methods: byte-level encoding, subword encoding with an 8k vocabulary, and subword encoding with a 32k vocabulary. The task involved preprocessing the data, building and training models, and evaluating their performance.

Data Source:
The data was fetched from a specific URL providing a small subset (100 samples) of the IMDB dataset in plain text format.

Text Encoding Methods Used:

Byte-level Encoding: Encodes each character in the text as a sequence of bytes. This method is simple but does not capture semantic information as effectively as subword or word-level encodings.
Subword Encoding (8k vocabulary): A more sophisticated encoding method that splits words into subword units, with a vocabulary size of 8,000. This method balances between capturing semantic information and managing vocabulary size.
Subword Encoding (32k vocabulary): Similar to the 8k vocabulary method but with a larger vocabulary size of 32,000, potentially capturing more nuanced semantic information.

Model Architecture:
A simple deep learning model was built using TensorFlow, consisting of:

An embedding layer to map the encoded text into dense vectors.
A convolutional layer to capture local patterns.
An LSTM layer to capture sequential dependencies.
Dense layers for the final classification.

Evaluation:
The models were evaluated on a validation set, with metrics such as accuracy, precision, recall, and F1-score. Additionally, training and validation accuracy and loss were plotted to visualize the model performance.
Report on the Task

1. Data Handling:

Successfully extracted and processed the text data from the provided URL.
Three different encoding strategies were applied to the text data, each with its strengths and weaknesses.

2. Model Performance:

Byte-level Encoding: The model achieved decent performance but was somewhat limited in capturing the semantic richness of the text.
Subword Encoding (8k vocabulary): Showed improved performance compared to byte-level encoding, as it could better capture semantic patterns in the text.
Subword Encoding (32k vocabulary): Provided the best performance among the three, indicating that a larger vocabulary size helped in better understanding the text.

3. Evaluation Metrics:

Accuracy: All three models performed relatively well, with the 32k subword model slightly outperforming the others.
Precision, Recall, and F1-score: The classification reports provided detailed insights, showing that the subword models generally offered a better balance between precision and recall compared to the byte-level model.
