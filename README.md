# Chatbot-Intent-Classifier

A simple chatbot trainer using NLTK and TensorFlow for intent recognition and response generation.

---

## Features
- Natural Language Processing with NLTK
- Neural Network model using TensorFlow/Keras
- Intent classification using bag-of-words
- Stemming and tokenization
- JSON-based intent configuration
---

## Prerequisites
- Python 
- NLTK
- TensorFlow 
- NumPy
---

## Installation
1. Clone the repository:
```bash
git clone https://github.com/zain-ul-abideen-5036/Chatbot-Intent-Classifier
cd your-repo-name
```
2. Install dependencies
```
pip install nltk tensorflow numpy
```
3. Download NLTK data:
```
import nltk
nltk.download('punkt')
```
---

## File Structure
```
.
├── train.ipynb           # Training notebook
├── intents.json          # Intent patterns and responses
├── model.h5              # Trained model
├── labels.pkl            # Intent labels
└── README.md
```
---

## Usage
1. Prepare your ```intents.json``` file with patterns and responses:
```
{
  "intents": [
    {
      "tag": "greeting",
      "patterns": ["Hi", "Hello", "Hey"],
      "responses": ["Hello!", "Hi there!", "Greetings!"]
    }
  ]
}  
```
2. Run the training notebook:
```
jupyter notebook train.ipynb
```
3. The notebook will:
- Preprocess the data
- Train the neural network model
- Save the trained model and vocabulary files

---

## Model Architecture
```
model = Sequential([
    Dense(8, input_shape=(input_len,), activation='relu'),
    Dense(8, activation='relu'),
    Dense(output_len, activation='softmax')
])
```
---
## Training Details
- Optimizer: Adam
- Loss: Categorical Crossentropy
- Epochs: 1000
- Batch Size: 8
---
