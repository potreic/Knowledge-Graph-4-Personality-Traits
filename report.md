# Knowledge Graph Construction Using Large Language Models for Personality Trait Extraction

## 1. Title

**Knowledge Graph Construction Using Large Language Models for Personality Trait Extraction**

---

## 2. Background

Knowledge Graphs (KGs) serve as a structured form of representing information, capturing the relationships between entities in a way that supports reasoning, inference, and retrieval of contextual meaning. Traditional KG construction requires extensive manual annotation and domain-specific datasets, which are both time-consuming and costly.

With the advancement of **Large Language Models (LLMs)**, it has become possible to extract semantic relationships directly from unstructured text. This project leverages an LLM-based pipeline to build a Knowledge Graph that models **human personality traits** following the **Big Five Personality Model** — Openness, Conscientiousness, Extraversion, Agreeableness, and Neuroticism.

By integrating psychological insight into data representation, the system aims to connect personality behavior and textual expression in a structured, explainable way.

---

## 3. Problem Statement

Constructing a personality-aware Knowledge Graph poses multiple challenges:

1. **Data limitation:** Real-world datasets with labeled personality attributes are scarce.  
2. **Subjectivity:** Personality interpretation from text often depends on human judgment.  
3. **Scalability:** Manual annotation is infeasible for large corpora.

The project addresses these issues by generating **synthetic personality text data** and employing **LLM-based automation** to identify and structure psychological traits from textual inputs.

---

## 4. Objectives

1. To generate synthetic textual data that simulates the Big Five personality traits.  
2. To design and implement a pipeline for constructing a Knowledge Graph using LLM-based information extraction.  
3. To evaluate the generated Knowledge Graph’s accuracy using precision, recall, and F1-score.  
4. To represent extracted traits in a structured graph format using (Subject, Predicate, Object) relationships.

---

## 5. Methodology

The project is divided into five major stages:

### a. Synthetic Data Generation

Since no labeled dataset was available, synthetic text was generated to represent personality-driven scenarios. For example, workplace dialogues were written where participants express distinct behavioral patterns (e.g., assertiveness, empathy, creativity). Each narrative corresponds to one or more Big Five traits. This approach ensures coverage across different personality dimensions while maintaining realism.

### b. LLM-Orchestrated Workflow

The system employs **LangChain** for orchestration and **DeepSeek API** as the LLM backbone. Instead of using a single prompt, multiple chained stages were implemented to improve structure and reduce ambiguity:

1. **Extraction stage:** The model identifies entities and psychological traits mentioned in the text.  
2. **Triplet construction:** The extracted information is converted into Knowledge Graph triples (Subject, Predicate, Object).  
3. **Validation stage:** The structured triples are compared to a manually defined reference set.

### c. Personality Representation

The Knowledge Graph captures personality associations in the form:
```
(Alex, has_trait, Conscientiousness)
(Ben, has_trait, Extraversion)
(Chloe, has_trait, Assertiveness)
```


This format ensures interpretability while aligning with the Big Five model’s psychological taxonomy.

### d. Normalization

To maintain consistency, text normalization steps include:

- Lowercasing textual input  
- Removing punctuation and unnecessary whitespace  
- Standardizing entity and trait naming  

However, psychologically relevant terms and names were **not normalized** to preserve meaning. This selective normalization balances linguistic clarity with semantic integrity.

### e. Implementation Framework

The implementation pipeline integrates LangChain’s structured prompt chains with DeepSeek’s semantic extraction capabilities. Each stage is modular and allows independent evaluation or re-prompting, ensuring the workflow remains adaptable and transparent.

---

## 6. Results and Discussion

The pipeline successfully extracted meaningful personality relationships from the generated text. Example output triples include:
```
(Alex, has_trait, Conscientiousness)
(Ben, has_trait, Extraversion)
(Chloe, has_trait, Assertiveness)
```


The Knowledge Graph structure reflects how individuals behave in specific contexts, such as decision-making under pressure or collaboration in group settings. By representing behavioral patterns through relational triples, the system demonstrates how psychological information can be transformed into structured, machine-readable data.

The LangChain workflow proved effective for chaining tasks like extraction, formatting, and validation, offering better controllability compared to using a single prompt. This multi-step process increased the model’s precision and consistency in extracting correct traits.

---

## 7. Evaluation

To assess the KG’s performance, **Precision**, **Recall**, and **F1-score** were used:

- **Precision** = (Correctly extracted triples) / (Total extracted triples)  
  → Measures accuracy of the output.  

- **Recall** = (Correctly extracted triples) / (Total relevant triples in ground truth)  
  → Measures completeness of the extraction.  

- **F1-score** = 2 × (Precision × Recall) / (Precision + Recall)  
  → Provides a balanced overall measure.  

The **ground truth** consisted of manually verified triples derived from the same synthetic texts. This ensures that evaluation reflects the model’s ability to replicate human reasoning when identifying personality patterns.

This evaluation framework is standard in information extraction and is well-suited for determining the balance between the model’s accuracy and completeness.

---

## 8. Obstacles / Challenges

- **Data Scarcity:** Absence of real personality-annotated data required the creation of synthetic text.  
- **Prompt Sensitivity:** LLMs may produce inconsistent or verbose outputs, requiring prompt tuning and multi-step validation.  
- **Subjectivity:** Human interpretation of personality traits introduces evaluation bias.  
- **Processing Time:** Chaining multiple prompts increases API latency and cost.

Despite these challenges, the pipeline achieved coherent and interpretable results that could generalize across diverse scenarios.

---

## 9. Conclusion

This project demonstrates that **Large Language Models** can effectively construct **Knowledge Graphs** representing human personality traits. Through synthetic data generation, prompt chaining via LangChain, and structured extraction with DeepSeek, the workflow achieved both flexibility and interpretability.

The use of **Big Five Personality Model** enables a psychological foundation for graph construction, allowing extracted data to hold both semantic and behavioral value. Evaluation through **precision, recall, and F1-score** ensures that the system not only performs accurately but also remains measurable and improvable.

Future work can include expanding to real psychological datasets, integrating graph-based embeddings for deeper analysis, and fine-tuning LLMs for more consistent personality interpretation.

### 🌿 Credits

1. **Nibroos Haryanto** — System and Prompt Engineer  
2. **Gemini** — [View Chat](https://gemini.google.com/share/d3704085ccc6)  
3. **GPT** — [View Chat](https://chatgpt.com/share/69037ae0-12c4-8009-bc9e-06eb91284b1c)

---

<div align="center">

💚 **Crafted with care by Nibroos, GPT & Gemini** 💚

</div>
