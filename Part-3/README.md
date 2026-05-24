# 🐳 Dockerfile Generator

A simple GenAI-powered project that generates optimized Dockerfiles based on the programming language provided by the user.

This project uses:
- Ollama
- Llama3 model
- Python

The goal of this project is to understand how AI can assist in DevOps automation tasks like generating Dockerfiles using best practices.

---

# 📌 Features

- Generate Dockerfiles for different programming languages
- Uses local LLM with Ollama
- Beginner-friendly AI + DevOps project
- Helps understand prompt engineering and automation

---

# 🛠 Tech Stack

- Python
- Ollama
- Llama3
- Docker concepts

---

# 📋 Prerequisites

## Install Ollama

### Linux

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### MacOS

```bash
brew install ollama
```

---

# ▶ Start Ollama Service

```bash
ollama serve
```

---

# 📥 Pull Llama3 Model

```bash
ollama pull llama3.2:1b
```

---

# 🚀 Project Setup

## Create Virtual Environment

### Linux / MacOS

```bash
python3 -m venv venv
source venv/bin/activate
```

### Windows

```powershell
python -m venv venv
.\venv\Scripts\activate
```

---

# 📦 Install Dependencies

```bash
pip install -r requirements.txt
```

---

# ▶ Run the Application

```bash
python generate_dockerfile.py
```

---

# 💡 How This Project Works

1. User enters a programming language
2. Python script sends the prompt to Ollama
3. Ollama uses the Llama3 model locally
4. AI generates a Dockerfile
5. The generated Dockerfile follows basic containerization best practices

---

# 📝 Example Usage

```bash
python generate_dockerfile.py
```

### Input

```bash
Enter programming language: python
```

### Example Output

```dockerfile
FROM python:3.11-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD ["python", "app.py"]
```

---

# 🧠 What I Learned

- Basics of Ollama and local LLMs
- How AI models can help automate DevOps tasks
- Prompt engineering fundamentals
- Dockerfile structure and optimization basics
- Python API integration with AI models

---

# ⚠ Troubleshooting

## Ollama Service Not Running

Start Ollama manually:

```bash
ollama serve
```

---

## Model Not Found

Download the model again:

```bash
ollama pull llama3.2:1b
```

---

## Virtual Environment Issues

Make sure the virtual environment is activated before installing dependencies.

---

# 🚀 Future Improvements

- Add support for more programming languages
- Add Docker Compose generation
- Build a simple web UI
- Add Kubernetes YAML generation
- Improve Dockerfile optimization logic