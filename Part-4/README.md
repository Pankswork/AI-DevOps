# Day 4 - AI-Powered Shell Scripting & CLI Automation

## 📌 Topics Covered

- Using AI to improve Bash scripting
- AI-assisted Python scripting
- CLI automation using AI tools
- Prompt engineering for scripting tasks
- Understanding how AI can speed up DevOps workflows

---

# 🤖 AI-Assisted Shell Scripting

AI tools can help generate:
- shell scripts
- automation scripts
- infrastructure setup commands
- debugging steps
- AWS CLI commands
- Kubernetes commands

Instead of writing everything manually, AI can assist by:
- generating boilerplate code
- explaining errors
- improving scripts
- suggesting best practices

---

# 🛠 Hands-On Practice

## Installing GitHub Copilot

Installed the :contentReference[oaicite:0]{index=0} extension on:
- VS Code
- Antigravity

### Steps Performed

1. Open Extensions tab
2. Search for `GitHub Copilot`
3. Install the extension
4. Login using GitHub account
5. Enable AI suggestions inside the editor

### My Understanding

GitHub Copilot works like an AI coding assistant directly inside the IDE.

It can:
- auto-complete code
- generate scripts
- suggest commands
- help with debugging
- improve productivity

---

# 🧠 Mini Challenge

## Prompt

```bash
Generate a shell script to create a VPC in AWS with all best practices.
```

---

# 📌 Important Things Learned While Prompting AI

I noticed that AI generates much better scripts when the prompt contains:
- clear requirements
- file names
- variable names
- expected output
- detailed context

---

# ✅ Better Prompt Example

```bash
Generate a Bash script named create_vpc.sh using AWS CLI.

Requirements:
- Create VPC
- Create public and private subnets
- Enable DNS support
- Add tags
- Use variables for CIDR blocks
- Include error handling
- Follow AWS best practices
- Add comments for readability

If anything is unclear, ask questions before generating the script.
```

---

# 📌 Prompt Engineering Notes

## Adding File Name for Context

Providing file names helps AI understand:
- project structure
- scripting purpose
- expected output type

Example:

```bash
create_vpc.sh
deploy_app.sh
backup_logs.py
```

---

## Adding Description for More Context

Detailed descriptions improve AI-generated output quality.

Example:

```bash
Create a production-ready AWS VPC setup script with proper subnet separation and tagging.
```

---

## Using Variables

Using variables makes scripts:
- reusable
- cleaner
- easier to maintain

Example:

```bash
VPC_CIDR="10.0.0.0/16"
AWS_REGION="ap-south-1"
```

---

## Asking AI to Clarify Missing Information

One important thing I learned is that prompts should allow AI to ask follow-up questions if requirements are unclear.

Example:

```bash
If any requirement is unclear, ask before generating the script.
```

This helps avoid incomplete or incorrect automation scripts.

---

# 💡 Example AI-Generated AWS CLI Commands

## Create VPC

```bash
aws ec2 create-vpc --cidr-block 10.0.0.0/16
```

---

## Create Subnet

```bash
aws ec2 create-subnet \
--vpc-id vpc-12345 \
--cidr-block 10.0.1.0/24 \
--availability-zone ap-south-1a
```

---

## Enable DNS Support

```bash
aws ec2 modify-vpc-attribute \
--vpc-id vpc-12345 \
--enable-dns-support
```

---

# 🧠 What I Learned

- AI can speed up scripting and automation tasks
- Better prompts generate better DevOps scripts
- Context and detailed requirements improve AI accuracy
- GitHub Copilot can assist with Bash and Python scripting
- Prompt engineering is important for infrastructure automation
- AI should still be reviewed manually before production use

---

# ⚠ Important Note

AI-generated scripts are useful for learning and automation, but they should always be reviewed carefully before running in production environments.

Especially for:
- AWS infrastructure
- security groups
- IAM permissions
- production deployments