# 🎤 HackIndia Showdown Pitch Script: GramAI
*Time limit: 3 Minutes. Speak with high energy and confidence. Emphasize the keywords in **bold**.*

---

## 🎬 [0:00 - 0:30] The Hook & Problem (Criterion: Problem Solving)
"Hello Judges, we are Team Git Push Pray. 

Right now, in 2026, there are over **150 Million Indian farmers** who do not have a smartphone. They do not have 4G internet. They cannot use the cool web apps or ChatGPT wrappers everyone else is building today. 

Because of this digital divide, they get scammed by middlemen, they don't know the real Mandi prices, and they miss out on critical government schemes.

We asked ourselves: How do we bring the power of Generative AI to someone who only has a **10-year-old Nokia feature phone?**

The answer is **GramAI**."

## 🚀 [0:30 - 1:15] The Solution & Demo (Criterion: Innovation & Demo)
"GramAI is an AI Voice Assistant over a **simple phone call**. No apps. No internet.

*Let me show you live.* 
**(Action: Put your phone on speaker and dial the Exotel number. Show the phone to the camera).**

*(AI answers: "Namaste! GramAI mein aapka swagat hai...")*

**(You say):** *"Mera naam Ramesh hai. Aaj Nashik mein pyaz ka kya rate chal raha hai?"*

**(Action: Explain while the AI processes for 1-2 seconds)**
"Right now, our backend is streaming my audio via WebSockets, transcribing my Hinglish in real-time, extracting my intent, and hitting the live Data.gov.in API to get the real price."

*(AI answers with the live Nashik onion price).*

"This isn't a hallucination. That is **real-time live data** injected into the LLM context mid-conversation."

## 🧠 [1:15 - 2:00] The AI Magic (Criterion: Use of AI)
"To make this work seamlessly, we had to solve several hard engineering problems using AI:
1. **The Static Problem:** Telecom lines have terrible static. We wrote a custom amplitude-based noise gate to filter out Exotel's line static so the AI doesn't hallucinate background noise.
2. **Intent Routing:** We use Gemini 3.5 Flash to rapidly classify the caller's intent—whether they are asking about Weather, Mandi Prices, or Schemes—and we route the API calls accordingly.
3. **Barge-in Detection:** If the farmer interrupts the AI, it instantly stops speaking and listens, just like a real human."

## 📊 [2:00 - 2:30] The Business Value & Speed (Criterion: Execution Speed)
"But we didn't just build a bot. We built a **platform**. 

**(Action: Share screen showing the Next.js Dashboard)**
As you can see on our real-time Next.js dashboard, every single call is logged. Our AI automatically extracts the **Call Summary, Customer Sentiment, and Lead Information**. 

And look at this—**(Show your phone screen)**—as soon as the call ended, our system sent me an **SMS with a text summary** of my query. 

We built this entire full-stack platform—FastAPI, WebSockets, Next.js, 3 API integrations, and the AI pipelines—in just a few days entirely using **Vibe Coding**. Prompt-driven development allowed us to iterate at the speed of thought."

## 🏁 [2:30 - 3:00] The Closing
"GramAI isn't just a hackathon prototype. It's a scalable solution ready to deploy to Krishi Vigyan Kendras across the country. 

We are turning ideas into products, and bringing the AI revolution to the people who need it the most. 

Thank you. We are ready for your questions."
