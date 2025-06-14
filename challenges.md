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

### 📚 Exploring Ontology and Trying to Find Missing Information

The results of our queries gave us few information about our abbey, something that made the research of the gaps more difficult.

**✅ Solution:**  
We tried to build more generic queries to find bigger amounts of information (e.g.: the query where we lo oked for cultural properties in Nonantola).

---

### 🔍 Identifying Proper Predicates for RDF Triples

Predicates and properties may seem very similar to one another, and many others were difficult to find. 

**✅ Solution:**  
We designed more specific queries to search for properties related to abbeys in general.

---

### 💬 Engineering Effective LLM Prompts

Especially in step 3, often LLMs were deficient in giving the answers we wanted.

**✅ Solution:**  
We refined our prompt strategies according to the **three required techniques** (`zero-shot`, `few-shot`, `chain-of-thought`), aligning them with the type of missing information we wanted to retrieve.

---

## 🏛️ Selecting an Appropriate IRI that could represent the topic

To enrich the cultural data, we needed to choose the most suitable IRI to represent the [Abbazia di Nonantola](https://w3id.org/arco/resource/HistoricOrArtisticProperty/0100210793). However, only two relevant IRIs were found through Query 2.
Our topic is an immovable cultural property, hence there are only visual representations in the ArCo Ontology. Moreover, finding the second IRI ([https://w3id.org/arco/resource/PhotographicHeritage/0800634107](https://w3id.org/arco/resource/PhotographicHeritage/0800634107)) for the [Abbazia di Nonantola](https://w3id.org/arco/resource/HistoricOrArtisticProperty/0100210793) was quite challenging since there was no reference to the Abbazia whatsoever in the title of the cultural property.

**✅ Solution:** 
We chose two IRIs of the [Abbazia di Nonantola](https://w3id.org/arco/resource/HistoricOrArtisticProperty/0100210793). For the first two triples we used the IRI of the photo of the absidal part, but we didn’t choose the same IRI for the other triples (3 and 4) because we were looking at the front part of the abbey.

---

### 🖥️ Technical and Infrastructure Issues

Working with AI and IT tools meant that we were also vulnerable to downtimes and performance issues. On multiple occasions, the [ArCo SPARQL endpoint](https://dati.cultura.gov.it/sparql) was extremely slow or unresponsive. Similarly, [ChatGPT](https://chat.openai.com/) occasionally failed due to traffic overload.

**✅ Solution:**  
Despite losing approximately **1.5 days** of work, we resumed our tasks as soon as the services became available and were able to complete the project without compromising quality.

---

Each of these challenges helped us gain deeper insight into semantic web technologies, LLM prompting strategies, and the complexities of digital cultural heritage enrichment.

<hr>
<div style="display: flex; justify-content: space-between; margin-top: 2em;">
  <a href="rdf.html">← Previous</a>
  <a href="conclusion.html">Next →</a>
</div>
