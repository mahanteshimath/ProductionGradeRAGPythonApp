# Production-Grade RAG Python Application

A production-ready Retrieval-Augmented Generation (RAG) system that allows users to upload PDFs, ask questions, and get AI-powered answers based on the document content. Built with FastAPI, Streamlit, OpenAI, and Qdrant vector database.

## 🌟 Features

- 📄 PDF document ingestion and processing
- 🔍 Semantic search using vector embeddings
- 🤖 AI-powered question answering using OpenAI GPT
- 🎯 Production-ready architecture with event-driven design
- 📊 User-friendly Streamlit interface
- 🔄 Asynchronous processing using Inngest
- 📦 Vector storage with Qdrant

## 🏗️ Architecture

The application follows a modern, event-driven architecture:

1. **Frontend (Streamlit)**
   - Handles PDF uploads
   - Provides question-answering interface
   - Displays results with source citations

2. **Backend (FastAPI + Inngest)**
   - Processes PDF ingestion events
   - Manages question-answering workflow
   - Coordinates with vector database

3. **Vector Database (Qdrant)**
   - Stores document embeddings
   - Enables semantic search
   - Manages document chunks

## 🚀 Getting Started

### Prerequisites

- Python 3.13 or higher
- OpenAI API key
- Inngest account
- Qdrant instance (local or cloud)

### Environment Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/mahanteshimath/ProductionGradeRAGPythonApp.git
   cd ProductionGradeRAGPythonApp
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a .env file with your configuration:
   ```
   OPENAI_API_KEY=your_openai_api_key
   INNGEST_EVENT_KEY=your_inngest_key
   QDRANT_URL=your_qdrant_url  # Default: http://localhost:6333
   ```

### Running the Application

1. Start the FastAPI backend:
   ```bash
   uvicorn main:app --reload
   ```

2. In a new terminal, start the Streamlit frontend:
   ```bash
   streamlit run streamlit_app.py
   ```

3. Access the application:
   - Frontend UI: http://localhost:8501
   - API Documentation: http://localhost:8000/docs

## 🛠️ Tech Stack

- **FastAPI**: Backend API framework
- **Streamlit**: User interface
- **OpenAI**: Embeddings and LLM
- **Qdrant**: Vector database
- **Inngest**: Event processing
- **LlamaIndex**: Document processing
- **Python-dotenv**: Environment management
- **Uvicorn**: ASGI server

## 📋 Usage

1. **Upload a PDF**
   - Click the "Upload PDF" button in the Streamlit interface
   - Wait for the ingestion confirmation

2. **Ask Questions**
   - Type your question in the input field
   - Click "Ask" or press Enter
   - View the AI-generated answer and source citations

## 🔧 Advanced Configuration

- Adjust chunk size and overlap in `data_loader.py`
- Modify vector search parameters in `vector_db.py`
- Configure Inngest event settings in `main.py`
- Customize UI components in `streamlit_app.py`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.
