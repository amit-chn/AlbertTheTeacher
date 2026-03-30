# Albert & Berta Classroom 🇩🇪🍺

A specialized AI-powered German learning application built with **Streamlit** and **Google Gemini API**. 

This tool is explicitly designed to bridge the gap between strict **C1/C2 Academic German** and **Munich Street Casual / Bavarian slang**.

## 🧠 The Core Concept

Instead of a generic chatbot, this app utilizes a dual-persona architecture:
* **Professor Albert:** A brutally honest, highly analytical linguistics professor. He focuses strictly on grammar, syntax, and C1-level academic vocabulary.
* **Berta:** Albert's mother, a traditional pub owner in Munich. She provides the casual, street-level Bavarian translations so you don't sound like a textbook at the bar.

## ✨ Key Features

* **Contextual Language Detection:** * Inputs in **Hebrew/English** trigger a "Learning Mode" (Translations, Etymology, and Mnemonics).
    * Inputs in **German** trigger "Review Mode" (Grammar correction and academic elevation).
* **Anki Deck Automation:** The app uses hidden JSON generation to extract exactly 10 relevant B1-C1 vocabulary words per interaction and generates a formatted **CSV file** ready for immediate import into Anki.
* **Session Memory:** Built with Streamlit's `session_state` to maintain full chat history during the learning session without resetting on every prompt.
* **Smart Rate Limiting:** Actively catches Google API `429 ResourceExhausted` errors and parses the server response to tell the user exactly how many seconds to wait.
* **Static Asset Integration:** Uses pre-rendered situational images (Strict, Facepalm, Proud, etc.) to enhance UI without the latency cost of dynamic image generation.

## 🛠️ Tech Stack

* **Frontend & Logic:** Python, Streamlit
* **LLM Engine:** Google Generative AI (`gemini-2.5-flash`)
* **Data Handling:** Regex (`re`), JSON (`json`)
