
# TransBioRetro  
*A Transformer-based Self-Correcting Beam Search for Bio Retrosynthesis*

---

## 📘 Project Overview

**TransBioRetro** is a hybrid deep learning framework designed to predict viable biosynthetic pathways for target molecules using AI-driven retrosynthetic reasoning. Combining a transformer-based architecture with contrastive learning and a novel self-correcting beam search, this model addresses limitations in traditional organic retrosynthesis by incorporating enzymatic and natural reaction pathways.

This project was developed as a final-year major project under the **Department of Artificial Intelligence and Machine Learning** at **SIES Graduate School of Technology**.

---

## 👥 Contributors

- **Pranav Pillai** – [ppillai294@gmail.com](mailto:ppillai294@gmail.com)  
- **Suyash Utekar** – [suyashutekar130707@gmail.com](mailto:suyashutekar130707@gmail.com)  
- **Aditya Randive** – [adityaran1405@gmail.com](mailto:adityaran1405@gmail.com)

---

## 📁 Project Structure

```
TransBioRetro/
│
├── notebook.ipynb                 # Main Jupyter Notebook for model training and testing
├── model.zip                      # Final trained model weights
├── dataset/                       # Dataset folder containing curated biosynthetic data
│   ├── biosynthetic_reactions.csv
│   └── uspto_organic_reactions.csv
├── src/                           # Source code for model, tokenizer, and beam search
│   ├── model.py
│   ├── tokenizer.py
│   ├── beam_search.py
│   └── utils.py
├── requirements.txt               # Project dependencies
└── README.md                      # Project documentation
```

---

## 🚀 Features

- Transformer-based sequence-to-sequence model for SMILES prediction
- Enhanced with **contrastive learning** using NT-Xent loss
- Introduces **self-correcting beam search** to dynamically rerank predictions
- Recursive **multi-step retrosynthesis strategy** with chemical filtering
- Trained on combined biosynthetic and organic datasets from KEGG, MetaCyc, MetaNetX, USPTO-NPL

---

## 🧬 Dataset Details

The dataset used consists of:
- **Biosynthetic Reactions**: From KEGG, MetaCyc, MetaNetX, BRENDA
- **Organic Reactions**: From USPTO-NPL repository

### Preprocessing Includes:
- SMILES standardization and tokenization
- Stereochemical information preservation
- Atom-mapping with RXNMapper
- Reaction type tagging (〈B〉 for biosynthetic, 〈C〉 for chemical)

---

## ⚙️ Setup Instructions

1. **Clone the repository**:

```bash
git clone https://github.com/your-username/TransBioRetro.git
cd TransBioRetro
```

2. **Create and activate a virtual environment**:

```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. **Install required dependencies**:

```bash
pip install -r requirements.txt
```

---

## 🧪 Running the Model

Launch the Jupyter notebook:

```bash
jupyter notebook notebook.ipynb
```

Follow the cells step-by-step to:
- Load the dataset
- Tokenize and prepare SMILES sequences
- Train or load the model
- Predict retrosynthetic pathways

---

## 📊 Evaluation Results



### 🔹 Multi-Step Retrosynthesis Pathway

Visualizes recursive breakdown of the target molecule into known bio-building blocks.

![image](https://github.com/user-attachments/assets/faf81359-a8be-4ebe-9227-e2ff33f16c03)
![image](https://github.com/user-attachments/assets/dfeda3e1-2dbb-4474-a4be-a41fd3e345b5)
![image](https://github.com/user-attachments/assets/ea7fb4d0-f6d6-49ae-a7a5-54d4a97c7eba)
![image](https://github.com/user-attachments/assets/96878970-854e-4c24-895f-dfff07da3379)


---

## 🔮 Future Scope

- Expand dataset diversity and include real-time experimental feedback
- Incorporate 3D stereochemical information and molecular dynamics
- Deploy as a web-based synthesis planning tool
- Apply to pharmaceutical R&D, green chemistry, and biofuel synthesis

---

## 📚 References

Key papers and sources used:
- Schwaller et al. (2019), *Molecular Transformer*, ACS Central Science
- Zheng et al. (2020), *Self-correcting Transformers for Retrosynthesis*
- Dong et al. (2021), *Retrosynthesis Planning: Datasets and Models*
- Koch et al. (2020), *Reinforcement Learning for Bioretrosynthesis*

Refer to the complete bibliography in `TransBioRetro_MajorProject_Report_final.pdf`.

---

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---
