# Hotel Receptionist Chatbot

## Project Description:
An AI based chatbot that provides hotel reception services to the customers. The chatbot is trained using a particular dataset. Feed-forward neural network is used to train
the chatbot. Natural Language Toolkit (NLTK) is used to tokenize, stemming and bag-of-word creation, which helps as data/text preprocessing. Chatbot provides appropriate information to the customers for relevant queries, after being trained. This chatbot can be transformed for any arbitrary purpose just by altering the dataset.

## Tools:
1. Programming Language: Python
2. Dataset Format: JSON
3. Machine Learning Library: PyTorch
4. Natural Language Toolkit (NLTK)

## Project Details:
* **Dataset**: "intent.json" file contains the dataset to train the model on. Every intent has a specific tag like 'greetings' or 'goodbye'. Each tag has several patterns which 
invoke that particular intent. Several responses are also associated with each intents. Based on these patterns a random respond will selected by the bot.
* **Data/Text Preprocessing**: "nltk_utils.py" file preprocess the dataset using Natural Language Toolkit (NLTK). Tokenize method takes a phrase and return a list of words from 
the phrase. Stemming method stems each words i.e. "organisation" is stemmed as "organ". Bag of word method returns a boolean list that provides information on whether a given 
list of tokenized sentence's words are available on a given list of words or not.
* **Model**: "model.py" file uses PyTorch library to build a feed-forword neural network model with 1 hiddel layer. ReLU is used as an activation function. Width and depth of 
the model are also provided.
* **Training**: "train.py" file trains the model. First, it preprocess the dataset using "nltk_util.py" methods. Later, hyperparameters like number of epochs, learning rate etc
are determined here. Based on the hyperparameters model is trained on CPU or GPU (depending on the availability) using PyTorch. Training progress and results are shown in
console. After training state of the model is saved on "data.pth" file. 
* **Chat**: "chat.py" is the main class for our chatbot. It loads the current trained state of our chatbot model. It greets the user and chat is begun. Until user type "quit" 
chat will continue. For any irrelevant queries, bot will respond with "I do not understand message". For 3 consecutive failed attempt of conversation it'll provide user with 
direct communication information of the organisation.

## Instructions to run the codes: 
1. Install python environment (e.g. conda or venv) 
2. Install pytorch according to your environment from https://pytorch.org 
3. Install nltk by running the command "pip install nltk" in the terminal 
4. Uncomment "# nltk.download('punkt') " once, for first time running nltk_utils.py.  

## Reference: 
1. https://www.nltk.org 
2. https://pytorch.org
3. https://python-engineer.com

## Youtube unlisted video link:
* https://www.youtube.com/watch?v=j_hWKBWLufc
