Intelligent Video Information Retrieval using RAG :

This project implements a Retrieval-Augmented Generation (RAG) pipeline to perform semantic search, topic detection, timestamp extraction, summarization, and question answering from YouTube videos and general video files.
The system enables users to ask natural-language questions and receive context-aware answers grounded strictly in video transcripts.

Project Overview
The project supports two modes:

1) YouTube Video RAG
 Fetches YouTube transcripts with timestamps
 Performs semantic retrieval over transcript chunks
 Answers whether a topic is discussed, with exact timestamps
2) General Video RAG
 Extracts audio from video files
 Transcribes audio using Whisper
 Builds a FAISS vector index for retrieval
Supports QA, topic detection, and summarization
Both pipelines use LLMs + embeddings + FAISS to ensure accurate, grounded responses.

Key Features :
Semantic search over video transcripts
Topic-based content detection (YES / NO)
Exact timestamp extraction (MM:SS format)
Video content summarization
Context-aware question answering
Supports YouTube videos and local video files
Strictly transcript-grounded responses (no hallucinations).

Tech Stack :

Python
LangChain
FAISS Vector Store
HuggingFace Embeddings
Google Gemma-2-2B-IT
Faster-Whisper (for video transcription)
NLP & Prompt Engineering.

Workflow :
1️)Transcript Ingestion

YouTube transcripts via youtube-transcript-api

Video transcription via Faster-Whisper

2️)Chunking & Indexing

Timestamp-aware chunk creation

Embedding generation

Storage in FAISS vector database

3️) Retrieval

Similarity-based retrieval using embeddings

4️) Augmentation & Generation

Retrieved chunks passed to LLM

Structured prompts enforce grounded answers

Outputs include explanations, summaries, and timestamps.
