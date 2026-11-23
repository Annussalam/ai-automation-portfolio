# WhatsApp AI Assistant with Website Knowledge Base (RAG)

**Problem:** Customers send the same questions on WhatsApp all day, and business information is spread across websites and documents that a chatbot can't search.

**What it does:** two connected n8n workflows.
1. **Knowledge base builder:** collects information from a business website and stores it in a searchable database.
2. **WhatsApp assistant:** answers customer messages using that stored information.

**Status:** Both workflows built and tested. The knowledge base builder collects website content into Supabase, and the WhatsApp assistant, tested with Meta's WhatsApp test number, replies using that stored information. Appointment booking is the next feature.

**Tools:** n8n, WhatsApp Cloud API, Groq (LLM), OpenAI Embeddings, Supabase Vector Store, Redis, Google Sheets, JavaScript

## Workflow 1: WhatsApp Assistant

![WhatsApp assistant workflow](whatsapp-workflow.png)

- Receives WhatsApp messages and answers them with an AI agent.
- Searches the Supabase vector store, so answers come from the business's own information (RAG).
- Remembers earlier messages in the conversation using chat memory.
- Checks WhatsApp's 24-hour reply window. If it is open, the AI answer is sent. If it has closed, an approved template message is sent instead.
- Logs every conversation to Google Sheets.

## Workflow 2: Knowledge Base Builder

![Knowledge base builder workflow](knowledge-base-workflow.png)

1. Starts from a website address.
2. Downloads the page and extracts the links and content.
3. Visits the linked pages and extracts their details.
4. Cleans and organizes the text with JavaScript.
5. Splits the text into small pieces and creates embeddings.
6. Saves them in the Supabase vector store.
7. Waits between items so the process stays within limits.

This turns a business website into a knowledge base the assistant can search. Updating the assistant means running this workflow again.

## How It Works Together

1. The knowledge base builder collects and stores the business information.
2. A customer sends a WhatsApp message.
3. The AI agent searches the stored information and writes an answer, using chat memory to keep context.
4. The conversation is saved to Google Sheets.
5. The 24-hour window check decides whether to send the answer or a template message.

The knowledge base holds what the business offers. Chat memory only keeps track of the current conversation.

## Testing

- Ran the knowledge base builder and confirmed the website content was saved in Supabase.
- Sent test messages from Meta's WhatsApp test number and checked that replies used the stored information.
- Tested [number] sample questions: [number] answered correctly from the knowledge base, [number] needed improvement.

## Appointment Booking (next feature)

When a customer asks to book, the workflow will collect their name, service and preferred time, check availability in Google Calendar, create the appointment and send a confirmation.

## Works With My Voice Agent

This assistant can be paired with my [AI Voice Receptionist](../ai-voice-calling-agent/README.md), so a business can handle both WhatsApp messages and phone calls using shared business information.

## Customization

Built in n8n, so it can be adapted to a specific business: a different website or documents as the source, tone and language, booking rules, handoff to a person, and integrations with a CRM or other tools.

## Demo Video

Demo video coming soon. Message me for a live demo.

---

**Developed by Annus Salam**

Want a version for your business? Email me: annus.automates@gmail.com
