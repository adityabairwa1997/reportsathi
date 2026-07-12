# ReportSathi

**Your medical reports, explained simply.**

ReportSathi is a web app that reads medical test reports (PDF, image, or text) and presents a clear, plain-language summary — currently in English and Hindi, with more Indian regional languages planned.

## Status: Prototype

This is a single-file HTML prototype, built to validate the core flow before investing in a full architecture.

## How it works

1. User uploads a lab/diagnostic report (PDF, JPG, PNG, or TXT)
2. User picks a language (English / हिंदी)
3. The file is sent to the Claude API with a structured prompt
4. Claude extracts each test result and returns plain-language explanations as JSON
5. Results render as color-coded cards: test name, value, normal range, status (normal / watch / attention), explanation, and a gentle next-step suggestion

## Tech

- Single-file HTML/CSS/JS — no build step, no backend
- Claude Haiku API (`claude-haiku-4-5`) for extraction + explanation
- Client-side only — files are not stored or persisted anywhere

## Safety notes

- Visible disclaimer on every screen: this is not a diagnosis and does not replace a doctor
- No file storage beyond the browser session
- Status language is kept calm and non-alarming, especially for "attention" results

## Roadmap

- [ ] Expand to additional Indian regional languages (Bengali, Tamil, Telugu, Marathi, etc.)
- [ ] Move file processing server-side for privacy and larger file support
- [ ] User testing on real (de-identified) lab reports across formats
- [ ] Domain registration and public deployment
- [ ] Accessibility pass (screen readers, font scaling, color-blind-safe status indicators)

## Disclaimer

ReportSathi is an informational tool only. It does not provide medical diagnoses and is not a substitute for professional medical advice. Always consult a qualified healthcare provider about your test results.
