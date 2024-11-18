# AI Powered Knowledge Systems 

## Mission

To create a Software as a Service, (SASS), product that enable the medical community to harness the power of AI to improve extraction and presentation of relevent, accurate and complete information from the vast amount of data available in the medical literature.


## Current concepts

What are the current concepts/buzz words in this space?

### LLM

A large language model (LLM) is a type of artificial intelligence (AI) program that can recognize and generate text, among other tasks. LLMs are trained on huge sets of data — hence the name "large." LLMs are built on machine learning: specifically, a type of neural network called a transformer model.

We represent it in our architecture as a brain and this serves us well as we can also think what would a human do at this stage?

![brain](./images/rag/brain.png)

### Vector Databases

![vector space](./images/rag/vector-space.png)

OpenAI has 1536 dimensions

### Semantic search

Semantic search vectors are numerical representations of data and related contexts that are used to rank and deliver search results based on their relevance. 

The closer two points in vector space are, the more similar they are.

There are a few different methods such as cosine similarity, dot product, Euclidean distance etc.

### RAG

RAG = Retrieval Augmented Generation

RETRIEVAL:

We retrieve the most useful information from a vector database and then use it to generate a response using the LLM.

AUGEMENTED:

We combine the retreived documents and the query and pass it to the LLM to generate a response.

GENERATION:

The LLM generates the final response.


### Prompt Engineering

There is a difference between sending the documents and query to the LLM as is and a prompt template:

"You are an expert in the field of medicine. Answer the following question: {question} based on the following documents: {documents}"

If you are unsure about your answer, say "I don't know".

Use a professional and formal language in your responses.

Where possible, use references from the documents.

I like to thing of it as giving an actor details about a scene or giving a detailed job description to an researcher.

### AI Agents

An artificial intelligence (AI) agent is a software program that can interact with its environment, collect data, and use the data to perform self-determined tasks to meet predetermined goals. Humans set goals, but an AI agent independently chooses the best actions it needs to perform to achieve those goals. For example, consider a contact center AI agent that wants to resolves customer queries. The agent will automatically ask the customer different questions, look up information in internal documents, and respond with a solution. Based on the customer responses, it determines if it can resolve the query itself or pass it on to a human.

Whilst we may have our overall flowchart, the AI Agent will determine the path to take. It is like having the roll of a dice determine the next step. We have a predetermined set of tasks, but the agent will determine the best way to complete those tasks.

## Naive Rag

Two years ago when we first looked at RAG, the strategy was to take a document and split into chuncks of say 500 characters and have an overlap of 100 charactes with the next chunk to maintain some context.

This works very well for single modality text documents where this Niave Rag is in effect a search tool, taking an unstructured query and using LLMs and semantic search to find relevant chunks and answer the question.

## Changes in 2yrs

In the past two years there have been many changes in the space.

- Context windows, the amount of text we can pass to the LLM has grown from 4K to 32K+
- Compute power has greatly increased, costs have gone donw by 90%.
- LLMs have become bigger and better, with many specialist LLMs that are fine tuned for particular uses.
- LLMs can now understand images, tables and videos better, with LLMs that can parse different media and convert them into text.
- Many frameworks and services for RAG have emerged and 2025 is thought of the year that the question will be which system to use?
- Naive Rag has been replaced with more sophisticated strategies that involve all aspects of the architecture:

Without needing to understand this next image, here is the current 'state of the art' RAG architecture:

![RAG](./images/rag/current-rag-architecture.png)

New academic papers for better techniques are continually being published.

*"This is the worst it will ever be..."* - someone said.

## Proposed application

### unstructured.io


### Text processing

### Table processing

### Image processing

## Requirements

### Hosting

This is detailed in the architecture section.

Postgres/Django on render.com.

The front end is decoupled from backend so that we can change the technology of the front end as we see fit.

### Data

We will need a set of pdfs, Word, Powerpoint and Excel documents etc for a particular domain area to carry out evaluation of the app.

### What do we want?

Given that we have all these atoms of data and metadata, what do researchers want the app to do?

## Timescale

Most of the core is done soe March-June will be final develpoment, testing and evaluation. 

By the end of June, a SaSSO will be ready to go live or the project will come to an end.

## Costs

Base costs of a DB,hosting and OpenAI is around $320/month which I am happy to pay.

When useage grows, the costs will increase. These will need to be borne by the project.

For customers, they can use their own OpenAI account. Charges for DB and website traffic will be borne by the project/customer/ 

This mechanism is yet to be determined.

<br>