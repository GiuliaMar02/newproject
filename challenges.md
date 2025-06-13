---
layout: default
title: Abbazia di Nonantola
---

<div style="text-align: center; margin-bottom: 20px;">
  <a href="index.html">🏠 Home</a> |
  <a href="topic.html">🏛️ Topic</a> |
  <a href="methodology.html">⚒️ Methodology</a> |
  <a href="sparql.html">📊 SPARQL&Results</a> |
  <a href="gaps.html">🔍 Identifying Gaps</a> |
  <a href="prompts.html">💬 LLM Prompts</a> |
  <a href="rdf.html">🔗 RDF Triples</a> |
  <a href="conclusion.html">✅ Conclusion</a>
</div>

---

<img src="assets/images/challenges_solutions.png" alt="Challenges" width="400">

# Challenges Faced During the Project

In the development of our KE4H project on the **[Abbazia di Nonantola](https://w3id.org/arco/resource/HistoricOrArtisticProperty/0100210793)**, we encountered several challenges related to semantic technologies, data extraction, and prompt engineering. Below we describe each problem and how we addressed it.

---

### 🧩 Understanding the Functioning of SPARQL

At the beginning, we faced difficulties in understanding how SPARQL works and how to formulate accurate and precise queries, as this language requires strict syntax and logic.

**✅ Solution:**  
We examined existing SPARQL patterns and learned how to use key expressions such as `UNION`, `OPTIONAL`, `FILTER`, and `VALUES` effectively, which improved our confidence in writing complex queries.

---

### 📚 Managing Large and Repetitive Data

The results of our SPARQL queries often produced vast amounts of information, many of which were redundant or irrelevant to our topic. This made it difficult to identify missing or valuable data.

**✅ Solution:**  
We refined our keyword usage and filtering strategies. Despite initial difficulties, we successfully identified meaningful gaps in the dataset.

---

### 🔍 Identifying Proper Predicates for RDF Triples

Selecting suitable predicates was particularly challenging, especially when several similar options existed within the ontology or when the required property was hard to locate.

**✅ Solution:**  
We created more focused SPARQL queries to discover specific predicates and cross-referenced them with [ArCo](http://wit.istc.cnr.it/arco/?lang=en) documentation and examples.

---

### 💬 Engineering Effective LLM Prompts

Our initial prompts to the LLMs ([ChatGPT](https://chatgpt.com/) and [Gemini](https://deepmind.google/technologies/gemini/)) often resulted in vague or irrelevant responses.

**✅ Solution:**  
We refined our prompt strategies according to the **three required techniques** (`zero-shot`, `few-shot`, `chain-of-thought`), aligning them with the type of missing information we wanted to retrieve.

---

### 🏛️ Selecting an Appropriate IRI

To enrich the cultural data, we needed to choose the most suitable IRI to represent the **[Abbazia di Nonantola](https://w3id.org/arco/resource/HistoricOrArtisticProperty/0100210793)**. However, only two relevant IRIs were found through Query 2.

**✅ Solution:**  
We selected the IRI linked to the **photograph of the abbey’s apsidal part**, as it provided the most complete and visually representative depiction.

---

### 🖥️ Technical and Infrastructure Issues

Working with AI and IT tools meant that we were also vulnerable to downtimes and performance issues. On multiple occasions, the [ArCo SPARQL endpoint](https://dati.cultura.gov.it/sparql) was extremely slow or unresponsive. Similarly, [ChatGPT](https://chat.openai.com/) occasionally failed due to traffic overload.

**✅ Solution:**  
Despite losing approximately **1.5 days** of work, we resumed our tasks as soon as the services became available and were able to complete the project without compromising quality.

---

Each of these challenges helped us gain deeper insight into semantic web technologies, LLM prompting strategies, and the complexities of digital cultural heritage enrichment.
