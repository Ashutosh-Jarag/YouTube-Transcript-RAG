🎥 YouTube Transcript RAG 🚀
Welcome to YouTube Transcript RAG—a fun and powerful Python project that lets you dive into YouTube video transcripts like a pro! 📜 This Retrieval-Augmented Generation (RAG) system fetches transcripts, transforms them into searchable embeddings, and answers your questions with the help of advanced AI models. Whether you're curious about a video's content or need quick insights, this project has you covered! 😎
🌟 What’s This All About?
This project uses the magic of LangChain, FAISS, and AI models (like OpenAI and Google’s Gemini) to:

📥 Fetch YouTube video transcripts using the youtube-transcript-api.
✂️ Split transcripts into bite-sized chunks for easy processing.
🧠 Embed text into vectors with OpenAI or Google Generative AI.
🔍 Store embeddings in a FAISS vector store for lightning-fast retrieval.
💬 Answer your questions by combining relevant transcript snippets with AI-generated responses.

Perfect for researchers, content creators, or anyone who wants to extract knowledge from YouTube videos without watching them all! 🎉
🛠️ Features

Transcript Extraction: Grab transcripts from any YouTube video (if available).
Smart Chunking: Splits text into manageable pieces with RecursiveCharacterTextSplitter.
Vector-Powered Search: Uses FAISS for efficient similarity searches.
AI-Powered Answers: Leverages gemini-1.5-pro or OpenAI models for accurate, context-aware responses.
Flexible Pipeline: Built with LangChain’s RunnableParallel for seamless query processing.
Interactive Notebook: Run everything in a Jupyter notebook for easy experimentation.

📋 Requirements
To get started, you’ll need Python 3.11+ and the following dependencies. Install them with:

cmd - "pip install -r requirements.txt"

Key Dependencies

langchain-openai: For OpenAI embeddings and chat models.
langchain-google-genai: For Google’s Gemini models and embeddings.
youtube-transcript-api: Fetches YouTube transcripts.
faiss-cpu: Stores embeddings for fast retrieval.
tiktoken: Tokenization for OpenAI models.
python-dotenv: Manages API keys.
requests, duckduckgo-search, jupyter, ipywidgets: Extra utilities for a smooth experience.

See the full list in requirements.txt.
🚀 Getting Started
Follow these steps to set up and run the project:

1.Clone the Repository (if you’re using Git):
 - git clone https://github.com/your-username/youtube-transcript-rag.git
 - cd youtube-transcript-rag


2.Install Dependencies:
 - pip install -r requirements.txt


3. Set Up API Keys:Create a .env file in the project root and add your API keys:

 OPENAI_API_KEY=your_openai_api_key
 GOOGLE_API_KEY=your_google_api_key

4.Load them in the notebook:
 - from dotenv import load_dotenv
 - load_dotenv()


5. Launch Jupyter Notebook:Open YT_RAG.ipynb in Jupyter:
 - jupyter notebook


6. Run the Notebook:Execute the cells to:

Fetch a YouTube transcript by video ID.
Index the transcript in a FAISS vector store.
Ask questions like, “What’s DeepMind?” or “Does this video talk about nuclear fusion?”



🎮 How to Use It

Open the Notebook: Fire up YT_RAG.ipynb in Jupyter Notebook or JupyterLab.
Fetch a Transcript: Enter a YouTube video ID to grab its transcript.
Index the Content: The system splits and embeds the transcript automatically.
Ask Away!: Query the system with questions about the video. Example:result = main.invoke("What is the main topic of the video?")
print(result)


Explore Results: Get concise answers with relevant transcript snippets.

📂 Project Structure

YT_RAG.ipynb: The main Jupyter notebook with the RAG pipeline.
requirements.txt: List of required Python packages.
.env: Stores API keys (keep this private!).
README.md: You’re reading it! 😄

⚠️ Notes & Tips

API Keys: Make sure you have valid OpenAI and Google API keys.
Model Settings: The notebook uses gemini-1.5-pro with a temperature of 0.2 for reliable responses.
FAISS: This project uses faiss-cpu. For faster performance on large datasets, try faiss-gpu.
Error Handling: Watch out for TranscriptsDisabled errors if a video lacks transcripts.
Experiment: Tweak chunk sizes or model parameters in the notebook for better results.

🤝 Contributing
Got ideas to make this project even cooler? 🌈 Submit issues, feature requests, or pull requests on GitHub. We’d love to hear from you!
📜 License
This project is licensed under the MIT License. Check out the LICENSE file for details.
🙌 Acknowledgments

LangChain: For powering the RAG pipeline.
YouTube Transcript API: For making transcript fetching a breeze.
xAI: For inspiring AI-driven projects like this one! 🚀

Happy querying, and enjoy exploring the world of YouTube transcripts! 🎬
