# AI Poweered Knowledge Systems

This is a work in progress where I collect resources and ideas concerning AI Search, RAG, Agentic AI and AI Agents in the Data Pipeline.

As others have shared with me, I share my own research.

The areas I am working on are:

## AI Search

Using both Semantic and traditonal keyword search, a Hybrid search system can yield the best document retrieval for RAG implementations.

We get the best k results from Full Text Search/Keyword search and the k best results from semantic search, combine them together and rerank and then return N results.

## Agentic RAG

Retrieval Augmented Generation enables us to add domain specific data to our our prompts for better answers.

Agentig RAG uses Agents to plan, retrieve, refine and generate answers using specilaist agents for each of these aspects.

An example of this is Langgraph's **agentic-RAG**:

![agentic-rag](./images/agentic-rag.png)


## AI Agents in the Data Pipeline

The use of AI Agents in the Data Pipeline from ETL, Analysis to Reporting enables us to generate reports from data sources.

Some aspects are best done with traditional Data Processing and we should not make them agentic just because that is in fashion.

This can add non-deterministic bureaucracy to the data pipeline.

<br>