# Retrieval and Rerank
SentenceTransformers are used to generate embeddings for queries, sentences, and paragraphs, in the context of semantic search.

In scenarios involving intricate search requirements, such as question-answering retrieval, enhanced search performance can be achieved through the implementation of the Retrieve & Re-Rank strategy.

## Retrieve & Re-Rank Pipeline

![image](https://github.com/ArunVigneshFAI/Retrieval_and_Rerank/assets/141916176/c4c249ad-2848-49dd-b831-5afda1c75359)

In the given approach, a search query initiates a two-stage process. Initially, a retrieval system is employed, capable of procuring a substantial list of potential matches (e.g. 100 potential matches) deemed relevant to the query. The retrieval process can encompass lexical search methods like ElasticSearch, or it can integrate dense retrieval strategies utilizing a bi-encoder architecture.

However, it's acknowledged that the retrieved documents might encompass items of varying relevance to the search query. Consequently, the second phase involves the application of a re-ranker built upon a cross-encoder framework. This re-ranker computes relevance scores for all candidates in relation to the provided search query.

The ultimate output comprises a meticulously ranked list of hits, poised to be presented to the user, thus enhancing the efficiency and precision of the search process.
