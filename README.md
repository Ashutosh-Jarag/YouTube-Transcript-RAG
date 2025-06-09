# YouTube Transcript RAG
Overview
YouTube Transcript RAG is a Python-based project that implements a Retrieval-Augmented Generation (RAG) system to process and query YouTube video transcripts. It fetches transcripts, creates embeddings, stores them in a FAISS vector store, and uses a language model to answer questions based on the transcript content. The system leverages LangChain for RAG pipeline construction and integrates with OpenAI and Google Generative AI models.
Features

Fetches YouTube video transcripts using the youtube-transcript-api.
Splits transcripts into manageable chunks with RecursiveCharacterTextSplitter.
Generates embeddings using OpenAI or Google Generative AI embeddings.
Stores embeddings in a FAISS vector store for efficient retrieval.
Answers user queries by retrieving relevant transcript segments and generating responses with a language model (Gemini-1.5-Pro).
Utilizes LangChain's RunnableParallel for efficient query processing.

Requirements
To run this project, ensure you have Python 3.11 or later installed. The required packages are listed in requirements.txt. Install them using:
pip install -r requirements.txt

Key Dependencies

langchain-openai: For OpenAI embeddings and chat models.
langchain-google-genai: For Google Generative AI embeddings and chat models.
langchain-community: Community tools including FAISS.
youtube-transcript-api: To fetch YouTube transcripts.
faiss-cpu: Vector store for embeddings.
tiktoken: Tokenization for OpenAI models.
python-dotenv: Environment variable management.
requests, duckduckgo-search, jupyter, ipywidgets: Additional utilities.

Setup

Clone the Repository (if applicable):
git clone <repository-url>
cd youtube-transcript-rag


Install Dependencies:
pip install -r requirements.txt


Set Environment Variables:Create a .env file in the project root and add your API keys:
OPENAI_API_KEY=your_openai_api_key
GOOGLE_API_KEY=your_google_api_key

Load the environment variables in your notebook:
import os
from dotenv import load_dotenv
load_dotenv()


Run the Notebook:Open YT_RAG.ipynb in Jupyter Notebook or JupyterLab:
jupyter notebook

Execute the cells sequentially to set up the RAG pipeline and query the system.


Usage

Load the Notebook: Open YT_RAG.ipynb and run the initial cells to install dependencies and import libraries.
Fetch Transcripts: Provide a YouTube video ID to fetch its transcript using YouTubeTranscriptApi.
Index Transcripts: The transcript is split, embedded, and stored in a FAISS vector store.
Query the System: Use the provided chain to ask questions about the video content. For example:result = main.invoke("What is DeepMind?")
print(result)


Example Query: The notebook includes examples like querying whether nuclear fusion is discussed and retrieving relevant transcript segments.

Project Structure

YT_RAG.ipynb: Main Jupyter notebook containing the RAG implementation.
requirements.txt: List of Python dependencies.
.env: Environment file for API keys (not included in version control).
README.md: Project documentation (this file).

Notes

Ensure you have valid API keys for OpenAI and Google Generative AI.
The notebook uses gemini-1.5-pro with a temperature of 0.2 for consistent responses.
FAISS is CPU-based; for GPU support, consider installing faiss-gpu.
Handle TranscriptsDisabled exceptions for videos without transcripts.

Contributing
Contributions are welcome! Please submit issues or pull requests for bug fixes, feature additions, or documentation improvements.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgments

Built with LangChain for RAG pipeline.
Uses YouTube Transcript API for transcript fetching.
Inspired by advancements in AI and conversational systems.

