# PathoIntern – Embeddings, Clustering & Vectorization Workshop Lab 9

## Team Members
- **Sumanth Reddy K**
- **Muthuraj Jayakumar**
- **Lohith Reddy Danda**

---

## Project Overview

This project presents a structured **Natural Language Processing (NLP)** workshop built around the **PathoIntern** domain.  
Instead of using a generic or transit-based assistant scenario, this notebook repositions the workflow around a **pathology-support and clinical triage inspired setting**, where modern text representation methods are applied to:

- semantic retrieval
- text vectorization
- embedding generation
- similarity analysis
- clustering
- dimensionality reduction

The notebook demonstrates how raw textual information can be transformed into meaningful numerical representations using both **classical NLP methods** and **modern embedding-based approaches**.

---

## Repository Link

```bash
https://github.com/Lohithreddy29/Embeddings-Clustering-Vectorization-Workshop-Lab9.git
````

---

## Why This Project Matters

Raw text cannot be directly used by machine learning algorithms.
Before a system can compare, retrieve, cluster, or interpret textual content, the text must first be transformed into a structured numerical format.

This project matters because it demonstrates that workflow clearly, systematically, and in a domain-specific setting.

The notebook shows how text can move through the following pipeline:

**raw text → preprocessing → vectorization → embeddings → similarity → clustering → interpretation**

That makes this project relevant not only for coursework, but also for real NLP applications such as:

* semantic search
* intelligent assistants
* question-answer retrieval
* clinical text grouping
* recommendation systems
* vector database preparation

---

## Core Learning Objectives

This workshop is designed to help the learner:

* understand **Bag-of-Words** vectorization
* understand **TF-IDF** weighting
* explore **Word2Vec** semantic embeddings
* integrate **GloVe 6B** pre-trained embeddings
* use **OpenAI embeddings** for modern semantic retrieval workflows
* compare representation methods using **cosine similarity**
* apply **K-Means clustering** to discover semantic groups
* visualize hidden structure using **PCA** and **t-SNE**
* understand how representation quality affects intelligent assistant behavior

---

## PathoIntern Context

The entire notebook is framed around **PathoIntern**, a pathology-oriented assistant concept.

Rather than using toy examples, the project uses a **synthetic domain-specific corpus** inspired by pathology support and clinical workflow scenarios. This allows the notebook to demonstrate how NLP methods can support:

* pathology workflow assistance
* semantic grouping of clinically relevant prompts
* intelligent question-answer matching
* retrieval of related pathology-oriented content
* clustering of domain-specific semantic patterns

This makes the notebook more original, more professional, and more aligned with real-world NLP thinking.

---

## NLP Techniques Covered

### 1. Bag-of-Words

Bag-of-Words converts documents into sparse term-frequency vectors.

For a vocabulary of size $V$, each document is represented as:

$$
\mathbf{x}_d = [c_1, c_2, c_3, \dots, c_V]
$$

where each component represents the count of a vocabulary term in the document.

---

### 2. TF-IDF

TF-IDF reweights terms based on how informative they are across the corpus.

$$
\text{TF-IDF}(t, d, D) = \text{TF}(t, d) \times \log\left(\frac{N}{df(t)}\right)
$$

This helps reduce the influence of overly common words and strengthens more meaningful terms.

---

### 3. Word2Vec

Word2Vec learns dense vector representations based on contextual co-occurrence.

Words appearing in similar contexts tend to occupy nearby positions in vector space.

---

### 4. GloVe 6B

GloVe introduces pre-trained word vectors learned from a much larger corpus.

This project includes **GloVe 6B (50-dimensional vectors)** to compare local semantic learning with broader pre-trained language knowledge.

---

### 5. OpenAI Embeddings

The notebook also includes an **OpenAI embeddings workflow** for semantic vector generation.

This reflects a more modern production-style NLP approach and is useful for:

* semantic similarity
* retrieval
* question-answer ranking
* vector search preparation

---

### 6. Clustering

The notebook uses **K-Means clustering** to group semantically related questions and text records.

---

### 7. Dimensionality Reduction

High-dimensional vectors are projected into lower dimensions using:

* **PCA** – for structural variance analysis
* **t-SNE** – for local semantic neighborhood visualization

---

## Notebook Contents

| Section                   | Description                                                            |
| ------------------------- | ---------------------------------------------------------------------- |
| Introduction              | Purpose of the workshop and PathoIntern framing                        |
| Imports and Setup         | Required libraries, environment setup, and helper configuration        |
| Premium Helper Functions  | Pagination, plot explanation helpers, and text preprocessing utilities |
| Synthetic Corpus Creation | Domain-specific PathoIntern question-answer corpus                     |
| Text Preprocessing        | Cleaning, tokenization, and normalization                              |
| Bag-of-Words              | Sparse vector representation                                           |
| TF-IDF                    | Weighted document representation                                       |
| Word2Vec                  | Local embedding training and semantic similarity                       |
| GloVe 6B Integration      | Loading and applying pre-trained embeddings                            |
| OpenAI Embeddings         | API-based embedding workflow                                           |
| Similarity Analysis       | Cosine similarity between text vectors                                 |
| Clustering                | K-Means semantic grouping                                              |
| PCA / t-SNE               | Visual exploration of embedding structure                              |
| Assistant Workflow        | Question-response retrieval examples                                   |
| Final Interpretation      | Comparative analysis, limitations, and conclusion                      |

---

## Project Structure

```text
Embeddings-Clustering-Vectorization-Workshop-Lab9/
│
├── PathoIntern_EmbeddedClustering.ipynb
├── README.md
├── requirements.txt
├── .gitignore
├── .env
│
├── glove.6B/
│   ├── glove.6B.50d.txt
│   ├── glove.6B.100d.txt
│   ├── glove.6B.200d.txt
│   └── glove.6B.300d.txt
│
└── .venv/
```

---

## Files and Paths

### Main Notebook

```text
PathoIntern_EmbeddedClustering.ipynb
```

### Environment File

```text
.env
```

### GloVe Embedding Path Used by the Notebook

```text
glove.6B/glove.6B.50d.txt
```

### Requirements File

```text
requirements.txt
```

### Git Ignore File

```text
.gitignore
```

---

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Lohithreddy29/Embeddings-Clustering-Vectorization-Workshop-Lab9.git
cd Embeddings-Clustering-Vectorization-Workshop-Lab9
```

