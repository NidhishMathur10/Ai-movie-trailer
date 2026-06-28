# AI-Powered Cinematic Trailer Generator 🎬🤖

An automated Python pipeline that transforms a simple movie title and genre into a fully realized, multi-scene cinematic trailer. By orchestrating generative language models, asynchronous text-to-speech, and programmatic video editing, this project completely streamlines the multi-modal content creation workflow.

## 🚀 Features

* **Automated Scriptwriting:** Generates a structured 3-scene concept, complete with detailed visual direction and narration scripts using **Google Gemini 2.5 Flash**.
* **Contextual Imagery:** Leverages precise prompts provided by Gemini via **Google AI Studio** to generate high-quality scene visuals.
* **Async Audio Synthesis:** Converts narrative text into high-quality, natural-sounding voiceovers instantly using **Edge-TTS** and Python's `asyncio`.
* **Programmatic Video Editing:** Converts images into timed clips, applies smooth fade transitions, overlays the generated voiceover track, and exports the final video automatically using **MoviePy**.

---

## ⚙️ How It Works (The Pipeline)

1. **The Concept:** The user inputs a movie title and its genre.
2. **The Script:** Gemini 2.5 Flash acts as the creative director, spitting out 3 sequential scenes detailing exact image prompts and voiceover lines.
3. **Asset Generation:** * Visual prompts are processed via Google AI Studio to generate the scene backdrops.
   * Concurrently, `edge-tts` leverages `asyncio` to quickly turn the text scripts into high-quality `.mp3` voiceover files.
4. **The Final Cut:** MoviePy brings it all together by transforming the static scene images into timed video clips, applying smooth fade-in/fade-out transitions, stitching them into a unified video track, syncing the master audio, and rendering out the final `cinematic_trailer.mp4`.

---

## 🛠️ Tech Stack

* **Core Logic & Prompting:** Google Gemini 2.5 Flash (Google AI Studio)
* **Audio Generation:** Edge-TTS
* **Video Compositing:** MoviePy
* **Orchestration:** `asyncio`

---

## 💻 Getting Started

### Prerequisites

Make sure you have Python installed, then install the required dependencies:

```bash
pip install moviepy edge-tts google-generativeai
