# ✨ Nexora — Vibe Matcher (AI Prototype)

A mini AI-powered fashion recommendation system that matches a user's *"vibe"* query (e.g., **"energetic urban chic"**) to the most relevant fashion items using **text embeddings** and **cosine similarity**.

---

## 💡 Why AI at Nexora?

AI at **Nexora** can transform subjective style language into precise, data-driven recommendations.  
This prototype demonstrates how AI models can translate abstract “vibes” into measurable vector embeddings and retrieve matching fashion items — bridging creativity with intelligent personalization at scale.

---

## ⚙️ Project Overview

| Step | Description |
|------|--------------|
| 🧾 **Data Preparation** | Created a small mock dataset (5–10 fashion items) with names, descriptions, and vibe tags. |
| 🧠 **Embeddings** | Used OpenAI embeddings (`text-embedding-3-small`) or deterministic pseudo-embeddings (for offline demo). |
| 📈 **Vector Search** | Computed cosine similarity between query and product embeddings using `scikit-learn`. |
| 🧮 **Evaluation** | Tested multiple vibe queries, logged similarity scores, and measured latency. |
| 🔁 **Reflection** | Suggested improvements like vector databases, multimodal embeddings, and personalization. |

---

## 🧰 Tech Stack

- **Languages:** Python  
- **Libraries:** Pandas, NumPy, scikit-learn, Matplotlib  
- **Optional:** OpenAI API for real embeddings  

---

## 🚀 How to Run

You can open and run this notebook directly in **Google Colab** 👇  

🔗 [**Open in Colab**](https://colab.research.google.com/drive/19hJua6S7ZbjBnZseBn75D8hC89gL0zjm?usp=sharing)

### ▶️ Running the Notebook

**Option 1 — With OpenAI API:**
```python
import os
os.environ["OPENAI_API_KEY"] = input("Enter your OpenAI API key: ").strip()
```
Then run the notebook from top to bottom to generate real embeddings.

**Option 2 — Offline Demo Mode:**

If you don’t have API credits, the notebook automatically uses deterministic pseudo-embeddings for smooth offline execution.

(The logic, cosine similarity, and evaluation remain identical.)

---

## 📄 Evaluation Results

All evaluation metrics (queries, top matches, similarity scores, latency) are saved in:

📊 vibe_match_eval.csv

---

## ✅ Summary

- Queries tested: 4
- Mean latency: ~0.2 sec per query
- Mode: Offline (pseudo-embedding)
- Similarity threshold: 0.7 for "good" matches

> Since this run used pseudo-embeddings, all similarity scores are random and below threshold.
> Real OpenAI embeddings typically yield 0.7–0.9 for strong matches.

---

## 📊 Evaluation Plots

- Latency per Query	
- Top-1 Similarity per Query	
- Similarity Distribution	

---

## 🧩 Reflection

- Scalability: The current approach works well for small datasets. In production, it could be scaled using vector databases such as Pinecone or FAISS for faster retrieval.
- Edge Cases: Includes low-similarity fallback and deterministic offline embeddings when API is unavailable.
- Enhancements: Could integrate multimodal embeddings (image + text) for richer fashion matching and personalization using user preferences.
- Optimization: Caching embeddings and introducing a lightweight re-ranking layer (boosting scores for matching vibe tags) would improve accuracy and speed.
- Learning Outcome: This project demonstrates how embeddings and vector search enable semantic, human-like recommendation systems.

---

## 🧩 Requirements

Install dependencies (if running locally):
```python
pip install -r requirements.txt
```

---

## 🙌 Acknowledgement

This project was developed as part of the AI Internship assignment at Nexora, demonstrating end-to-end understanding of embedding-based recommendation systems.

---

## 👤 Author

**Ayush Rawat**  
📧 [rawat.ayush.work@gmail.com](mailto:rawat.ayush.work@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/ayushrawat20)