---

### 2. Create and Activate a Virtual Environment

#### Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```

#### macOS / Linux

```bash
python -m venv .venv
source .venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Configure the `.env` File

Create or update the `.env` file in the project root:

```env
OPENAI_API_KEY=your_actual_openai_api_key_here
OPENAI_EMBEDDING_MODEL=text-embedding-3-small
```

> Note: The API key is not hardcoded in the notebook.
> It is intentionally loaded through `.env` for secure configuration.

---

### 5. Confirm GloVe File Placement

Make sure the following file exists:

```text
glove.6B/glove.6B.50d.txt
```

---

### 6. Launch the Notebook

```bash
jupyter notebook
```

Then open:

```text
PathoIntern_EmbeddedClustering.ipynb
```

You may also run it through **VS Code Jupyter**.

---

## Dependencies

Main Python libraries used in this project:

* **numpy**
* **pandas**
* **matplotlib**
* **plotly**
* **scikit-learn**
* **gensim**
* **nltk**
* **openai**
* **python-dotenv**
* **jupyter**
* **notebook**
* **ipykernel**
* **ipywidgets**
* **jinja2**
* **pillow**

Install all of them with:

```bash
pip install -r requirements.txt
```

---

## Important Notes

### OpenAI Embeddings

The OpenAI section is included as part of the notebook’s modern embedding workflow.
If your API key is missing, invalid, or out of quota, that section will skip or fail gracefully depending on execution conditions.

### GloVe Files

The GloVe files are large external assets and are typically ignored through `.gitignore`.
That means collaborators should download them locally and place them inside:

```text
glove.6B/
```

### `.env` Security

Do **not** commit your `.env` file with a real API key to GitHub.

---

## Key Strengths of This Project

* domain-specific PathoIntern framing
* strong academic notebook structure
* modern NLP workflow coverage
* integration of both local and hosted embeddings
* premium visualization and explanation flow
* semantic retrieval demonstration
* clustering and dimensionality reduction analysis
* professional project setup for GitHub submission

---

## Practical Applications

The techniques in this notebook are relevant to:

* semantic search systems
* pathology-support assistants
* clinical note triage workflows
* intelligent question-answer retrieval
* recommendation systems
* topic grouping
* vector search pipelines
* retrieval-augmented AI systems

---

## Comparative Insight

One of the most important ideas demonstrated in this notebook is that different NLP representations solve different kinds of problems:

* **Bag-of-Words** captures occurrence
* **TF-IDF** captures importance
* **Word2Vec** captures local semantic context
* **GloVe** captures broader pre-trained language meaning
* **OpenAI embeddings** represent a modern semantic retrieval direction

This comparison is one of the central learning outcomes of the workshop.

---

## Limitations

Although the project is strong as a comparative NLP workflow, a few limitations should be acknowledged:

* the corpus is synthetic and relatively small
* Word2Vec quality is constrained by corpus size
* GloVe is pre-trained on general text, not specifically pathology language
* OpenAI embeddings depend on API access and available quota
* clustering results are exploratory and should be interpreted qualitatively

These limitations do not reduce the value of the project, but they help place the findings in the correct academic context.

---

## Final Conclusion

This project demonstrates a complete NLP workflow within the **PathoIntern** domain, beginning with sparse vectorization and progressing toward modern embedding-based semantic analysis.

It shows how text can be transformed from raw language into structured vector spaces suitable for:

* retrieval
* similarity comparison
* clustering
* semantic interpretation

More importantly, the notebook shows that representation quality directly affects how intelligent a system can appear.
A keyword-based system behaves very differently from an embedding-based system, and that difference becomes especially meaningful in a domain-oriented assistant setting such as PathoIntern.
It is a structured demonstration of how modern NLP techniques can be compared, interpreted, and applied in a meaningful domain-specific context.

---


