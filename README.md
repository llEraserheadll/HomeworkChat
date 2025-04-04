# 📄 Homework Chat: Your AI-Powered Assignment Assistant

Chat with your PDFs like they're your professor!  
This project uses **RAG (Retrieval-Augmented Generation)** to help answer questions directly from your uploaded documents – perfect for assignments, study material, or reports.

---

## 🚀 Tech Stack

<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" />
  <img src="https://img.shields.io/badge/LangChain-000000?style=for-the-badge&logo=langchain&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/FAISS-009688?style=for-the-badge" />
</p>

---

## 💡 Features

- 🧠 Ask questions based on content from one or more PDF files
- 🔎 Uses **RAG** to search your documents before answering
- 🗂️ Upload multiple PDFs and combine them into a searchable knowledge base
- 🤖 Conversational memory for a natural chat experience
- 🎨 Custom chatbot-style UI with avatars and styles

---

## 🧠 What Is RAG?

**Retrieval-Augmented Generation (RAG)** is an AI technique where:

1. Your documents are split into chunks.
2. These chunks are stored in a **vector database** using embeddings (like OpenAI or HuggingFace).
3. When you ask a question, the most relevant chunks are retrieved and passed into a language model to give a precise, contextual answer.

This means the chatbot doesn't "hallucinate" — it sticks to your data!

---

## 📦 Project Structure

```bash
homework-chat/
├── app.py               # Main Streamlit app
├── htmlTemplates.py     # Custom chat UI templates
├── requirements.txt     # Python dependencies
└── README.md            # You're here!
```

---

## 🛠️ How to Run the Project

1. **Clone the repository**
```bash
git clone https://github.com/your-username/homework-chat.git
cd homework-chat
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Add your OpenAI key**

Create a `.env` file in the root directory and add:

```bash
OPENAI_API_KEY=your_openai_api_key
```

4. **Run the Streamlit app**
```bash
streamlit run app.py
```

5. **Upload your PDFs and start chatting!**

---

## 🧰 Under the Hood: How It Works

| Step | Module | Description |
|------|--------|-------------|
| 📥 Extract | `get_pdf_text()` | Reads text from uploaded PDFs using PyPDF2 |
| ✂️ Split | `get_text_chunks()` | Splits the text into manageable chunks |
| 🧬 Embed | `get_vectorstore()` | Converts chunks into vector embeddings using OpenAI |
| 🧠 Memory + Retrieval | `get_conversation_chain()` | Sets up the RAG logic and chat memory |
| 💬 UI | `htmlTemplates.py` + Streamlit | Renders messages and avatars for user/bot interaction |

---

## 🚧 Future Improvements

- Add support for other document types (Word, TXT)
- Add HuggingFace embedding support toggle
- Save/load past chat sessions
- Dockerize the app for easy deployment

---

## ❤️ Credits

Made with 💻 + 📚 to make studying less stressful.
