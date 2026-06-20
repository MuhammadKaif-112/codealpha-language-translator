# Language Translation Tool

A simple, browser-based language translation tool built using HTML, CSS, and JavaScript. Users can enter text, select a source and target language, and get an instant translation — with options to copy the result or have it read aloud.

This project was built as part of an internship task.

---

## Features

- Enter any text and select source/target languages from dropdown menus
- Translate text using a live translation API
- Clean, responsive UI that works on desktop and mobile
- Copy translated text to clipboard with one click
- Listen to the translated text using text-to-speech
- Friendly error handling (empty input, failed requests, missing voice support)

---

## Tools & Technologies Used

| Tool / Technology | Purpose |
|---|---|
| **HTML5** | Page structure — text boxes, dropdowns, buttons |
| **CSS3** | Styling — layout (Flexbox), gradients, shadows, responsive design |
| **JavaScript (Vanilla JS)** | Logic — handling clicks, calling the API, updating the page |
| **Fetch API** | Sending requests to the translation API and receiving responses |
| **MyMemory Translation API** | Free, no-signup translation service used to translate text |
| **Web Speech API** (`SpeechSynthesis`) | Built-in browser feature used for text-to-speech playback |
| **Clipboard API** (`navigator.clipboard`) | Used for the "Copy" button functionality |
| **VS Code** | Code editor used to build the project |
| **Live Server (VS Code extension)** | Used for local testing with auto-refresh on save |

---

## How It Works

1. The user types text into the "Enter Text" box and selects a **From** and **To** language.
2. On clicking **Translate**, the JavaScript code sends the text to the MyMemory Translation API using `fetch()`.
3. The API processes the request and returns the translated text as a JSON response.
4. The translated text is displayed in the "Translated Text" box.
5. The user can:
   - Click **Copy** to copy the translated text to their clipboard.
   - Click **Listen** to hear the translation spoken aloud (if a voice for that language is available in the browser/OS).

---

## Why MyMemory API?

Google Translate API and Microsoft Translator both require a paid cloud account and an API key to use. Since this is a student/internship project, the **MyMemory Translation API** was used instead — it's free, requires no signup or API key, and works directly from the browser. This made it possible to build and test the tool without any billing setup.

---

## Known Limitation

Text-to-speech (Listen button) depends on the **voices installed on the user's operating system/browser**, not on the code itself. Major languages like English, Spanish, and French are widely supported, but some languages (e.g., Urdu) may not have a built-in voice on every system. The tool detects this and shows a clear message instead of failing silently.

---

## How to Run

1. Download/clone the project folder.
2. Open `index.html` in any modern web browser (Chrome, Edge, Firefox).
   - Optional: Use the **Live Server** extension in VS Code for auto-refresh during development.
3. Type text, select languages, and click **Translate**.

No installation, build steps, or API keys are required.

---

## Project Structure

```
translator/
└── index.html   (contains all HTML, CSS, and JavaScript)
```

---

## Author

Muhammad Kaif — BS Artificial Intelligence
Built as part of internship task submission.
