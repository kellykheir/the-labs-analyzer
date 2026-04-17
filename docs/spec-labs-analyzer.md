# The Labs Analyzer - Design Spec

## Project Overview
- **Name:** The Labs Analyzer
- **Track:** Healthcare Track (Elfie) - Challenge #3
- **Purpose:** AI-powered lab report analysis for patients
- **Target Users:** B2C patients receiving lab results

## Problem Statement
Patients receive complex lab reports they don't understand. Results are in medical terminology with no plain-language explanation. This creates anxiety and delays necessary follow-up actions.

## Solution
An AI-powered web app that:
1. Accepts PDF lab reports
2. Extracts text using pdf.js
3. Analyzes results via Qwen3-32b (Groq)
4. Returns color-coded, easy-to-understand results with recommendations

## Architecture
```
PDF Input → pdf.js (text extraction) → Qwen3-32b (Groq API) → JSON Parser → React UI
```

## Stack
- Single HTML file with embedded React+Babel
- pdfjs-dist for PDF text extraction
- Qwen3-32b via Groq API (60 req/min, 500K tokens/day)
- CSS inline (no external dependencies)

## Features
1. **PDF Upload** - Drag & drop or click to browse
2. **Automatic Analysis** - Extracts all lab tests from report
3. **Color-coded Results** - Normal/Borderline/High/Low/Critical with visual badges
4. **Patient-friendly Summary** - 2-3 sentences in plain language
5. **Key Findings** - Top 3 important points
6. **Next Steps** - Actionable recommendations per abnormal result
7. **Language Support** - EN default (FR/VN extensible)

## Data Structure (JSON Output)
```json
{
  "patient_summary": "string",
  "overall_status": "normal|attention|urgent",
  "tests": [
    {
      "name": "string",
      "value": "string",
      "unit": "string",
      "reference_range": "string",
      "status": "normal|borderline|high|low|critical",
      "explanation": "string",
      "next_step": "string"
    }
  ],
  "key_findings": ["string"],
  "urgent_action_required": boolean
}
```

## Future Extensibility
- Image input (lab scan photos) via OCR → Qwen
- Multi-language support (AR, VN, FR, EN)
- Integration with Elfie existing infrastructure

## Deliverables
- Single HTML file (working prototype)
- Live demo
- Screenshots for submission
- GitHub repository

## Constraints
- Must use Qwen model (strict requirement)
- Can combine with other AI tech (disclose in submission)
- Build during hackathon period (no pre-existing components without attribution)