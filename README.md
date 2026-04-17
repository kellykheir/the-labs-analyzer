# The Labs Analyzer

AI-powered lab report analysis for patients. Built for **Elfie Healthcare Track** at **Qwen AI Build Day**.

## Demo

Simply open `index.html` in a browser, enter your Groq API key, and upload a PDF lab report.

## Features

- **PDF Upload** - Drag & drop or click to upload
- **Smart Parsing** - Extracts known lab tests (Hemoglobin, Glucose, Cholesterol, etc.)
- **Qwen AI Analysis** - Uses Qwen3-32b via Groq API for clinical analysis
- **4 Language Support** - English, French, Vietnamese, Arabic
- **Color-coded Results** - Normal (green), Borderline (yellow), High (orange), Low (blue), Critical (red)
- **Plain Language** - Medical terms explained simply
- **Actionable Next Steps** - Specific recommendations per abnormal result
- **Rate Limit Handling** - Automatic retry with user-friendly messages

## How It Works

```
PDF → pdf.js (text extraction) → Test Parser → Qwen3-32b (Groq) → JSON → UI
```

## Setup

1. Open `index.html` in a browser
2. Enter your Groq API key when prompted
3. Upload a PDF lab report
4. Get instant analysis!

## Getting a Groq API Key

1. Go to https://console.groq.com
2. Sign up / Log in
3. Create an API key
4. Paste it in the app

## Tech Stack

- **Frontend**: React 18 (CDN), Single HTML file
- **PDF**: pdf.js (CDN)
- **AI**: Qwen3-32b via Groq API
- **No build required** - Just open in browser

## AI Integration

This project uses **Qwen3-32b** as required by the hackathon rules. The model is accessed via Groq API for fast inference suitable for developing countries where major cloud providers may not be available.

## For Hackathon Submission

- **Live Demo**: Open `index.html` on local server
- **Screenshots**: UI showing analysis results
- **Video**: Screen record the upload → analysis flow
- **Repository**: This codebase

## Sample Data

A sample PDF lab report is included: `726730472-Health-Checkup-Report.pdf`

## License

MIT
