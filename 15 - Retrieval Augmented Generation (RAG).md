# Retrieval Augmented Generation (RAG)

## Overview

LLM tools usually leverage pre-existing knowledge up to a certain cutoff date (e.g., GPT-4's cutoff is September 2021). RAG enhances this by incorporating real-time, domain-specific information from a connected knowledge base.

## How RAGs Work

1. **Knowledge Base**: Documents are ingested, broken into chunks, transformed into text embeddings, and stored in a database.
2. **User Query**: The user asks a question.
3. **Retrieval**: Relevant information is retrieved from the knowledge base using an embedding model.
4. **Augmented Generation**: The LLM uses retrieved data to enhance its responses, incorporating both pre-trained data and additional context.

The architecture for RAGs is implemented using transformers consisting of two parts: an encoder and a decoder:

- **Encoder**: Transforms input text into vectors.
- **Decoder**: Generates new text from vectors.

### Approaches

- **RAG-Sequence**: Uses retrieved documents to predict the best possible answer.
- **RAG-Token**: Uses documents to generate the next token, then retrieves them to answer the query.

## Benefits of RAGs

- **Information Richness**: Ensures responses are current and relevant.
- **Reduced Fabrication**: Uses verifiable data to provide context.
- **Cost-Effective**: More economical than fine-tuning an LLM.

## Creating a Knowledge Base

### Vector Databases

Stores numerical representations of documents (embeddings). Allows efficient management and search of large datasets by breaking them into chunks.

### From Text to Embeddings

- Convert text to vector embeddings.
- Chunk documents at sentence or paragraph levels.
- Add context to chunks for better meaning.
- Use models like word2vec, ada-002 by OpenAI, Azure Computer Vision.

## Retrieval and Vector Search

Transforms user queries into vectors and searches for relevant documents.

### Retrieval Methods

- **Keyword Search**: Text-based searches.
- **Semantic Search**: Uses word meanings.
- **Vector Search**: Uses embeddings to find closest vectors.
- **Hybrid Search**: Combines keyword and vector search.

### Vector Similarity

Measures how similar vectors are using:

- **Cosine Similarity**: Based on the angle between vectors.
- **Euclidean Distance**: Straight line between endpoints.
- **Dot Product**: Sum of products of corresponding elements.

### Search Index

Stores embeddings for quick retrieval of similar chunks.

### Re-ranking

Orders search results by relevance using machine learning.

## Evaluating the Application

### Evaluation Metrics

- **Quality**: Natural, fluent, and human-like responses.
- **Groundedness**: Responses based on supplied documents.
- **Relevance**: Responses match the query.
- **Fluency**: Grammatically sensible responses.

## Use Cases for RAG and Vector Databases

- **Question and Answering**: Internal company data for employee queries.
- **Recommendation Systems**: Matching similar items like movies or restaurants.
- **Chatbot Services**: Personalized conversations based on user data.
- **Image Search**: Image recognition and anomaly detection.
