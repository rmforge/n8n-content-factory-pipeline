# n8n-content-factory-pipeline
Scaling content output by repurposing video assets into multi-channel posts using AI.
# 🎬 Automated "Content Factory" Pipeline

This pipeline transforms one long-form video into multiple finished social media assets, allowing content teams to scale output by 400% without increasing headcount.

**Problem Solved:** The manual, multi-day process of transcribing, clipping, copywriting, and scheduling social posts from video content.

## Architecture & Features

### 1. Video Analysis & Creative AI
The workflow treats the raw video file as the single source of truth for all content.

* **Ingestion:** Triggered by a file upload event (Google Drive).
* **Transcription:** Uses an LLM (Whisper model) to analyze and transcribe the video content.
* **Viral Ghostwriter Agent:** An AI Agent is prompted to generate distinct content formats (Twitter threads, LinkedIn posts, Newsletter sections) from the single transcript, matching brand voice guidelines.
* **Human-in-the-Loop:** Drafts are routed to a Notion/Airtable calendar for final editorial review and approval before publishing.

### 2. Output and Impact
The system ensures consistent brand presence and frees up creative staff for strategy.


## Files in this Repository

* `content_factory_pipeline.json`: The sanitized n8n workflow file.
* `README.md`: This document.

## How to Run Locally

1.  Import the workflow file.
2.  Configure the OpenAI/Deepgram API for transcription and the Notion/Airtable credential.
3.  Simulate a file upload to test the full pipeline.
