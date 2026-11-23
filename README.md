# NanoCloud Notes — Hybrid AI Study & Research Workspace

**NanoCloud Notes** is a web application built with the **Firebase AI Logic Hybrid Inference SDK** that intelligently routes AI tasks between on-device execution (Gemini Nano in Chrome) and cloud execution (Gemini in Firebase).

## Live Demo
👉 **Try it live:** https://github.io

## Value Proposition & Why Hybrid AI?
Students and researchers frequently review notes in low-connectivity environments (classrooms, commutes, offline study sessions) while still needing deep synthesis when online:
* **⚡ Quick Summary (`prefer_on_device`):** Prioritizes local execution via Gemini Nano when available on supported Chrome devices for zero-latency, private, offline-capable bullet summaries and key-term extraction, automatically falling back to the cloud on unsupported devices.
* **☁️ Deep Study Guide & Quiz (`prefer_in_cloud`):** Routes complex multi-step reasoning to Gemini in the cloud via Firebase AI Logic to generate structured study guides and practice quiz questions.

## Firebase Products Used
* **Firebase AI Logic SDK:** Runtime hybrid inference (`getAI`, `getGenerativeModel` with `prefer_on_device` and `prefer_in_cloud` modes).
* **Firebase App Check:** Protects backend Gemini API endpoints (configured with a debug token for hackathon judging and testing).
* **Google Analytics for Firebase:** Tracks hybrid inference routing events across on-device and cloud fallbacks.

## How to Run / Test Locally or via GitHub Pages
1. Clone or fork this repository.
2. Open `index.html` and replace `firebaseConfig` and `FIREBASE_APPCHECK_DEBUG_TOKEN` with your own Firebase project credentials (or test directly via the live GitHub Pages link above).
3. Serve `index.html` over HTTPS or `localhost` in Google Chrome.
4. 
