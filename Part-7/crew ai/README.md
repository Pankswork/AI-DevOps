# Day 7 - AI Agents for DevOps (Hands-on)

## 📌 Topics Covered

- What are AI Agents?
- Difference between AI Assistants and AI Agents
- Multi-Agent Systems
- Building AI Agents using CrewAI
- Running AI Agents locally using Ollama
- Automating research and report generation

---

# 🤖 What are AI Agents?

AI Agents are autonomous systems that can:

- understand a goal
- plan tasks
- execute actions
- collaborate with other agents
- generate outputs

Unlike traditional AI assistants, AI agents can perform multiple tasks automatically without requiring constant user interaction.

---

# 🧠 AI Assistant vs AI Agent

## AI Assistant

Examples:
- ChatGPT
- Gemini
- Claude

### How it works

```text
User → Prompt → AI Response
```

The user is responsible for:
- asking questions
- managing workflow
- combining outputs

### Example

```text
Research Kubernetes trends
Summarize findings
Write a blog
```

You would need to perform each step manually.

---

## AI Agent

### How it works

```text
User → Goal → Agent → Task Execution → Final Result
```

The agent can:

- break tasks into smaller steps
- gather information
- analyze data
- generate reports
- collaborate with other agents

### Example

```text
Research Kubernetes trends and create a blog report.
```

The agent handles the entire workflow automatically.

---

# 🚀 Why AI Agents Matter in DevOps

AI agents can help automate:

- infrastructure research
- incident investigations
- log analysis
- documentation generation
- monitoring reports
- cloud cost analysis
- security assessments

Instead of manually performing repetitive tasks, agents can execute them autonomously.

---

# 🛠 Hands-On Project

## Project Goal

Build a multi-agent system that:

1. Researches Kubernetes trends
2. Analyzes gathered information
3. Creates a blog-style report automatically

---

# 🏗 Project Architecture

The project uses two AI agents.

## Agent 1: Researcher

### Responsibilities

- Collect information
- Research Kubernetes trends
- Gather relevant insights
- Summarize findings

### Input

```text
Latest Kubernetes trends
```

### Output

```text
Research notes and findings
```

---

## Agent 2: Reporting Analyst

### Responsibilities

- Read research findings
- Organize information
- Generate final report
- Format content in Markdown

### Input

```text
Research data from Research Agent
```

### Output

```text
Formatted report.md
```

---

# 🔄 Workflow

```text
User Goal
      ↓
Research Agent
      ↓
Collected Findings
      ↓
Reporting Agent
      ↓
Markdown Report
```

This demonstrates how multiple agents can collaborate to complete a larger task.

---

# ⚙️ Tools Used

## CrewAI

CrewAI is an open-source framework used to build and manage AI agents.

It provides:

- agent definitions
- task orchestration
- multi-agent collaboration
- workflow management

---

## Ollama

Ollama allows running Large Language Models locally.

Benefits:

- free to use
- private
- no API costs
- works offline

---

## Llama 3.1

The project uses:

```text
Llama 3.1
```

as the underlying model for agent reasoning and content generation.

---

# 📁 Project Structure

```text
project/
│
├── agents.yaml
├── tasks.yaml
├── crew.py
├── main.py
├── reports.md
└── config/
```

---

# 📄 Agent Configuration

Agents are defined inside YAML files.

Example responsibilities:

## Research Agent

```yaml
role: Kubernetes Researcher
goal: Find latest Kubernetes trends
backstory: Expert Kubernetes analyst
```

---

## Reporting Agent

```yaml
role: Technical Writer
goal: Create detailed report
backstory: Experienced DevOps blogger
```

---

# 📋 Task Configuration

Tasks define what each agent should do.

Example:

```yaml
task:
  description: Research latest Kubernetes trends
```

and

```yaml
task:
  description: Create a detailed report from research findings
```

---

# ▶ Running the Project

## Create Virtual Environment

```bash
python -m venv venv
```

Activate:

### Linux / Mac

```bash
source venv/bin/activate
```

### Windows

```powershell
.\venv\Scripts\activate
```

---

## Install CrewAI

```bash
pip install crewai
```

---

## Run Ollama

```bash
ollama serve
```

---

## Pull Llama Model

```bash
ollama pull llama3.1
```

---

## Execute Project

```bash
python main.py
```

---

# 📊 Output

The system automatically generates:

```text
reports.md
```

The report contains:

- Kubernetes trends
- analysis
- observations
- blog-style formatting

without requiring manual research.

---

# 💡 Advantages of AI Agents

## Automation

Agents can execute complete workflows automatically.

---

## Collaboration

Multiple agents can work together on different tasks.

---

## Productivity

Reduces manual effort.

---

## Scalability

Can be extended with more agents.

Examples:

- Security Agent
- Cloud Cost Agent
- Monitoring Agent
- Incident Response Agent

---

# ⚠ Limitations

Local models may:

- have older knowledge
- produce less accurate responses
- require more tuning

Compared to enterprise APIs:

- OpenAI
- Anthropic
- Gemini

local models can sometimes provide lower-quality outputs.

---

# 🧠 My Understanding

AI Agents are a major step beyond traditional chatbots.

Instead of responding to a single prompt, they can:

- reason through tasks
- collaborate
- execute workflows
- produce complete deliverables

This makes them highly useful for DevOps automation and operational tasks.

---

# 📚 What I Learned

- Difference between AI assistants and AI agents
- Basics of multi-agent systems
- Introduction to CrewAI
- Running AI agents locally using Ollama
- Agent and task configuration using YAML
- Automated research and report generation
- Real-world use cases of AI agents in DevOps

---

# 🚀 Future Improvements

Possible enhancements to this project:

- Add web search capabilities
- Add Kubernetes documentation lookup
- Generate PDF reports
- Integrate Slack notifications
- Create DevOps incident analysis agents
- Build cloud cost optimization agents
- Add monitoring and observability agents