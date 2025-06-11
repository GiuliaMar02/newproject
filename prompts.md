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
  <a href="triples.html">🔗 RDF Triples</a> |
  <a href="challenges.html">⚠️ Challenges</a> |
  <a href="conclusion.html">✅ Conclusion</a>
</div>

# USE LLM TO VERIFY AND PRODUCE NEW KNOWLEDGE

We used two LLMs: [ChatGPT](https://chat.openai.com/) and [Gemini](https://gemini.google.com/)

## First Missing Information: the alternative name of the Abbazia di Nonantola

### Zero-shot Prompting Technique

According to this technique, we asked the LLMs a prompt without giving any examples or demonstrations, relying on their general understanding of language and tasks. This helps test their raw ability to provide useful answers without prior context or scaffolding.

This technique is particularly helpful when:

- A quick answer is needed
- No examples are available
- The task is generic or straightforward

In our case, this method was sufficient to extract the missing alternative name, as demonstrated below.

### [ChatGPT](https://chat.openai.com/)

![Screenshot](assets/images/prompt_1.png)

- ChatGPT provided more than one name, including the one we were searching for.
- The answer was detailed: it included the **English** name of the abbey, its **ecclesiastical** name, and additional context like **location**, **dedication to San Silvestro**, **foundation date**, and **diocese**.
  
### [Gemini](https://gemini.google.com/)

![Screenshot](assets/images/prompt_2.png)

- Gemini gave a more **concise and direct** response, but still provided the **correct alternative name**.
- It confirmed the **dedication to Pope San Silvestro**, added info about **relics**, and provided the **English** name of the abbey.
- Unlike ChatGPT, Gemini also included a **photo** of the abbey.

### Confirmation from Official Source

The official site of the Abbey confirms this information:

> “Da ultimo, una quarta dedicazione, questa volta a San Silvestro I papa, sarebbe avvenuta il 20 novembre 756 ad opera del vescovo Romano di Bologna. Da quel momento l’abbazia, impreziosita dal corpo del santo papa portato da Roma a Nonantola dai longobardi nel 756, assunse definitivamente il titolo di San Silvestro.”  
> — [abbazianonantola.it](https://abbazianonantola.it/)

---

## Second Missing Information: Commission

### Chain-of-Thought (Zero-shot) Technique

In this case, we applied **Chain-of-Thought** prompting in combination with the **Zero-shot** approach.

This method encourages the model to "think aloud," reasoning step-by-step before giving a final answer. It helps improve the quality of responses, especially when dealing with complex or historical topics like **commissions** involving multiple figures.

This approach was particularly effective with stronger models such as GPT-4. As shown below, [ChatGPT](https://chat.openai.com/) provided a more coherent and historically grounded answer compared to [Gemini](https://gemini.google.com/).

---

### Prompt:  
**Who was the commissioner of the Abbazia di Nonantola? Let’s think step by step**

---

### [ChatGPT](https://chat.openai.com/)

> Sure! Let's break it down step by step to identify the commissioner (or founder/patron) of the Abbazia di Nonantola:
>
> **Step 1: What is the Abbazia di Nonantola?**  
> The Abbazia di Nonantola (Abbey of Nonantola) is a historic Benedictine monastery located in the town of Nonantola, near Modena in northern Italy. It was a significant religious, cultural, and political center during the Middle Ages.
> 
> **Step 2: When was it founded?**  
> The abbey was founded in the 8th century, more precisely in the year 752.
> 
> **Step 3: Who commissioned or founded it?**
> The founder and commissioner of the abbey was:
> 
> ➤ Saint Anselm (Anselmo di Nonantola)
> 
> • He was a Lombard nobleman and the brother-in-law of King Aistulf of the Lombards.
> 
> • Anselm was a duke (duke of Friuli) before becoming a monk.
> 
> •	Around 752, he founded the abbey with the support of King Aistulf.
> 
> •	The abbey received many privileges and became one of the most powerful monastic institutions in northern Italy.
> 
> **Step 4: Support from the Lombard king**  
> •	King Aistulf of the Lombards played an important supporting role in the establishment of the abbey.
> •	He donated land and resources, helping to ensure its prominence and autonomy.

> ✅ **Final Answer**:  

> The Abbazia di Nonantola was commissioned (founded) by Saint Anselm (Anselmo di Nonantola) in 752, with the support of King Aistulf of the Lombards.

•	ChatGPT talks about “commissioner” as a synonym of “founder” and after providing us with a short historical background, it gives us a precise name: Saint Anselm. 

---

### [Gemini](https://gemini.google.com/)

> The term "commissioner" in relation to the Abbazia di Nonantola can refer to different roles throughout its long history, especially considering periods where the abbey was managed by commendatory abbots.
> Here's a breakdown:
> •	Abbots Commendatory: From 1449 onwards, the Abbey of Nonantola saw the beginning of the "Commenda" system. This meant that the abbot, known as an abbot commendatory (abate commendatario), was not necessarily a resident monk but an external figure, often appointed by the Pope or a secular ruler, who received the revenues of the abbey. These commendatory abbots effectively "commissioned" or oversaw the abbey's administration and assets, although their involvement in the spiritual life of the monastery varied greatly.
> Notable commendatory abbots included:
> •	Gurone d'Este (1449–1484)
> 
> •	Giuliano card. Della Rovere (1485–1503), who later became Pope Julius II.
> 
> •	San Carlo Borromeo (1560–1566)
> 
> •	Current Leadership: Today, the Abbazia di Nonantola is part of the Archdiocese of Modena-Nonantola. The current Archbishop-Abbot is Erio Castellucci. He serves as the spiritual and administrative head, effectively the "commissioner" in a modern sense, overseeing the abbey and its activities.
> 
> If you are looking for a specific historical period or a particular type of "commissioner," please provide more details, as the term can be interpreted in various ways for an institution with such a rich and long history.

---

