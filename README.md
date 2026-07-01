# 📧 AI Cold Email Generator using Llama 3.1, LangChain & ChromaDB

An AI-powered Cold Email Generator that automatically extracts job details from a company's career page and generates personalized business outreach emails using **Llama 3.1**, **LangChain**, and **ChromaDB**.

The application scrapes a job posting, identifies the required skills and experience using an LLM, retrieves the most relevant portfolio projects through semantic search, and generates a professional cold email tailored to the job requirements.

---

## 🚀 Features

- 🌐 Extract job descriptions directly from a career page URL
- 🤖 AI-powered job information extraction using Llama 3.1
- 🧠 Prompt engineering with LangChain
- 📄 Structured JSON extraction from unstructured webpages
- 🔍 Semantic portfolio retrieval using ChromaDB
- ✉️ Personalized cold email generation
- 💻 Simple and interactive Streamlit interface

---

## 🏗️ Project Architecture

```text
                User
                  │
                  ▼
        Streamlit Web Interface
                  │
                  ▼
         Enter Job Posting URL
                  │
                  ▼
      LangChain WebBaseLoader
                  │
                  ▼
      Scrape Job Description
                  │
                  ▼
          Text Preprocessing
             (Regex Cleaning)
                  │
                  ▼
        Llama 3.1 (Groq API)
          Job Information
            Extraction
                  │
                  ▼
     Role • Skills • Experience
                  │
                  ▼
      ChromaDB Vector Search
                  │
                  ▼
     Relevant Portfolio Links
                  │
                  ▼
        Llama 3.1 (Groq API)
        Cold Email Generation
                  │
                  ▼
         Generated Cold Email
```

---

## 📂 Project Structure

```
.
├── app/
│   ├── main.py
│   ├── chains.py
│   ├── portfolio.py
│   ├── utils.py
│   └── resource/
│       └── my_portfolio.csv
│
├── vectorstore/
├── requirements.txt
├── runtime.txt
├── .env
└── README.md
```

---

## ⚙️ Tech Stack

### AI & LLM

- Llama 3.1 70B
- Groq API
- LangChain

### Vector Database

- ChromaDB

### Backend

- Python 3.11

### Frontend

- Streamlit

### Data Processing

- Pandas
- Regex

### Environment Management

- python-dotenv

---

## 🛠️ Installation

### Clone Repository

```bash
git clone https://github.com/<your-username>/<repository-name>.git
cd <repository-name>
```

---

### Create Virtual Environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Configure Environment Variables

Create a `.env` file in the project root.

```env
GROQ_API_KEY=your_groq_api_key
```

Get your API key from:

https://console.groq.com/keys

---

## ▶️ Run the Application

```bash
streamlit run app/main.py
```

The application will start at:

```
http://localhost:8501
```

---

## 💡 How It Works

### Step 1

Enter a job posting URL.

Example:

```
https://jobs.nike.com/job/R-33460
```

---

### Step 2

The application scrapes the webpage using LangChain's `WebBaseLoader`.

---

### Step 3

The webpage text is cleaned using regular expressions to remove:

- HTML tags
- URLs
- Special characters
- Extra whitespace

---

### Step 4

The cleaned content is sent to **Llama 3.1** which extracts:

- Job Role
- Experience
- Required Skills
- Job Description

The output is converted into structured JSON.

---

### Step 5

The extracted skills are searched against a ChromaDB vector database containing portfolio projects.

The most relevant portfolio links are retrieved using semantic similarity search.

---

### Step 6

The retrieved portfolio links are provided as additional context to the LLM.

The model generates a personalized cold email highlighting relevant experience.

---

## 📊 Example Workflow

```
Career Page URL
        │
        ▼
Website Scraping
        │
        ▼
Text Cleaning
        │
        ▼
LLM Job Extraction
        │
        ▼
Skill Extraction
        │
        ▼
Vector Search
        │
        ▼
Relevant Portfolio Links
        │
        ▼
LLM Email Generation
```

---

## 📁 Portfolio Dataset

Portfolio information is stored in:

```
app/resource/my_portfolio.csv
```

Each entry contains:

- Technology Stack
- Portfolio Link

Example:

| Tech Stack | Portfolio |
|------------|-----------|
| Python, Django | GitHub Link |
| Java, Spring Boot | GitHub Link |
| React, Node.js | GitHub Link |

---

## 🧠 AI Concepts Used

- Large Language Models (LLMs)
- Prompt Engineering
- Semantic Search
- Vector Databases
- Retrieval-Augmented Generation (RAG) Concepts
- Structured Output Parsing

---

## 📦 Dependencies

- LangChain
- LangChain Community
- LangChain Groq
- ChromaDB
- Streamlit
- Pandas
- python-dotenv
- Selenium
- Unstructured

---

## 🚀 Future Improvements

- Support PDF and DOCX job descriptions
- Support multiple LLM providers (OpenAI, Gemini, Claude)
- Better HTML parsing using BeautifulSoup
- Configurable prompt templates
- Improved portfolio ranking with reranking models
- Docker support
- Cloud deployment
- User authentication
- Email export functionality

---

## 👨‍💻 Author

**Sonu Yaduvanshi**

B.Tech Information Technology

AI | Machine Learning | Backend Development

GitHub: https://github.com/<your-github>

LinkedIn: https://linkedin.com/in/<your-linkedin>

---

## 📄 License

This project is intended for educational and portfolio purposes.
