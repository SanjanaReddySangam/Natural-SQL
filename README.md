# 🧠 Natural SQL — Convert Natural Language to SQL Queries

Natural SQL is a modern Streamlit-based web application that lets you write SQL queries using plain English. Powered by **Google’s Gemini API**, this app bridges the gap between non-technical users and databases by converting **natural language into valid SQL queries** based on user-defined schemas.

---

## 🚀 Why This Project?

Writing SQL queries can be daunting for those unfamiliar with database languages. Whether you’re an analyst, student, or business user, Natural SQL helps you:

- Ask database questions without writing complex SQL.
- Quickly prototype queries using plain English.
- Build multiple data scenarios by uploading different schemas.

> 💡 **Goal**: Democratize access to databases by removing the need to know SQL syntax.

---

## 🔍 What Makes It Unique?

✅ **Multi-Project Support**  
Each project stores its own schema, allowing users to switch between use cases—just like navigating between chats.

✅ **User-Friendly UI**  
Built with Streamlit, the interface is intuitive: just choose or create a project, upload a JSON schema, type your question, and get SQL.

✅ **Schema-Aware AI**  
The Gemini model uses your uploaded schema to ensure queries align with your actual database structure.

✅ **Ngrok Ready (Optional)**  
Use `ngrok` to share your app with others in real-time from your local machine.

---

## ✨ Features

- 🌐 Natural language → SQL conversion using Google Generative AI (Gemini).
- 🗃️ Schema-based project isolation.
- 🔀 Project switcher in sidebar.
- 📥 Upload JSON schemas easily.
- 🧠 Gemini prompt tuning for smart and safe queries.
- 🌍 Share your app with public users using ngrok.
- 📦 Lightweight, Python-only, runs in a browser.

---

## 🔧 Requirements

- Python 3.7+
- Streamlit
- google-generativeai
- pandas
- pyngrok

---

## 🛠️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/SanjanaReddySangam/Natural-SQL.git
cd Natural-SQL
```

### 2. Install Dependencies

```bash
pip install streamlit google-generativeai pandas pyngrok
```

### 3. 🔐 Add Your API Keys

You need to set the following before running the app:

#### ✅ Gemini API Key
Get yours from [Google AI Studio](https://makersuite.google.com/app/apikey)

Open `nl2sql_streamlit.py` and **replace** this line:

```python
GEMINI_API_KEY = "your-api-key-here"
```

With your own Gemini API key, like:

```python
GEMINI_API_KEY = "AIzaSyXXXXXXX"
```

#### ✅ Ngrok Auth Token (Optional, for public sharing)

Create an account at [ngrok.com](https://dashboard.ngrok.com/) → copy your token.

Run this in your terminal:

```bash
ngrok authtoken YOUR_NGROK_TOKEN
```

---

## 🚀 Running the App

### 1. Start Locally

```bash
streamlit run nl2sql_streamlit.py
```

App will open in your browser at `http://localhost:8501`.

### 2. Share Publicly (Optional)

In a second terminal:

```bash
ngrok http 8501
```

Copy the public URL from the ngrok output and share it!

---

## 🧪 Usage Guide

### 1️⃣ Create or Select a Project  
Use the sidebar to:
- Choose an existing project, or  
- Select `<New Project>` → Enter a name → Click `Create Project`

### 2️⃣ Upload Your Schema  
Paste your schema in JSON format:
```json
{
  "tables": {
    "employees": {
      "columns": {
        "id": "INTEGER PRIMARY KEY",
        "name": "TEXT",
        "salary": "INTEGER"
      }
    }
  }
}
```
Click `Upload Schema`.

### 3️⃣ Ask Questions in Natural Language  
Examples:
- `"List all employees who earn over 50000."`
- `"What is the average salary by department?"`

Click `Generate SQL` to see the result!

---

## 📦 Example Projects

### 🏢 EmployeeManagement

**Schema includes**: `employees`, `departments`

- “List employees in the HR department”  
- “What’s the total salary expense?”

---

### 🛒 ECommerce

**Schema includes**: `products`, `orders`, `customers`, `order_items`

- “Top 5 best-selling products?”  
- “Orders placed last week?”

---

### 🎬 MovieDB

**Schema includes**: `movies`, `actors`, `roles`

- “Who acted in more than 5 movies?”  
- “List movies released after 2010.”

---

## 👩‍💻 Contributing

Want to improve it? Please fork the repo and submit a pull request!  
Ideas, bugs, and suggestions are welcome via [issues](https://github.com/SanjanaReddySangam/Natural-SQL/issues).

---

## 📄 License

MIT License © 2025 [Sanjana Reddy Sangam](https://github.com/SanjanaReddySangam)
