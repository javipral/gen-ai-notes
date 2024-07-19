# Building a Search Applications

## Building a Search Application

### Semantic Search

Semantic search uses the meaning of words in a query to return relevant results. EG: Searching for "my dream car" will understand "ideal car" instead of literally searching for dreams about cars.

### Text Embeddings

Text embeddings are semantic numerical representations of text used in natural language processing. EG: A text like "Today we are going to learn about Azure Machine Learning" can be transformed into a vector of 1536 numbers, each representing different aspects of the text.

### How Embedding Index works

For a search app that allows users to search for youtube videos of a particular channel in a semantic way we could:

1. **Download Transcripts**: Get transcripts for each YouTube video in the channel.
2. **Extract Speaker Name**: Use Functions to extract the speaker's name from the first 3 minutes of each transcript.
3. **Segment Text**: Chunk the transcript into 3-minute text segments with overlapping words for better context.
4. **Summarize Text**: Use OpenAI Chat API to summarize each segment into 60 words.
5. **Generate Embeddings**: Pass each segment to the OpenAI Embedding API to get a 1536-dimensional vector representing the semantic meaning of the segment.
6. **Store in Index**: Save all data in an Embedding Index (`embedding_index_3m.json`).

### Vector Databases

- **Purpose**: Store embedding indices for efficient retrieval and search.
- **Examples**: Azure Cognitive Search, Redis, Pinecone, Weaviate.

### Cosine Similarity

- **Definition**: Cosine similarity measures the similarity between two vectors, often referred to as `nearest neighbor search`.
- **Usage**: Vectorize the query text using the OpenAI Embedding API, then calculate the cosine similarity between the query vector and each vector in the Embedding Index. Sort the results by cosine similarity to find the most similar text segments.
- **Mathematical Perspective**: Measures the cosine of the angle between two vectors in multidimensional space, which allows for similarity measurement even if documents differ in size.
