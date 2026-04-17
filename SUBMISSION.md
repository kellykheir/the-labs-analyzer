# Hackathon Submission - The Labs Analyzer

## Project Name
The Labs Analyzer

## Track
**Healthcare Track (Elfie)** - Challenge #3: Lab Report Analysis

## Problem Statement
Patients receive complex lab reports with medical terminology they don't understand. Results lack plain-language explanations, creating anxiety and delaying necessary follow-up care. There's no simple way for patients to get instant, reliable explanations of their lab results.

## Solution
The Labs Analyzer is a web app that:
1. Accepts PDF lab reports via drag & drop
2. Extracts text using pdf.js
3. Parses known lab tests automatically (Hemoglobin, Glucose, Cholesterol, etc.)
4. Analyzes results using Qwen3-32b AI model
5. Returns color-coded, easy-to-understand results with:
   - Patient-friendly summary
   - Key findings highlighted
   - Abnormal results with explanations
   - Actionable next steps

## How It Works
```
PDF Upload → pdf.js (text extraction) → Test Parser → Qwen3-32b (Groq API) → JSON Analysis → UI Display
```

## AI Integration
- **Model:** Qwen3-32b (required by hackathon rules)
- **Provider:** Groq (free tier available)
- **Why Qwen:** Open-source model suitable for deployment in developing countries where major cloud providers may not be available

## Technical Stack
- Single HTML file (no build required)
- React 18 (CDN)
- pdf.js for PDF extraction
- Qwen3-32b via Groq API
- CSS inline styling

## Key Features
- [x] PDF drag & drop upload
- [x] Smart lab test parsing
- [x] AI-powered analysis with Qwen3-32b
- [x] Color-coded results (Normal/Borderline/High/Low/Critical)
- [x] Plain language explanations
- [x] Actionable recommendations
- [x] 4 language support (EN/FR/VN/AR)
- [x] Rate limit handling with auto-retry
- [x] B2C focused (patients)

## Demo
Simply open `index.html` in a browser.

## Compliance
- Qwen model used as required by hackathon rules
- Clear attribution for all components
- Built during hackathon period
- No pre-existing components used without disclosure
