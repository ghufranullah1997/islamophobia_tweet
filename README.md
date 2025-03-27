# Islamophobic Tweet Detection Using Transfer Learning

This repository contains the implementation of a deep learning-based system to classify tweets as Islamophobic or not, using transfer learning techniques. The project focuses on enhancing hate speech detection capabilities—particularly Islamophobia—by leveraging the Universal Language Model Fine-tuning (ULMFiT) approach.


---

## 🧾 Overview

With the rise of social media platforms, the spread of hate speech—especially Islamophobic content—has become increasingly prevalent. Manual moderation is impractical at scale, highlighting the need for automated solutions. This project addresses that need through an NLP-based classification system.

---

## 📌 Problem Statement

Detecting hate speech specifically targeted toward Muslims requires a more nuanced classification than general offensive content detection. The complexity arises due to overlapping features with other types of toxicity and the broad context in which hate speech can appear.

---

## 📊 Dataset

- **Source**: Tweets collected using `SNScrape` between January 2021 and July 2021.
- **Hashtags Used**:
  - `#TripleTalaq`
  - `#PopulationControlBill`
  - `#UniformCivilCode`
  - `#IslamicTerrorism`
  - `#IslamicTerrorist`
- **Size**: 874 tweets
- **Annotation**: Manually labeled with support from the Department of Mass Communication into:
  - Islamophobic
  - Racist
  - Neither

---

## 🧠 Methodology

- **Model Used**: [ULMFiT (Universal Language Model Fine-tuning)](https://arxiv.org/abs/1801.06146)
- **Steps**:
  1. Language model fine-tuned on the dataset using Wikitext-103 as a base.
  2. Token normalization and mapping.
  3. Gradual unfreezing of layers.
  4. Discriminative learning rates applied for efficient learning.
  
This approach improves performance even on small datasets due to effective transfer learning.

---

## ✅ Results

- **Overall Accuracy**: 82%
- **F1-Score**:
  - Islamophobic: 0.81
  - Not Islamophobic: 0.82
- **Recall**:
  - Islamophobic: 73%
  - Not Islamophobic: 94%

The confusion matrix shows an even distribution, indicating balanced classification performance.


---

## 🛠️ Tech Stack

- Python
- FastAI
- ULMFiT
- SNScrape
- Jupyter Notebook

---

## 📚 References

- [Time Article on Hate Speech on Twitter](https://time.com/6080324/twitterhate-speech-penalties/)
- Z. Waseem and D. Hovy (2016), NAACL
- Gambäck & Sikdar (2017), Use of CNNs in Hate Speech Detection
- K. Shah et al. (2020), Comparative Study of ML Models in Text Classification


---

Feel free to open issues or pull requests to improve the project.
