# 🇸🇦 **Arabic Dialect + Code-Switching Detection with Socio-Linguistic Profiling**

Links to notebooks in collab
1. https://colab.research.google.com/drive/1GYkX0gQwDUnY2lxECQXI685pT1eu7gID?usp=sharing
2. https://colab.research.google.com/drive/11Dmsw0s8n1zJw3NaoJhMv39jF1ZsA0Gh?usp=sharing
3. https://colab.research.google.com/drive/1SwselmPfy6B4viQjcHz_IT29PlveRPn1?usp=sharing
4. https://colab.research.google.com/drive/10Xi2UpzW-zfZo_Vivqrh_RfbuVF2VeEe?usp=sharing

**Vision 2030 Alignment**: *Digital Transformation, Cultural Identity, AI in Government & Media*
**Project Description**:

* **Code-switching detection** (English-Arabic mix common on social media).
* Building a **socio-linguistic profiler** to infer speaker’s region.
* Fine-tune Arabic CAMeLBERT model

**Why It Stands Out**:

* Enhances NLP capabilities in a **low-resource language** region.
* Useful for **public sentiment monitoring, e-government tools, and media analysis**.
* Shows understanding of **cultural nuances**, which non-Arab developers often overlook.
* Very few global ML experts specialize in Arabic dialect NLP. Adding code-switching and socio-linguistic profiling (region/age/emotion) is novel.

---



🔬 Projected Research-Driven Goals

Use self-supervised pretraining on dialectal Arabic (e.g., contrastive learning, SimCLR-style), or fine-tune LLMs on Twitter or TikTok comments to detect dialect/emotion/code-switch boundaries.

---

## 🔠 1) Arabic Dialect + Code-Switching Profiler

### 🎯 Objective:

Build a model that:

* Detects Arabic dialects (Gulf, Egyptian, Levantine, etc.)
* Detects **code-switching** between English and Arabic

---

### 📚 Research Papers

Will start with these for grounding and architecture inspiration:

1. **[MARBERT: Pretraining BERT on Arabic Tweets](https://aclanthology.org/2021.acl-long.551.pdf)**

   * Focused on dialectal Arabic.
2. **[CAMeL Tools](https://aclanthology.org/2020.lrec-1.868v2.pdf)**

   * Toolkit for Arabic NLP, including dialect identification.
3. **[AraBERTv2: Arabic BERT](https://arxiv.org/abs/2003.00104v2)**

   * Standard Arabic and dialect support.
4. **[Fine-grained Arabic Dialect Identification](https://aclanthology.org/W19-4622.pdf)**

   * Dataset and task focused on multi-dialect detection.

---

### 📊 Datasets

These are freely available and used in prior research:

| Dataset                                          | Description                                                 | Link                                                                     |
| ------------------------------------------------ | ----------------------------------------------------------- | ------------------------------------------------------------------------ |
| **ADI / MADAR**                                  | Multilingual Arabic Dialect Identification across 25 cities | [MADAR](https://sites.google.com/nyu.edu/madar/)                              |


> 💡 If none have code-switching annotations: build my own from Twitter using regex + langdetect (Arabic vs English tokens) for weak supervision.

---

### 🧠 Baseline Models

* Naive-Bayes, SVM, Logistic Regression models
* Token-level classification via BiLSTM and CNN models

### ⭐ State of the Art Models

* `CAMeBERT` (via Hugging Face)
---

### 🛠 Tools

* Hugging Face Transformers (`AutoModelForSequenceClassification`)
* TensorFlow and PyTorch for model creation, training, and inference
* CAMeL Tools for morphological features
* `stanza` and `nltk` for preprocessing
