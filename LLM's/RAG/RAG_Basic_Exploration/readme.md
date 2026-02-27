This notebook is the basic exploration of RAG ( Retrieval Augmented Generation).
The goal is to understand how retrieval enhances LLM responses by grounding them in external knowledge.


What is RAG?

**RAG combines:**

Retriever → Finds relevant context from documents.

Generator (LLM) → Produces answer using retrieved context.

Instead of relying purely on model memory, the system retrieves relevant chunks and injects them into the prompt.


**Pipeline Implemented:**

Document loading.

Text chunking strategies.(The folder named chunking in the same folder).

Embedding generation.

Vector similarity search.

Context injection into prompt.

Final answer generation.


