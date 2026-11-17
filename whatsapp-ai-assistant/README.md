# WhatsApp AI Assistant (Google Docs Knowledge Base)

**Problem:** Customers send the same questions on WhatsApp all day, and updating a chatbot usually needs a developer.

**What it does:**
- Replies to WhatsApp messages using a live Google Doc. Update the document and the assistant uses the new information, with no coding.
- Checks WhatsApp's 24-hour reply window and sends an approved template message when the window has closed.
- Logs conversations to Google Sheets.

**Status:** Working prototype. Appointment booking is the next feature.

**Tools:** n8n, WhatsApp Cloud API, Google Docs, Google Sheets, Gemini

## Workflow Screenshot

![WhatsApp workflow](whatsapp-workflow.png)

## Demo Video

Demo video coming soon. Message me for a live demo.

## How It Works

1. A customer sends a WhatsApp message.
2. n8n receives it and reads the business information from a Google Doc.
3. The AI agent writes an answer using that information.
4. The conversation is saved to Google Sheets.
5. If the 24-hour window is open, the answer is sent. If not, an approved template message is sent.

---

**Developed by Annus Salam**

Want a version for your business? Email me: [your email]
