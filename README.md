# RAG Chatbot with Multi-Modal Input Support

## 🚀 Overview
This project is an advanced **Retrieval-Augmented Generation (RAG) chatbot** built with **Python** and **Streamlit**, capable of handling multiple file types, web pages, and YouTube video transcriptions. The chatbot first summarizes the input and then enables users to ask questions based on the extracted content.

## ✨ Features
- 📂 **Multi-File Upload Support**: Accepts **PDF, DOCX, CSV, Images, Videos, and Audio** files.
- 🌐 **URL Processing**: Extracts text from **web pages** and **YouTube videos** (via subtitles).
- 🔍 **Retrieval-Augmented Generation (RAG)**: Retrieves relevant text chunks before answering queries.
- 📝 **Automatic Summarization**: Provides a summary of the uploaded document before Q&A.
- 🎥 **Speech-to-Text for Videos & Audio**: Converts spoken words into text using **OpenAI Whisper**.
- 🖼️ **Image Text & Caption Extraction**: Extracts text from images via **OCR (Tesseract)** and generates captions using **BLIP**.
- 🔥 **Optimized for Performance**: Utilizes **FAISS** for fast semantic search and **transformers** for summarization & embeddings.

## 📥 Supported Input Formats
| Input Type    | Processing Method |
|--------------|------------------|
| **PDF**      | Extracts text using `pdfplumber` |
| **DOCX**     | Reads content using `python-docx` |
| **CSV**      | Provides summary stats using `pandas` |
| **Images**   | Extracts text with `pytesseract` and captions via `BLIP` |
| **Videos**   | Extracts audio and transcribes using `Whisper` |
| **Audio**    | Converts speech-to-text via `Whisper` |
| **Web Pages** | Scrapes text from HTML using `BeautifulSoup` |
| **YouTube**  | Retrieves subtitles via `YouTubeTranscriptApi` |

## 🧠 Models Used
| Task | Model |
|------|-------|
| **Summarization** | `facebook/bart-large-cnn` (Hugging Face) |
| **Sentence Embeddings** | `all-MiniLM-L6-v2` (Sentence Transformers) |
| **Text Extraction from Images** | `pytesseract` (OCR) |
| **Image Captioning** | `Salesforce/blip-image-captioning-base` |
| **Speech-to-Text** | `OpenAI Whisper` & `Faster-Whisper` |
| **Text Retrieval** | `FAISS` (Facebook AI Similarity Search) |

## 🛠️ Installation
```bash
pip install torch transformers faiss-cpu sentence-transformers pdfplumber pymupdf python-docx pytesseract openai-whisper beautifulsoup4 requests youtube_transcript_api pytube moviepy
```

Additionally, install `tesseract-ocr` for image text extraction:
```bash
sudo apt-get install -y tesseract-ocr
```

## 🚀 Running the Chatbot
Run the chatbot using Streamlit:
```bash
streamlit run app.py
```

## 🎯 How It Works
1. **Upload a file or provide a URL** (web page or YouTube link).
2. The chatbot extracts, processes, and **summarizes** the content.
3. You can then **ask questions** based on the uploaded data.
4. The chatbot **retrieves relevant context** using FAISS.
5. It generates a final **AI-driven answer** using the summarized content.

## 🔗 Future Enhancements
- 🔄 **Real-time API support** for live document updates.
- 💬 **Better UI/UX** with a more interactive **ChatGPT-like interface**.
- 🏎️ **GPU Optimization** for even faster processing.

## 🤝 Contributing
Feel free to contribute via pull requests or report issues. Let’s build something amazing! 🚀

