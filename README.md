# 🎥 AI Video Assistant with RAG

An AI-powered video assistant that converts video content into structured insights and enables interactive question-answering over the video transcript.

The system processes a YouTube video or local audio/video file, transcribes the content using Whisper, generates AI-powered summaries and insights using Mistral AI, and provides a RAG-based chat interface for asking questions about the video.

---

## ✨ Features

- 🎬 YouTube video processing
- 📁 Local audio/video file support
- 🎙️ Speech-to-text transcription using Whisper
- 📝 Automatic video title generation
- 📋 AI-generated meeting/video summaries
- ✅ Action item extraction
- 🔑 Key decision extraction
- ❓ Open question extraction
- 🔎 Retrieval-Augmented Generation (RAG)
- 💬 Interactive chat with the video content
- 🧠 Vector search using Hugging Face embeddings and ChromaDB
- 🖥️ Streamlit-based web interface

---

## 🏗️ Architecture

```text
YouTube URL / Local File
          │
          ▼
   Audio Processing
          │
          ▼
     Audio Chunking
          │
          ▼
   Whisper Transcription
          │
          ▼
     Video Transcript
          │
          ├───────────────┐
          ▼               ▼
   Mistral AI          Vector Store
          │              │
          ├── Summary    │
          ├── Title      │
          ├── Actions    │
          ├── Decisions  │
          └── Questions  │
                         │
                         ▼
                   RAG Pipeline
                         │
                         ▼
                  Interactive Chat
