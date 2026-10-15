
# Website Data Scraper & Vector Database Pipeline

## 📌 Project Overview

An automated e-commerce data extraction and vector database pipeline built using **n8n, JavaScript, OpenAI Embeddings, and Supabase**.

The workflow extracts product information from website sitemaps, processes unstructured web content, and prepares searchable product knowledge for AI-powered applications.

- **Project Type:** Web Data Extraction & AI Knowledge Base
-- **Project Status:** Developed & Tested

## 🎯 Business Problem

E-commerce businesses often face challenges such as:

- Product information scattered across multiple web pages.
- Time-consuming manual collection of product details.
- Difficulty preparing website content for AI-powered assistants.
- Maintaining structured and accessible product knowledge.

## ⚡ Key Features

- **Sitemap-Based Discovery:** Extracts product page URLs from an XML sitemap.
- **Automated Web Scraping:** Retrieves product information through HTTP requests.
- **Structured Data Extraction:** Extracts product names, prices, descriptions, ingredients, usage instructions, and image URLs.
- **JavaScript Processing:** Filters URLs, cleans extracted text, and formats product records.
- **Batch Processing:** Processes individual product pages using loop-based execution.
- **Text Chunking:** Splits product content into smaller segments.
- **OpenAI Embeddings:** Converts text into vector representations.
- **Supabase Vector Storage:** Inserts processed documents and metadata into a vector database.

## 🔄 How It Works

1. **Manual Trigger:** Starts the extraction workflow.
2. **Sitemap Retrieval:** Fetches an e-commerce product sitemap.
3. **URL Extraction:** Identifies and filters product page links.
4. **Page Processing:** Retrieves product pages individually.
5. **HTML Extraction:** Collects relevant product attributes.
6. **Data Cleaning:** Normalizes text and prepares product content.
7. **Document Processing:** Splits content and generates embeddings.
8. **Vector Storage:** Inserts product documents and metadata into Supabase.

## 🧩 Workflow Architecture

**Manual Trigger → Sitemap Request → URL Extraction → JavaScript Filtering → Product Page Scraping → Data Cleaning → Document Loader → Text Splitter & OpenAI Embeddings → Supabase Vector Store**

## 🛠️ Technologies Used

- **n8n:** Workflow orchestration and automation
- **HTTP Requests:** Sitemap and webpage retrieval
- **HTML Extraction:** Product data extraction using CSS selectors
- **JavaScript:** Data filtering and transformation
- **OpenAI Embeddings:** Vector representation of product content
- **Supabase:** Vector database storage
- **Text Splitter:** Document chunking
- **JSON:** Structured records and metadata

## 📈 Business Benefits

- Reduces manual product data collection.
- Organizes product knowledge for AI-powered applications.
- Supports semantic search and retrieval-based systems.
- Creates a reusable foundation for RAG-powered customer support and product assistants.

## 📸 Workflow Screenshot

*Workflow screenshot will be added here.*

## 🎥 Demo Video

*Demo video coming soon.*

## 🚀 Project Results

- Developed a sitemap-driven product extraction workflow.
- Configured structured product information processing and text cleaning.
- Integrated OpenAI embeddings with Supabase Vector Store.
- Prepared a reusable data ingestion pipeline for AI knowledge retrieval applications.

---

**Developed by Annus Salam**
