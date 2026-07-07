# Youtube Video Summarizer using Extension ▶️

## 📌 Introduction

Youtube Video Summarizer is a browser-extension-based project that summarizes the currently open YouTube video by using its transcript. The project consists of:

- ✅ A Flask API endpoint (`/summary`) in Python
- ✅ Transcript extraction using `youtube-transcript-api`
- ✅ Text summarization using Hugging Face `transformers` pipeline
- ✅ A Chromium extension popup that calls the local API and displays the summary

---

## 🔄 Process / Flow

1. User opens a YouTube video in a Chromium browser tab.
2. User clicks the extension popup and presses the Summarise button.
3. Extension reads the active tab URL.
4. Extension sends a GET request to `http://127.0.0.1:5000/summary?url=<video_url>`.
5. Flask API extracts the YouTube video ID from the URL.
6. Transcript text is fetched using `youtube-transcript-api`.
7. Transcript is summarized in chunks using `transformers` summarization pipeline.
8. Summary text is returned by the API and displayed in the extension popup.

---

## 🛠️ Technology Used

| Component | Technology |
|-----------|-----------|
| Backend API | Python + Flask |
| Transcript Fetching | youtube-transcript-api |
| NLP Summarization | transformers pipeline |
| Extension UI | HTML + JavaScript |
| Browser Extension Standard | Chrome Manifest V3 |

---

## 🎓 Skills Gained

### Backend Development

- ✅ Building a lightweight REST endpoint using Flask
- ✅ Parsing and validating URL query input for API processing
- ✅ Connecting API logic to NLP summarization flow

### NLP Integration

- ✅ Extracting video transcripts with `youtube-transcript-api`
- ✅ Applying transformer-based summarization in Python
- ✅ Handling long transcript text through chunk-wise summarization

### Browser Extension Development

- ✅ Creating a Manifest V3 extension structure
- ✅ Reading active tab URLs with Chrome extension APIs
- ✅ Integrating popup UI actions with backend API calls
- ✅ Rendering asynchronous API responses in extension UI

---

## 📂 Project Structure

```text
Youtube-Video-Summarizer-main/
├── README.md
└── YouTube-Video-Summariser-main/
    ├── app.py
    └── extension/
        ├── manifest.json
        ├── popup.html
        ├── popup.js
        └── images/
```

---

## ⚙️ Setup Instructions

### ✅ Prerequisites

- ✅ Python modules:
  - `flask`
  - `youtube-transcript-api`
  - `transformers`
- ✅ A Chromium-based browser for loading the extension
- ✅ Local API access at `http://127.0.0.1:5000`

### 📦 Installation

```bash
pip install flask youtube-transcript-api transformers
```

### ▶️ Run Backend API

```bash
python app.py
```

### 🧩 Load Extension

1. Open browser extensions page (`chrome://extensions` in Chrome).
2. Enable Developer mode.
3. Click Load unpacked.
4. Select the folder:

```text
YouTube-Video-Summariser-main/extension/
```

### 🕹️ Usage

1. Open any YouTube video page.
2. Click the extension icon.
3. Press Summarize.
4. Wait for the summary to appear in the popup.

