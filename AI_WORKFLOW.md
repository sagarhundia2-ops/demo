# 🧠 Vibe Coding & Prompt Engineering Log

The theme of this hackathon is **Vibe Coding**—using AI to build faster, think in ideas, and use prompts as our primary interface. 

## 0. The "Vibe Coding" Stack
To build this at lightning speed, we used the following AI Developer Stack:
* **IDE:** Antigravity
* **Architecture & Complex Logic:** Claude opus 4.6 (via antigravity)
* **API Research & Bug Fixing:** Gemini 1.5 Pro
* **Frontend Generation:** v0.dev & Cursor

Here is exactly how we directed these models to build Dial2AI.

## 1. Zero-to-One Architecture Generation
We did not write boilerplate. We used high-level architectural prompts to generate the entire foundation.

**Our Prompt:**
> "I want to build a Python FastAPI backend that receives real-time WebSocket audio from an Exotel phone call (8kHz PCM). It needs to buffer the audio, detect 2 seconds of silence, run Google Gemini STT to transcribe the Hindi audio, and then use Gemini to generate a response. Generate the `main.py` and `stream.py` WebSocket routes."

**The Result:** AI generated a fully functional WebSocket server with structural buffering logic, saving us ~8 hours of reading Twilio/Exotel streaming documentation.

## 2. Advanced Algorithmic Prompting (The Noise Gate)
We ran into a critical real-world problem: Exotel telecom lines have constant background static. The AI kept transcribing the static as "Hello? Kaun bol raha hai?". 

Instead of manually writing signal processing code, we vibed it:
**Our Prompt:**
> "My WebSocket audio stream (16-bit PCM 8000Hz) is picking up telecom line static. Write a Python function `contains_speech(audio_chunk, threshold)` that unpacks the bytes and calculates the peak amplitude. If the peak amplitude is below the threshold, it should return False so I can ignore the static."

**The Result:** We got a perfect amplitude-based noise-gate filter in 5 seconds.

## 3. Intelligent Intent Routing
We needed the AI to stop hallucinating Mandi prices and Weather. We used Prompt Engineering to force Gemini to act as a router before generating the final response.

**The Routing Prompt (in `llm.py`):**
```python
intent_prompt = f"""
Classify the intent of the following user question into one of these categories: 'weather', 'mandi', 'scheme', or 'general'.
If 'weather', extract the location (e.g. Nashik).
If 'mandi', extract crop (e.g. tomato) and location.
If 'scheme', extract scheme name.
Question: {question}
Return ONLY valid JSON: {{"intent": "weather", "location": "nashik", "crop": "", "scheme": ""}}
"""
```
**The Result:** By prompting the LLM to output strict JSON, we created a deterministic API router inside our AI pipeline.

## 4. Generating the React Dashboard in One Shot
For the frontend, we didn't waste time writing CSS. 
**Our Prompt:**
> "Generate a complete Next.js dashboard using TailwindCSS and Recharts. It should have a dark, sleek, modern 'AI' vibe (bg-gray-950). Include 5 stat cards at the top (Total Calls, Success, Failed, Avg Length, Leads). Below that, put a line chart for 'Calls per Hour', and a recent calls table. Use standard Next.js components."

**The Result:** The entire `frontend/pages/index.js` was generated, fully styled, leaving us to only wire up the `fetch` calls to our backend.

## 5. Automated AI Call Analytics
After the call ends, we don't just hang up. We use AI to analyze the data.

**The Post-Call Prompt:**
```text
Analyze the following phone call conversation history and extract the following structured details:
1. Customer Name
2. Primary Intent
3. Outcome
4. Overall Sentiment
5. Call Summary (1 sentence)
6. Lead Information
Return strictly as JSON.
```

## 🚀 Conclusion
We did not type out loops and conditionals; we **directed an AI workforce**. By treating the LLM as our junior developer, data analyst, and frontend designer, we executed a startup-grade product in a fraction of the time a traditional engineering team would take. This is the power of Vibe Coding.
