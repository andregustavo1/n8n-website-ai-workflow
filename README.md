# WhatsApp to Website Automation

This repository contains a **complex n8n automation workflow** that integrates WhatsApp messages with AI agents to generate professional websites automatically based on user prompts.

## 🧠 Problem Solved

Traditionally, creating websites from scratch or even via no-code tools requires manual input, time, and guidance. This automation allows users to initiate website creation just by sending a message via WhatsApp — eliminating manual back-and-forth and significantly speeding up the process.

## 💡 Workflow Summary

- **Trigger**: A message is received via WhatsApp (Evolution API) using a webhook.
- **Message Bounce Controller**: Holds message flow to ensure sequential processing (waits for message to be fully received before passing it on).
- **AI Agent 1 (Intent Detector)**: Analyzes the message:
  - If it's a **regular conversation**, it replies like a chatbot.
  - If it's a **website request**, it proceeds to the next step.

### If it's a website request:

1. **AI Agent 2 (Site Creator Assistant)**:  
   Sends a personalized message telling the user that their website is being built.

2. **Prompt Builder**:  
   Uses the original user message to generate a **detailed prompt** for a professional website.

3. **Python API Automation**:  
   Sends the generated prompt to a backend API, which communicates with a third-party platform ([Lovable](https://www.lovable.so)) to build the website.

4. **Website Delivery**:  
   Receives a final URL from the API and sends the link back to the user via WhatsApp.

## ⏱️ Time to Build

On average, the website creation process takes **6 to 10 minutes** from message to delivery.

## 📸 Workflow Preview


