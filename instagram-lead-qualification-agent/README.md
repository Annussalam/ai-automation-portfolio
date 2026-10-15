
# AI Instagram Lead Qualification & Customer Engagement Agent

## 📌 Project Overview

An AI-powered Instagram customer engagement and lead qualification system built using **n8n, Google Gemini, Instagram API, Meta Webhooks, and Gmail**.

The workflow analyzes customer comments, identifies potential leads, generates personalized responses, and directs sensitive inquiries to human review.

- **Project Type:** AI Customer Engagement & Lead Qualification
- **Project Status:** Developed & Initially Tested

## 🎯 Business Problem

Businesses managing Instagram customer interactions often face challenges such as:

- High volumes of repetitive product and pricing inquiries.
- Difficulty identifying customers with genuine purchase intent.
- Delayed responses to customer questions.
- Manual monitoring of complaints and negative feedback.

## ⚡ Key Features

- **Automated Comment Replies:** Responds to eligible Instagram comments through API integration.
- **AI-Powered Analysis:** Identifies customer intent, sentiment, and inquiry category.
- **Lead Qualification:** Classifies leads as high, medium, low, or no purchase intent.
- **Priority-Based Routing:** Applies decision rules based on lead quality and customer sentiment.
- **Multilingual Communication:** Generates natural responses in English and Roman Urdu.
- **Complaint Management:** Creates Gmail drafts containing complaint details and suggested responses for human review.
- **Business Knowledge Integration:** Generates responses using predefined business information and communication rules.
- **Self-Comment Filtering:** Excludes comments from the connected business account.
- **Instagram DM Detection:** Captures incoming direct-message events and extracts message details.

## 🔄 How It Works

1. **Webhook Trigger:** Receives Instagram interactions through Meta Webhooks.
2. **Event Filtering:** Separates comment events from direct messages.
3. **Data Extraction:** Processes customer messages and relevant metadata.
4. **AI Classification:** Google Gemini analyzes intent, sentiment, lead quality, and priority.
5. **Response Generation:** Produces context-aware replies based on business guidelines.
6. **Conditional Routing:** Determines whether to reply automatically or require human intervention.
7. **Action Execution:** Publishes eligible comment replies or creates Gmail drafts for complaint review.

## 🧩 Workflow Architecture

**Instagram Webhook → Event Filtering → Data Processing → Gemini AI → Decision Logic**

**Comment Reply Path:**  
AI Decision → Instagram API → Public Comment Reply

**Complaint Review Path:**  
AI Decision → Gmail Draft → Human Review

**DM Processing Path:**  
Incoming DM → Message Detection → Data Extraction

## 🛠️ Technologies Used

- **n8n:** Workflow automation and orchestration
- **Google Gemini:** AI analysis and response generation
- **Instagram API:** Comment management and replies
- **Meta Webhooks:** Instagram event handling
- **Gmail:** Complaint draft creation
- **HTTP Requests:** API communication
- **JSON:** Structured AI outputs and data processing
- **Prompt Engineering:** Business-specific instructions and response rules

## 📈 Business Benefits

- Reduces repetitive customer support tasks.
- Helps identify and prioritize potential customers.
- Improves consistency in public customer interactions.
- Supports human oversight for complaints and sensitive issues.
- Provides a scalable foundation for Instagram customer engagement.

## 🔧 Planned Enhancement

**AI-Powered Instagram DM Auto-Replies**

Extend the existing DM detection workflow to automatically analyze incoming messages and deliver personalized responses through the Instagram Messaging API.

This functionality will be implemented and tested as part of the next workflow update.

## 📸 Workflow Screenshot

*Workflow screenshot will be added after importing the automation into n8n.*

## 🎥 Demo Video

*Demo video coming soon.*

## 🚀 Project Results

- Developed and initially tested an AI-powered Instagram engagement workflow.
- Implemented comment analysis, lead classification, and AI-generated responses.
- Integrated automated comment replies and complaint review routing.
- Established the initial workflow for processing Instagram direct messages.

---

**Developed by Annus Salam**
