Colab Link - https://colab.research.google.com/drive/1UZBdI-DbiquuSMqZgV9k1btfAPdGGYi-?usp=sharing

![image](https://github.com/arizzaa13/Intent-Recognition-System-Development-/assets/78647475/8c9b23ec-b017-4b0d-accf-5b7aa09e51a0)
# Intent-Recognition-System-Development-
The primary goal of this project is to design and implement an intent recognition system capable of accurately understanding user intents conveyed through natural language input. The system should be able to classify user queries or commands into predefined categories or intents, enabling effective interaction between users and the system.

## ✔ To perform Intent Recognition, these are the steps:

### 🔳Import Libraries

### 🔳Data Collection

### 🔳Data Cleaning 
As We can’t directly process this data. First, we have to clean it, this usually includes, removing punctuation marks or anything which might produce unwanted results. This is also done to reduce number of tokens, as we don’t want to tokenize everything.

### 🔳Data Preprocessing
Next step is to preprocess the data to make it suitable for training a neural network. This usually involves tokenization, which means breaking down each input sentence into individual words or sub-words.
But firstly, we need to prepare data in a format {intent : text data}

### 🔳Tokenization and Embedding 
With our data prepared, we can utilize TensorFlow's built-in tokenizer to perform both tokenization and embedding efficiently.

### 🔳Feature Extraction
Neural networks require numerical representations of sentences to function. To achieve this, we perform feature extraction by mapping each word to its index and creating a matrix that corresponds to its category (intent).

### 🔳One-Hot Encoding
For Categorical Data, we apply One-Hot Encoding.

### 🔳Model Building
The initial step in building a model involves setting hyperparameters, which are predefined settings specified before model training. These include parameters such as the number of epochs, embedding dimensions, vocabulary size, and target length. Adjusting these parameters can enhance the model's performance.

Next, we define our neural network's architecture with TensorFlow. For intent recognition, recurrent neural networks (RNNs) and their variant, long short-term memory (LSTM) networks, are commonly used due to their ability to effectively process sequential data like sentences. Alternatively, pre-trained models such as BERT or GPT can be utilized for superior performance.

In this instance, we are implementing an RNN using the 'Sequential' model from TensorFlow's Keras API. This model includes an embedding layer, an LSTM layer for handling sequences, and two dense layers for classification. The model summary is shown below.

### 🔳Training
With the model architecture set up, we can begin training the network with our labeled dataset. During training, the model fine-tunes its internal parameters to reduce the discrepancy between its predicted intents and the actual intents in the training data. This process includes forward propagation, where the model generates predictions, and backward propagation, where the model's parameters are adjusted based on the prediction errors.
In this step, we train the model by fitting it to the padded sequences and their corresponding categorical sequences. The model fine-tunes its internal parameters to minimize the gap between its predicted intents and the actual intents in the training data. Training occurs over a defined number of epochs and may halt early if there is no improvement in loss after 4 consecutive epochs.

### 🔳Evaluate
To verify our model's performance, we test it with new, unseen data and their corresponding labels. By providing text inputs along with their intents, we evaluate the model's accuracy, a process known as model evaluation. This crucial step helps determine the model's accuracy and reveals if it is overfitting or underfitting.

### 🔳Predict
After completing the training, our model is ready to make predictions on new, unseen sentences. When provided with an input sentence, the model processes it using the parameters it has learned and generates a probability distribution across the potential intents. The intent with the highest probability is taken as the predicted intent.








