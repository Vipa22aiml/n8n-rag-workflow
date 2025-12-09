# 🤖 n8n RAG Workflow - Intelligent Document Processing & Chat

<div align="center">
  <img src="./assets/workflow-screenshot.png" alt="n8n RAG Workflow" width="100%" />
</div>

## 🌟 Overview

This is a **Zero-Code RAG (Retrieval-Augmented Generation) Pipeline** built entirely in n8n that transforms static files into an intelligent, queryable knowledge base. Upload documents to Google Drive, and instantly chat with an AI that understands your content!

### ✨ What Makes This Special?

- **🔄 Automatic Processing**: Watches Google Drive for new files and processes them automatically
- **📊 Multi-Format Support**: Handles PDFs, Excel files, CSVs, and text documents
- **🧠 Vector Intelligence**: Uses Google Gemini embeddings for semantic search
- **💬 Chat Interface**: Built-in chat UI for natural conversation with your documents
- **🔍 Smart Memory**: Remembers conversation context for follow-up questions
- **⚡ Real-time Updates**: Files are processed and available for queries immediately

## 🏗️ Architecture Breakdown

The workflow is organized into four distinct sections:

### 1. 🔴 **Setup Phase** (Red Box)
**Purpose**: One-time database initialization
- Creates necessary tables in Supabase/PostgreSQL:
  - `documents`: Stores raw text content
  - `metadata`: Stores file information (name, author, date)
  - `rows`: Stores vector embeddings

### 2. 🔵 **Ingestion Pipeline** (Blue Box)
**Purpose**: Automated file processing and storage
- **Triggers**: Monitors Google Drive folder for new/updated files
- **Smart Processing**: Detects file type and applies appropriate extraction:
  - 📄 PDF → Extract PDF Text
  - 📊 Excel → Extract from Excel
  - 📈 CSV → Extract from CSV
  - 📝 Text → Extract Document Text
- **Vectorization**: Converts text to embeddings using Google Gemini
- **Storage**: Saves vectors to Supabase for lightning-fast retrieval

### 3. 🟡 **RAG AI Agent** (Yellow Box)
**Purpose**: Intelligent chat interface with document awareness
- **Chat Interface**: Clean, user-friendly messaging system
- **Memory**: Maintains conversation history via Postgres Chat Memory
- **Smart Retrieval**: Searches relevant documents before generating responses
- **AI Integration**: Powered by Google Gemini for natural, accurate responses

### 4. 🟢 **Agent Toolkit** (Green Box)
**Purpose**: Connects AI to vector database
- Creates searchable tools for the AI agent
- Enables semantic search across your document collection
- Provides context-aware responses based on your specific content

## 🚀 Quick Start Guide

### Prerequisites

- **n8n Account**: [Sign up here](https://n8n.io)
- **Google Cloud Account**: For Drive API and Gemini AI
- **Supabase Account**: For vector database storage

### Step 1: Configure Credentials

#### Google Cloud Setup
1. Enable **Google Drive API** and **Vertex AI API**
2. Create OAuth2 credentials
3. Add credentials to n8n:
   - `Google Drive` credential
   - `Google Gemini` credential

#### Supabase Setup
1. Create new Supabase project
2. Get your connection string and API key
3. Add to n8n:
   - `Supabase` credential
   - `Postgres` credential

### Step 2: Initialize Database

1. Import the workflow into your n8n instance
2. Navigate to the **Red Box** (Setup Phase)
3. Manually execute these nodes one by one:
   - Create Documents Table
   - Create Metadata Table
   - Create Document Rows

✅ **Success Check**: Visit your Supabase dashboard - you should see the new tables!

### Step 3: Set Up Document Processing

1. Open the **File Created** node in the Blue Box
2. Select your target Google Drive folder
3. **Activate the workflow** (toggle "Active" in top-right)
4. Upload a test file (PDF, CSV, or TXT) to your monitored folder
5. Check the "Executions" tab - you should see successful processing!

### Step 4: Start Chatting! 💬

1. Click **"Open chat"** button at the bottom of n8n
2. Ask questions about your uploaded documents
3. Example: *"What is the main topic discussed in the document I just uploaded?"*

## 🎯 Powerful Use Cases

### 1. 🛠️ **Automated Customer Support**
- **Scenario**: Product manuals and policy documents
- **Implementation**: Upload all manuals → Connect webhook to website chat
- **Result**: Customers get instant, accurate answers from your documentation

### 2. 📈 **Financial Data Analysis**
- **Scenario**: Hundreds of Excel/CSV files with sales data
- **Implementation**: Bulk upload financial files
- **Result**: Ask "Summarize Q3 sales trends" or "Find invoice for Client X"

### 3. 👥 **HR Onboarding Assistant**
- **Scenario**: Employee handbooks and policy documents
- **Implementation**: Upload HR materials
- **Result**: New hires ask "How many vacation days do I get?" and get instant answers

### 4. ⚖️ **Legal Document Review**
- **Scenario**: Contract analysis and review
- **Implementation**: Upload contracts and legal documents
- **Result**: "Does this contract contain a non-compete clause?"

### 5. 🧠 **Personal Knowledge Management**
- **Scenario**: Research articles, notes, receipts
- **Implementation**: Save everything to monitored Drive folder
- **Result**: "Where did I save the laptop receipt?" or "What did that AI trends article say?"

## 🔧 Technical Features

- **🔄 Real-time Processing**: Files are processed immediately upon upload
- **🧠 Semantic Search**: Uses vector embeddings for meaning-based retrieval
- **📚 Context Awareness**: Maintains conversation history
- **🔗 Multi-format Support**: PDFs, Excel, CSV, and text files
- **⚡ Fast Retrieval**: Vector database ensures lightning-fast searches
- **🛡️ Secure**: Your data stays in your Google Drive and Supabase

## 🛠️ Customization Options

### Adding New File Types
1. Add new case to the **Switch** node
2. Create appropriate extraction node
3. Connect to the embedding pipeline

### Custom Chat Interface
1. Replace the webhook with your custom endpoint
2. Style the chat interface to match your brand
3. Add authentication if needed

### Advanced Filtering
1. Add metadata filtering in the query tool
2. Implement document tagging system
3. Create specialized search functions

## 📊 Monitoring & Troubleshooting

### Health Checks
- Monitor the "Executions" tab for processing errors
- Check Supabase logs for database issues
- Verify Google Drive permissions for file access

### Common Issues
- **Files not processing**: Check Google Drive permissions
- **Empty responses**: Verify embeddings are being created
- **Memory issues**: Check Postgres connection for chat history

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. 🐛 **Report Bugs**: Open an issue with detailed description
2. 💡 **Suggest Features**: Share your ideas for improvements
3. 📖 **Improve Documentation**: Help make the setup clearer
4. 🔧 **Share Customizations**: Show us your workflow variations

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **n8n Team**: For building an amazing no-code platform
- **Google**: For providing powerful AI APIs
- **Supabase**: For the excellent vector database solution
- **Community**: For inspiration and feedback

---

<div align="center">
  <strong>⭐ If this workflow helped you, please give it a star! ⭐</strong>
</div>

<div align="center">
  <a href="https://github.com/Vipa22aiml/n8n-rag-workflow/issues">Report Bug</a> •
  <a href="https://github.com/Vipa22aiml/n8n-rag-workflow/issues">Request Feature</a> •
  <a href="#">Documentation</a>
</div>