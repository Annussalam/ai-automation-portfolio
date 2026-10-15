
# AI Voice Calling Agent | Customer Support Automation

## 📌 Project Overview

An AI-powered Voice Calling Agent developed using **Vapi, n8n, MCP, and Supabase** for a skincare e-commerce business scenario.

The system is designed to handle customer conversations, retrieve business information, manage customer records, and automate order-related tasks through connected workflows.

- **Project Type:** AI Voice Agent & Business Automation
- **Project Status:** Developed & Initially Tested

## 🎯 Business Problem

- Repetitive customer calls require manual attention.
- Customers need quick access to product information.
- Manual order entry and customer data management are time-consuming.
- Disconnected business systems create operational inefficiencies.

## ⚡ Key Features

- **AI Voice Conversations:** Handles customer interactions through Vapi.
- **MCP Tool Integration:** Connects the voice agent to multiple business automation workflows.
- **Supabase Data Retrieval:** Retrieves relevant product and customer information.
- **Order Automation:** Supports creating order records in Google Sheets.
- **Customer Data Management:** Supports customer information updates.
- **Modular Workflows:** Separates business operations into reusable automation tools.

## 🔄 Core Workflow Steps

1. **Customer Interaction:** A customer initiates a conversation with the AI voice agent.
2. **Voice AI Processing:** Vapi processes the conversation and identifies customer requirements.
3. **MCP Tool Execution:** The agent requests an appropriate business operation through the MCP Server.
4. **Information Retrieval:** Connected n8n workflows retrieve relevant information from Supabase.
5. **Order Processing:** The order creation workflow records order details in Google Sheets when required.
6. **Customer Data Update:** A separate workflow handles customer information updates.
7. **AI Response:** The voice agent uses the available information to continue the customer conversation.

## 🧩 Workflow Architecture

**Customer → Vapi Voice Agent → n8n MCP Server → Business Tools → AI Response**

### Connected Workflows

- **MCP Server:** Exposes business operations as callable tools.
- **Supabase Data Fetching:** Retrieves business and product information.
- **Google Sheets Order Creation:** Handles order record creation.
- **Customer Data Update:** Manages customer information updates.

## 🛠️ Technologies Used

- **Vapi:** AI Voice Calling Platform
- **n8n:** Workflow Automation & Orchestration
- **MCP:** Model Context Protocol for tool integration
- **Supabase:** Database and Business Information Retrieval
- **Google Sheets:** Order Management Records
- **REST APIs & Webhooks:** Communication between integrated systems

## 📈 Business Benefits

- Reduces repetitive customer service tasks.
- Supports faster customer inquiry handling.
- Connects customer conversations with business data.
- Streamlines order entry and customer record updates.
- Supports automation across multiple business applications.
- Can be adapted to e-commerce and service-based businesses.

## 📸 Workflow Screenshots

### Main AI Voice Calling Agent
*Screenshot will be added.*

### MCP Server
*Screenshot will be added.*

### Connected Business Workflows
- Supabase Data Fetching
- Google Sheets Order Creation
- Customer Data Update

*Workflow screenshots will be added.*

## 🎥 Demo Video

A demonstration video will be added after deployment and integration testing.

## 🚀 Deployment Status

**Developed & Initially Tested**

- Initial voice agent testing completed.
- MCP Server and connected automation workflows configured.
- Reconnection and end-to-end verification planned after self-hosted deployment.

---

**Developed by Annus Salam**
