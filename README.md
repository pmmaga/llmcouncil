# The LLM Council

A single-file web app for configuring a "council" of LLMs, sending a prompt to multiple models, and having a designated "speaker" synthesize a combined response.

## Why?

I remember using a desktop tool called Copernic(?) that was a search engine aggregator when it was actually useful to have results from different search engines. I thought it would be useful to have the same thing for LLMs and so I (and Gemini, and Copilot, and GPT) created this simple application. 99% of the code is generated so is the rest of this readme.

## What it does
- Configure multiple LLM integrations (API keys, endpoints, per-model settings).
- Assign one model as the Speaker and 2–6 models as Council Members.
- Send a prompt to each selected model, collect responses, and ask the Speaker to synthesize a final answer.
- Persist configuration and query history in browser localStorage.

## How to use
1. Open `index.html` in a browser (prefer running from a local server).
2. Enter API keys and configure models in the sidebar.
3. Drag one model into the "Speaker" slot and 2–6 models into the "Council Members" area.
4. Enter a prompt and click Send. The app will call each model, then call the Speaker to synthesize output and save the session to history.

## Notes & limitations
- API keys are stored in localStorage.
- Some provider endpoints and response shapes are examples; feel free to contribute fixes or add more models.

## Credits
- Tailwind CSS (CDN)
- marked (Markdown renderer; CDN)
