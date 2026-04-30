## Why **Self-RAG** is used

**Self-RAG (Self-Reflective Retrieval-Augmented Generation)** improves traditional RAG by allowing the model to decide:

1. **Whether retrieval is needed**

   * The model checks if external knowledge is required before searching.
   * Avoids unnecessary document retrieval.

2. **Which retrieved documents are useful**

   * It filters low-quality or irrelevant documents.
   * Improves answer quality.

3. **Whether the generated answer is grounded**

   * The model evaluates if the response is supported by retrieved content.
   * Reduces hallucinations.

4. **When to revise the answer**

   * If the answer is weak, the model can retrieve again and regenerate.

### Main benefits

* Better factual accuracy
* Less hallucination
* More efficient retrieval
* Higher answer reliability
* Improved reasoning over retrieved data

---

## Limitations of Traditional RAG

Traditional RAG has several limitations:

### 1. **Retrieval errors**

Sometimes the retriever fetches:

* irrelevant chunks
* incomplete context
* outdated data

Result → wrong answers.

---

### 2. **No quality checking**

Standard RAG usually:

* retrieves documents
* directly generates response

It does **not verify** whether retrieved data is trustworthy.

---

### 3. **Chunking issues**

Documents are split into chunks, causing:

* missing context
* broken meaning
* partial answers

---

### 4. **Hallucination still possible**

Even with retrieval, the LLM may:

* ignore retrieved content
* mix internal knowledge
* generate unsupported claims

---

### 5. **Static retrieval**

Traditional RAG cannot easily:

* re-retrieve
* refine search
* correct bad answers

---

### 6. **Latency**

RAG can be slower because it involves:

* embedding search
* vector DB lookup
* reranking
* generation

---

## Why Self-RAG improves RAG

Self-RAG adds:

**Retrieve → Evaluate → Generate → Reflect → Refine**

This makes the system more reliable than standard RAG.

---


