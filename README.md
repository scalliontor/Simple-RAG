# Simple RAG

## Simple RAG with basics use: uploading pdf and extract information in it
- Upload a PDF document
- Split the content into fixed length chunks
- Generate embeddings using bkai-foundation-models/vietnamese-bi-encoder (for embedding) 
- Store and index embeddings into a vector database
- Use lmsys/vicuna-7b-v1.5 (for response) as the local LLM
- Enable chat-based querying through a RAG pipeline


# Simple Agentic RAG System


## **Same Model Configuration as Original**
- **LLM**: `lmsys/vicuna-7b-v1.5` with 4-bit NF4 quantization
- **Embeddings**: `bkai-foundation-models/vietnamese-bi-encoder`
- **Text Splitter**: SemanticChunker with Vietnamese embeddings
- **Vector Database**: Chroma

## **Added Agentic Features (Simplified)**
- **Multiple Tools**: Document search, web search, calculator, summarizer
- **Simple Tool Selection**: Basic logic to choose appropriate tools
- **Interactive Interface**: Chat functionality

### How to use:
- Run: simple_chat() to start interactive mode
- Or test individual queries: agentic_rag('your question')
- Available commands in chat: 'quit', 'memory', 'clear'