# 🧠 Personality Knowledge Graph with LLMs

> Turn plain text into a *psychologically aware* Knowledge Graph — powered by LangChain + DeepSeek 🕸️💬

---

## 🌟 What’s This Project?

This project builds a **Knowledge Graph (KG)** that connects people and their **personality traits** — all extracted automatically from text using a **Large Language Model (LLM)**.  

Think of it as a system that *reads a story*, understands who’s being introverted, confident, or creative, and then maps that behavior in a structured graph like:
```
(Alex, has_trait, Conscientiousness)
(Ben, has_trait, Extraversion)
(Chloe, has_trait, Assertiveness)
```


It’s a mash-up of **AI**, **psychology**, and **data graphs** — all done in one chain of prompts. 🧩

---

## 🚀 Why Build This?

Because understanding *how people behave through text* is fascinating — and doing it **without labeled data** is even cooler.

💬 Real datasets are rare  
💡 Personality is subjective  
⚙️ Manual labeling? Nope, too slow  

So… we generated **synthetic scenarios** (like a project crisis meeting 💼) where each character shows traits under pressure — then let the **LLM + LangChain** do the heavy lifting.

---

## 🧩 How It Works

1. **Generate Synthetic Texts**  
   Create realistic scenarios that reflect human behavior and emotion.  
2. **Extract Personality Info (LLM time!)**  
   DeepSeek reads the text → finds who did what → detects traits.  
3. **Build the Graph**  
   LangChain organizes the output into (Subject, Predicate, Object) triples.  
4. **Evaluate**  
   Compare with a “ground truth” (manually defined) using **precision**, **recall**, and **F1-score**.

---

## 🔍 Example Output

```
(Alex, has_trait, Conscientiousness)
(Ben, has_trait, Extraversion)
(Chloe, has_trait, Assertiveness)
```

## 🧠 Personality Model Used
We use the Big Five Personality Model (because it’s the gold standard 💛):
1. Openness 🪄 — creative, curious
2. Conscientiousness 📋 — disciplined, organized
3. Extraversion 🎤 — social, energetic
4. Agreeableness 💕 — kind, cooperative
5. Neuroticism 🌧️ — anxious, emotional

---

## 🛠️ Tech Stack
1. 🦜 LangChain — Orchestrates the multi-step prompt pipeline
2. 🤖 DeepSeek API — The brain that extracts entities and traits
3. 🧬 Python + Pydantic — Keeps data structured and schema-validated
4. 💾 Graphviz — Graph representation and visualization
---

## 📈 Evaluation Metrics
We don’t just vibe, we verify. Using the classics from info extraction:
- Precision → How accurate the extracted triples are
- Recall → How complete they are
- F1-score → The perfect balance between both

---

## ⚡ Results Summary
✅ LLM successfully extracted personality traits from synthetic text
✅ Graph structure interprets behaviors logically
✅ LangChain pipeline made outputs more consistent

---

## 🧩 Folder Guide
```
📁 Knowledge-Graph-4-Personality-Traits/
 ├── notebook.ipynb        # Main workflow
 ├── report.md             # Formal project write-up
 ├── README.md             # You’re here 💁‍♀️              
 └── data/example.txt      # Generated KG triples
```
