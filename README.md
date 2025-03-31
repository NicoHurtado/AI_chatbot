# AI Chatbot with PyTorch and NLTK

A simple rule-based chatbot trained using PyTorch. It parses predefined intents from a JSON file, learns to classify them, and responds accordingly. Supports action mappings for intent-based function execution.

---

## 🧠 Features

- Intent classification via feedforward neural network (PyTorch).
- Text preprocessing with NLTK (tokenization + lemmatization).
- Bag-of-words model for feature vectorization.
- Function execution on intent match (optional).
- Model saving/loading support.

---

## 🚀 Installation

### 1. Clone this repo and navigate to the project:
```bash
git clone https://github.com/your-username/ai-chatbot
cd ai-chatbot
```

### 2. Create and activate a virtual environment (optional but recommended):
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install required packages:
```bash
pip install -r requirements.txt
```

### 4. Download necessary NLTK resources:
```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
```

---

## 📁 Project Structure

```
├── main.py                  # Main chatbot logic
├── intents.json             # Training data (user intents and responses)
├── chatbot_model.pth        # Trained model weights
├── dimensions.json          # Model input/output shape metadata
├── requirements.txt         # Dependencies
└── README.md                # Project info
```

---

## 🏁 Training the Model

Uncomment the training block in `main.py`:

```python
# assistant = ChatbotAssistant(...)
# assistant.parse_intents()
# assistant.prepare_data()
# assistant.train_model(batch_size=8, lr=0.001, epochs=100)
# assistant.save_model(...)
```

Then run:
```bash
python main.py
```

---

## 💬 Running the Chatbot

Comment out the training code and uncomment the inference block:

```python
assistant = ChatbotAssistant(...)
assistant.parse_intents()
assistant.load_model(...)
```

Then just run:
```bash
python main.py
```

Use `/quit` to exit the loop.

---

## 📌 Example `intents.json`

```json
{
  "intents": [
    {
      "tag": "greeting",
      "patterns": ["Hello", "Hi", "Hey"],
      "responses": ["Hi there!", "Hello!", "Hey!"]
    },
    {
      "tag": "goodbye",
      "patterns": ["Bye", "See you later"],
      "responses": ["Goodbye!", "See you soon!"]
    }
  ]
}
```

---

## 🔗 Dependencies

- `torch`
- `nltk`
- `numpy`

All are listed in `requirements.txt`.

---

## 📄 License

MIT License. Use freely for learning and educational projects.
