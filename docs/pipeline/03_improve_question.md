# Improve question

We can process the query using a pre-query to increase the quality of retrieval;

## Multi Query

We get the LLM to make N versions of the user query and then get all the unique documents for them.

## HyDE


![HyDE](../images/rag/hyde.png)

Hypothetical document embeddings is a technique that creates a theoretical document when responding to a query, as opposed to using the query and its computed vector to directly seek in the vector database.
