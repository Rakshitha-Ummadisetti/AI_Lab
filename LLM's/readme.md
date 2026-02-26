Chunking Methods Explorer
This is a browser-based tool to visualize and compare how different text chunking strategies work. 
What it does
Paste any text, adjust chunk size and overlap, and see how seven different strategies slice it with chunk count, average size, and token estimates shown live. A compare view lets you see all methods side by side.


Methods covered
Fixed size —> word-boundary-snapped character windows
Sentence-based —> abbreviation-aware sentence tokenizer (handles Dr., U.S., decimals)
Paragraph-based —> respects \n\n boundaries, recursively splits oversized paragraphs
Sliding window —> overlapping windows with word-boundary snapping
Semantic —> TF-IDF cosine similarity with adaptive σ-based breakpoints
Recursive —> faithful LangChain RecursiveCharacterTextSplitter implementation
Token-based —> BPE-approximate token counting with sentence-level overlap carry

What I learned
The naive implementations you find in most tutorials are wrong in subtle ways — sentence splitters that break on "Dr.", token counters that use chars÷4, recursive splitters that lose their separators. Getting these right matters because bad chunk boundaries directly hurt retrieval quality in RAG pipelines.
Semantic chunking without real embeddings is still useful — TF-IDF cosine similarity with an adaptive threshold captures topic shifts well enough to understand the concept before adding an API call.


Stack
Pure HTML/CSS/JS. No dependencies, no build step. Open the file in a browser.

