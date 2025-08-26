# 🧠 Wizora-AI – Web QA Backend + Chrome Extension

## 📌 Project Overview
**Wizora-AI** is an AI-powered project consisting of:  
1. A **FastAPI backend service** that takes a webpage URL and a user question, extracts the page content, and generates an answer using a pre-trained transformer model (`google/flan-t5-base`).  
2. A **Chrome Extension frontend** built with React + Tailwind + Vite, providing a simple interface to interact with the backend features.

---

## ✨ Features
- 🌐 **Webpage QA** → Ask questions about any webpage content.  
- 📄 **Document Chat** (via extension) → Interact with uploaded documents.  
- 📊 **Data Analysis** → Upload CSV/Excel and receive AI-generated insights.  
- 🤖 **AI Chatbot** → General chatbot responses.  
- 🎨 **Image Generator** → Create AI-generated images from text prompts.  

---

## 🛠️ Tech Stack
- **Backend:**  Python, FastAPI, Hugging Face Transformers, Readability-LXML  
- **Model:** FLAN-T5 (google/flan-t5-base)  
- **Frontend (Extension):** React (Vite), TailwindCSS, Chrome Extension APIs  
- **Other:** Python, Node.js, Postman (testing)  

---

## 📂 Project Structure
Backend/
│── README.md # Documentation
│── requirements.txt # Python dependencies
│── main.py / app/ # FastAPI backend
│
│── Wizora-AI-main/
│ └── AI extension/AI extension/
│ ├── index.html
│ ├── package.json
│ ├── tailwind.config.js
│ ├── vite.config.js
│ └── dist/ # Build output for Chrome Extension

yaml
Copy
Edit

---

## ⚙️ Setup & Installation

### 🔹 Backend
1. Clone or unzip the repo.  
2. Create virtual environment & install dependencies:
```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
Run the server:

bash
Copy
Edit
uvicorn main:app --reload
Test API with Postman:
POST http://127.0.0.1:8000/ask
JSON Body:

json
Copy
Edit
{
  "url": "https://www.geeksforgeeks.org/fastapi/",
  "question": "What is FastAPI?"
}
```
## Chrome Extension
Navigate to extension folder:
```
bash
Copy
Edit
cd Wizora-AI-main/"AI extension"/"AI extension"
Install dependencies:

bash
Copy
Edit
npm install
Build extension:

bash
Copy
Edit
npm run build
```
Load in Chrome:

Go to chrome://extensions/

Enable Developer Mode

Click Load unpacked → Select dist/ folder

📑 API Endpoints
POST /ask → Ask a question about a webpage

🧪 Example Request
json
Copy
Edit
{
  "url": "https://fastapi.tiangolo.com/",
  "question": "What are the key features of FastAPI?"
}

📈 Notes:
```
Uses readability-lxml to clean webpage content before processing.

Transformer model can be swapped (flan-t5-base, flan-t5-large, etc.).
```
