#  RAG-Based YouTube Summarizer & QA System
A Retrieval-Augmented Generation (RAG) project that extracts YouTube video transcripts and allows users to ask questions or generate summaries using a Hugging Face LLM (Qwen).


##  Features
- Extracts transcripts from YouTube videos
- Splits transcript into chunks for processing
- Generates embeddings using Sentence Transformers
- Stores vectors using FAISS
- Retrieves relevant context using similarity search
- Generates answers using Qwen (Hugging Face API)
- Supports full video summarization
- Enables question answering over video content


##  Architecture
YouTube Video  
↓  
Transcript Extraction (youtube-transcript-api)  
↓  
Chunking (LangChain)  
↓  
Embeddings (Sentence Transformers)  
↓  
FAISS Vector Store  
↓  
Retriever (Similarity Search)  
↓  
Context Injection  
↓  
Qwen LLM (Hugging Face)  
↓  
Final Answer / Summary  


##  Tech Stack
- Python
- LangChain
- FAISS
- Hugging Face Inference API
- Qwen/Qwen2.5-7B-Instruct
- YouTube Transcript API
- Sentence Transformers


##  Installation
pip install youtube-transcript-api  
pip install langchain langchain-community langchain-core  
pip install langchain-huggingface  
pip install sentence-transformers  
pip install faiss-cpu  
pip install huggingface_hub  
pip install python-dotenv  


##  Environment Setup
Create a `.env` file:
HF_TOKEN=your_huggingface_api_token


##  How to Run
1. Clone repo:
git clone https://github.com/aryasmita1/rag-based-youtube-summarizer.git  
cd rag-based-youtube-summarizer  

2. Open Jupyter Notebook:
jupyter notebook  

3. Run steps in order:
- Load YouTube transcript
- Chunk text
- Create embeddings
- Store in FAISS
- Setup retriever
- Initialize LLM
- Run QA or summarization
  

##  Usage
Question Answering:
What is DeepMind discussed in the video?
Summarization:
Summarize the video

##  Example Output
DeepMind is an AI research company focused on reinforcement learning, neural networks, and artificial general intelligence systems.


##  Limitations
- Requires YouTube captions
- Depends on embedding quality
- Hugging Face API latency
- Works best with English videos


##  Future Improvements
- Streamlit chatbot UI
- Multi-video knowledge base
- Conversational memory
- Timestamp-based answers
- Faster local LLM integration

