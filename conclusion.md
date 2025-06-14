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
  <a href="challenges.html">⚠️Challenges</a>
</div>

---

![Conclusion](assets/images/conclusion.png)

Our project on the **[Abbazia di Nonantola](https://w3id.org/arco/resource/HistoricOrArtisticProperty/0100210793)** allowed us to explore the potential and limitations of semantic web technologies and large language models in the context of Italian cultural heritage. Here are the main takeaways:

---

### 🧠 SPARQL and ArCo Ontology

SPARQL and the [ArCo](http://wit.istc.cnr.it/arco/?lang=en) ontology proved to be powerful tools for accessing structured data related to Italy's vast cultural heritage. We learned how:
- **Keyword selection** is crucial to obtaining relevant and non-redundant results.
- SPARQL’s logic-based structure allows for very precise queries that can uncover both explicit and implicit knowledge gaps in the data.

---

### 🤖 Large Language Models

Our work with LLMs, particularly **[ChatGPT](https://chatgpt.com/)** and **[Gemini](https://gemini.google.com/app)**, revealed the strengths and weaknesses of both systems:
- Theytend to perform better through **prompting techniques** that use examples, structured input, and clear task definitions (especially **few-shot** and **chain-of-thought**).
-However, when looking for vey specific information, the LLMs do not always provide the correct answer. **[ChatGPT](https://chatgpt.com/)** often appeared more fluent and logically structured, especially in **chain-of-thought** tasks.
- Moreover, though **[ChatGPT](https://chatgpt.com/)** may appear more efficient and “intelligent” when answering questions, especially with the chain-of-thought technique,  **[Gemini](https://gemini.google.com/app)** performs better than [ChatGPT](https://chatgpt.com/) when guided by well-structured prompting techniques, such as the few-shot technique. 

This finding contradicted our initial expectations and showed the importance of **model-specific prompting** strategies in both of the LLMs.

---

### 🌍 Future Developments

This project opens the door to several possibilities for future enrichment:
- **New RDF triples** (especially regarding the abbey’s inscriptions) could be integrated into ArCo to enhance its current representation of **[Abbazia di Nonantola](https://w3id.org/arco/resource/HistoricOrArtisticProperty/0100210793)**.
- Furthermore, the ontology could be further enriched with more accurate depictions of the abbey, directly connected to an **IRI about Abbazia di Nonantola as “Architectural or Landscape heritage”** or as an **“Immovable cultural property”**.


---

Through this project, we gained hands-on experience in **semantic enrichment**, **data querying**, and **LLM prompting**, while contributing to the visibility of a lesser-known yet historically significant cultural site.

<hr>
<div style="display: flex; justify-content: flex-start; margin-top: 2em;">
  <a href="challenges.html">← Previous</a>
</div>
