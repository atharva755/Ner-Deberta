Named Entity Recognition using DeBERTa (Hugging Face)

This project implements a powerful Named Entity Recognition (NER) model using the DeBERTa transformer architecture from Hugging Face. It is designed to extract entities such as names, locations, dates, and organizations from raw text using a custom BIO-labeled dataset.

---

📌 Features

- ✅ Fine-tuning DeBERTa for NER tasks
- ✅ Custom BIO-format dataset
- ✅ Evaluation using `seqeval` metrics
- ✅ Prediction script with clean token-label display
- ✅ Easily modifiable for other transformer models

---
 📁 Directory Structure

```
NER-DeBERTa-NER/
├── data/
│   └── trainmegadata.txt         # BIO formatted training data
├── models/
│   └── ner_model/                # Saved fine-tuned model
├── train_ner_deberta.ipynb       # Jupyter notebook for training
├── predict ner.ipynb             # Jupyter notebook for inference
├── README.md                     # Project description and usage
├── requirements.txt              # List of required libraries
└── .gitignore                    # Ignore unnecessary files
```

---

⚙️ Installation

Make sure you have Python 3.8+ installed. Then install the required libraries:

```bash
pip install -r requirements.txt
```

`requirements.txt` (example content)

```
transformers
datasets
seqeval
torch
scikit-learn
```

---

🏋️‍♂️ Training the Model

Open `train_ner_deberta.ipynb` and run all cells. The notebook will:

- Load your custom BIO dataset
- Tokenize the data
- Fine-tune DeBERTa on your dataset
- Save the model to `./models/ner_model/`

---

🔍 Using the Model for Inference

Open `predict ner.ipynb` and:

- Load your trained model and tokenizer
- Input a sample text
- See the extracted entities in a clear token-label format

---

📝 Example

 Input:
```
Sachin Tendulkar was born in Mumbai on 24th April 1973.
```

 Output:
```
[('Sachin', 'B-PER'), ('Tendulkar', 'I-PER'), ('Mumbai', 'B-LOC'), ('24th', 'B-DATE'), ('April', 'I-DATE'), ('1973', 'I-DATE')]
```

---

 📄 License

This project is licensed under the **MIT License**. Feel free to use and modify it for your own work!

---

 🙌 Acknowledgments

- Hugging Face Transformers
- DeBERTa Model
- Seqeval

---

👤 Author

Atharva Godse  
MSc Data Science & Big Data Analytics
