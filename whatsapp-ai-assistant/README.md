# WhatsApp AI Assistant for Dental Clinics

**Problem:** Dental clinics get the same WhatsApp questions all day: prices, timings, cleaning and whitening, location. Messages sent after hours often wait until the next morning, and a patient may book somewhere else in the meantime.

**What it does:** two connected n8n workflows.
1. **Knowledge base builder:** collects the clinic's information from its website and stores it in a searchable database.
2. **WhatsApp assistant:** answers patient messages using that stored information.

**Status:** Both workflows built and tested. The knowledge base builder collects website content into Supabase, and the WhatsApp assistant, tested with Meta's WhatsApp test number, replies using that stored information. Appointment booking is the next feature.

**Tools:** n8n, WhatsApp Cloud API, Groq (LLM), OpenAI Embeddings, Supabase Vector Store, Redis, Google Sheets, JavaScript

## System Overview

![Full system workflow](knowledge-base-workflow.png)

## What patients can ask

- Services and treatments (for example cleaning and whitening)
- Prices and packages
- Clinic timings and location
- General questions about visits and what to expect

The assistant answers only from the clinic's own information. It is not designed to give medical advice or diagnose problems, and for anything unclear it should point the patient to the clinic team.

## Workflow 1: WhatsApp Assistant

![WhatsApp assistant workflow](dental%20ai%20recipcionist.png)

- Receives WhatsApp messages and answers them with an AI agent.
- Searches the Supabase vector store, so answers come from the clinic's own information (RAG).
- Remembers earlier messages in the conversation using chat memory.
- Checks WhatsApp's 24-hour reply window. If it is open, the AI answer is sent. If it has closed, an approved template message is sent instead.
- Logs every conversation to Google Sheets, so the clinic can review what patients asked.

## Workflow 2: Knowledge Base Builder

1. Starts from the clinic's website address.
2. Downloads the page and extracts the links and content.
3. Visits the linked pages and extracts their details.
4. Cleans and organizes the text with JavaScript.
5. Splits the text into small pieces and creates embeddings.
6. Saves them in the Supabase vector store.
7. Waits between items so the process stays within limits.

When the clinic changes its prices or timings, running this workflow again updates the assistant.

## How It Works Together

1. The knowledge base builder collects and stores the clinic's information.
2. A patient sends a WhatsApp message.
3. The AI agent searches the stored information and writes an answer, using chat memory to keep context.
4. The conversation is saved to Google Sheets.
5. The 24-hour window check decides whether to send the answer or a template message.

The knowledge base holds what the clinic offers. Chat memory only keeps track of the current conversation.

## Testing

- Ran the knowledge base builder and confirmed the website content was saved in Supabase.
- Sent test messages from Meta's WhatsApp test number and checked that replies used the stored information.

## Works for Other Businesses

This assistant was built for a dental clinic, but the same system works for any business that answers repeated customer questions on WhatsApp. Only the knowledge base changes. For example:
- Other clinics (skin, aesthetic, general practice)
- Restaurants and cafés (menu, timings, reservations)
- Salons and spas
- Real estate agencies
- Gyms, education consultants and service businesses

## Appointment Booking (next feature)

When a patient asks to book, the workflow will collect their name, treatment and preferred time, check availability in Google Calendar, create the appointment and send a confirmation.

## Works With My Voice Agent

This assistant can be paired with my [AI Voice Receptionist](../ai-voice-calling-agent/README.md), so a business can handle both WhatsApp messages and phone calls using shared business information.

## Customization

Built in n8n, so it can be adapted to a specific business: its own website or documents as the source, tone and language, booking rules, handoff to a person, and integrations with a CRM or other tools.

## Demo Video

Demo video coming soon. Message me for a live demo.

---

**Developed by Annus Salam**

Want a version for your business? Email me: annus.automates@gmail.com
