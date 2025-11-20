# 🛠️ Website RAG Chatbot (n8n Workflow)

A fully automated **Retrieval-Augmented Generation (RAG)** chatbot built using **n8n**, designed for a plumbing company’s website. It answers customer questions instantly using company-specific PDF documents, stored as embeddings in Supabase. The chatbot is connected to the website through a simple footer script and triggers via the Webchat Trigger node in n8n.

This project can be easily customized for **any business or industry** by updating the document source and vector database.

---

## 🚀 Features

### ✅ RAG-Based Answering  
Uses Gemini Embeddings + Supabase Vector Store for accurate, context-rich responses.

### ✅ Fully Automated n8n Workflow  
Includes:
- Webchat Trigger Node  
- Google Drive Node  
- Data Loader Node  
- Gemini Embeddings Node  
- Supabase Vector Store Node  
- AI Agent Node  
- PostgreSQL Memory Node  

### ✅ Website Integration  
Add a single JavaScript snippet in your website’s footer to activate the chatbot.

### ✅ Customizable  
Replace the PDF file or database to adapt the chatbot to any field such as construction, education, real estate, repair services, etc.

---

## 🧩 Architecture Overview

```
User Question → Website Chat Widget  
       ↓  
Webchat Trigger Node (n8n)  
       ↓  
Google Drive Node → Download Company PDF  
       ↓  
Data Loader Node → Convert PDF to text chunks  
       ↓  
Gemini Embeddings Node → Create vector embeddings  
       ↓  
Supabase Vector Store → Store + Retrieve vectors  
       ↓  
AI Agent Node → Generate response using RAG  
       ↓  
PostgreSQL Memory Node → Store conversation context  
       ↓  
Chatbot Response Sent Back to Website  
```

---

## 🗂️ Requirements

- n8n hosted on cloud/VPS/local instance  
- Supabase project (for vector store)  
- Google Drive access (for document storage)  
- Gemini API key  
- PostgreSQL (conversation memory)  
- Website where the chatbot script will be added  

---

## ⚙️ Installation & Setup

### **1. Clone or Download This Repository**
```bash
git clone https://github.com/yourusername/website-rag-chatbot.git
```

### **2. Configure Supabase**
- Create a table for vector embeddings  
- Enable pgvector extension  
- Insert API keys in n8n credentials  

### **3. Prepare Your Knowledge Base**
Upload your PDF file to Google Drive.

### **4. Import n8n Workflow**
- Go to n8n → Workflows  
- Click **Import from File**  
- Upload the provided `.json` workflow  

### **5. Add Chatbot Script to Website**
Paste the following code in your site’s footer:

```html
<script src="YOUR_CHAT_WIDGET_SCRIPT_URL"></script>
```

### **6. Test the Chatbot**
Open your website → Type a question → n8n workflow triggers automatically.

---

## 🔧 Customization

To customize for any business:

1. Replace the PDF in Google Drive  
2. Regenerate embeddings using Gemini  
3. Update Supabase vector database  
4. Modify system prompts in AI Agent Node  
5. Change the chat widget’s branding  

---

## 📄 License
This project is open-source and can be modified freely. License details can be added here if applicable.

---



