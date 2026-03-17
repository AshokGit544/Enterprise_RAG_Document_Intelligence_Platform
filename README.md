# Enterprise RAG Document Intelligence Platform

## Project Overview
This project simulates an enterprise Retrieval-Augmented Generation (RAG) workflow for manufacturing-style documents similar to the type of document intelligence platform used in large enterprise environments.

The project demonstrates how unstructured enterprise documents can be:
- generated and standardized
- classified into document types
- processed for structured information extraction
- split into retrieval-friendly chunks
- enriched with business metadata
- indexed for retrieval
- searched using top-k similarity retrieval
- used to generate grounded responses from enterprise context

## Business Problem
Foundation models alone do not know a company’s internal documents well enough. In enterprise environments, important answers depend on private internal records such as quality reports, supplier invoices, maintenance notes, and engineering change notices.

Because of that, a model should not rely only on general knowledge. It should first retrieve the most relevant internal document chunks and then generate a response grounded in those retrieved records.

## Project Goal
The goal of this project is to simulate a Ford-style enterprise RAG workflow where:
1. enterprise documents are prepared
2. metadata is enriched
3. chunks are created for retrieval
4. top relevant chunks are retrieved for a question
5. the final answer is generated using retrieved business context

## End-to-End Flow
1. Create synthetic enterprise documents
2. Normalize and preprocess document text
3. Train a document classification workflow
4. Extract structured fields from unstructured text
5. Chunk documents into smaller retrieval units
6. Enrich chunks with metadata
7. Build retrieval-ready indexed text
8. Retrieve top-k relevant chunks for a query
9. Generate a grounded response from retrieved context
10. Evaluate context coverage and groundedness

## Main Features
- enterprise-style synthetic manufacturing documents
- document classification
- regex-based structured field extraction
- chunking for retrieval
- metadata enrichment
- retrieval-ready indexing
- top-k retrieval using TF-IDF and cosine similarity
- grounded response generation
- lightweight RAG evaluation metrics

## Project Structure
enterprise_rag_document_intelligence_platform/
- data/
  - raw_documents/
  - processed_documents/
  - chunked_documents/
  - vector_ready/
  - retrieval_outputs/
- outputs/
- config/

## Output Files
The project generates:
- enterprise_documents.csv
- processed_documents.csv
- documents_enriched.csv
- classification_results.csv
- extracted_entities.csv
- chunked_documents.csv
- vector_ready_records.csv
- top_k_retrieval_results.csv
- grounded_context.txt
- grounded_rag_response.txt
- rag_evaluation_summary.json
- project_summary.json

## How this reflects enterprise RAG work
This project reflects common enterprise RAG design patterns:
- chunking large internal documents into smaller retrieval units
- enriching chunks with business metadata
- building retrieval-ready indexed records
- retrieving top relevant internal context before answer generation
- improving groundedness and reducing unsupported responses

## Tools Used
- Python
- Pandas
- NumPy
- scikit-learn
- TF-IDF
- Cosine Similarity

## Future Enhancements
A stronger production version could add:
- sentence-transformer embeddings
- FAISS or vector databases
- LLM-based answer generation
- RAGAS-style evaluation
- better ranking strategies
- metadata filtering
- API-based serving
