# 🎤 HackIndia Showdown Pitch Script: Dial2AI
*Time limit: 3 Minutes. Speak with high energy and confidence. Emphasize the keywords in **bold**.*

---

## 🎬 [0:00 - 0:30] The Hook & The Problem
"Hello Judges, we are Team Git Push Pray. 

Right now, in 2026, the tech world is obsessed with building 5G web apps. But we are forgetting the **disconnected**. 

Over **350 Million people** in India still use basic feature phones. Nearly **50% of our rural population** lacks reliable internet. Because of this digital divide, they get scammed by middlemen, they don't know the real Mandi prices, and they miss out on critical government schemes.

We asked ourselves: How do we bring the power of Generative AI to someone who only has a **$10 Nokia phone?**

The answer is **Dial2AI**."

## 🚀 [0:30 - 1:15] The Solution & Live Demo
"Dial2AI is the world's first voice-native Generative AI platform over a **simple phone call**. No apps. No internet. No frustrating 'Press 1' IVR menus. 

*Let me show you live.* 
**(Action: Put your phone on speaker and dial the Exotel number. Show the phone to the camera).**

*(AI answers: "Namaste! Dial2AI mein aapka swagat hai...")*

**(You say):** *"Mera naam Ramesh hai. Aaj Nashik mein pyaz ka kya rate chal raha hai?"*

**(Action: Explain while the AI processes for 1-2 seconds and the hold music plays)**
"Right now, our backend is streaming my audio via WebSockets, transcribing my Hinglish in real-time, extracting my intent, and hitting the live Data.gov.in API to get the real price. Notice the hold music? That's our dynamic audio buffer ensuring there's zero dead air on the line."

*(AI answers with the live Nashik onion price).*

"This isn't a hallucination. That is **real-time live data** injected into the LLM context mid-conversation."

## 🧠 [1:15 - 2:00] Competitive Edge & Engineering
"Why are we better than what exists?
WhatsApp bots and apps like Pocket Pal AI require smartphones, internet, and digital literacy. Advanced tools like Google AI Edge Gallery require expensive hardware capable of running on-device AI. Traditional Kisan Call Centers have massive wait times. 

Dial2AI is **hardware agnostic, infinitely scalable, and requires zero app downloads**. 

To make this work seamlessly, we had to solve hard HCI problems:
1. **The Static Problem:** Telecom lines have terrible static. We wrote a custom amplitude-based noise gate to filter out Exotel's line static so the AI doesn't hallucinate background noise.
2. **Intent Routing:** We use Gemini 3.5 Flash to rapidly classify the caller's intent and dynamically route the API calls.
3. **Barge-in Detection:** If the caller interrupts the AI, it instantly stops speaking and listens, just like a real human."

## 📊 [2:00 - 2:30] The Platform & Speed
"But we didn't just build a bot. We built a **platform**. 

**(Action: Share screen showing the Next.js Dashboard)**
As you can see on our real-time Next.js dashboard, every single call is logged. Our AI automatically extracts the **Call Summary, Customer Sentiment, and Lead Information**. 

And look at this—**(Show your phone screen)**—as soon as the call ended, our system sent me an **SMS with a text summary** of my query. 

We built this entire full-stack platform in just a few days entirely using **Vibe Coding**. Prompt-driven development allowed us to iterate at the speed of thought."

## 🏁 [2:30 - 3:00] The Closing
"Dial2AI isn't just a hackathon prototype. It's a scalable solution ready to deploy across the country. 

We are turning ideas into products, and bringing the AI revolution to the people who need it the most. 

Thank you. We are ready for your questions."
