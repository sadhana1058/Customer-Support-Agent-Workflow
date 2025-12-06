# Customer-Support-Agent-Workflow
# 📬 Inbox Customer Support Agent – n8n Workflow

This repository contains an **automated email triage + AI response workflow** built using **n8n**.  
The workflow connects Gmail with an LLM-powered text classifier and an AI agent to automatically **label**, **classify**, and **respond** to incoming emails.

---

## 🚀 Features

### ✓ Gmail Trigger  
The workflow begins whenever a new email arrives. It captures:
- Sender information  
- Subject  
- Message body  

---

### ✓ Text Classification (via Ollama Model)  
Incoming emails are passed to an LLM model for classification into categories such as:

- **Customer Support**
- **Finance/Billing**
- **High Priority**
- **Promotions**

The classification result determines what Gmail label is applied.

---

### ✓ Automatic Labeling in Gmail  
Based on the classifier output, the workflow applies the appropriate label using Gmail’s API.  
This helps in **organizing your inbox automatically**.

---

### ✓ AI Agent for Auto-Responses  
An Ollama Chat Model is used to:
- Read the original email  
- Understand the context  
- Generate a helpful, professional reply  

This turns the workflow into a **smart customer-support assistant**.

---

### ✓ Automated Email Reply  
The generated AI response is sent back to the sender through Gmail’s “Reply to Message” node.

---

## 🧩 Node Breakdown

| Node | Description |
|------|-------------|
| **Gmail Trigger** | Starts workflow on new email |
| **Text Classifier** | LLM-based classification of email content |
| **Add Label to Message** | Applies Gmail labels |
| **AI Agent** | Generates contextual replies |
| **Reply to Message** | Sends the reply back to the user |
| **Ollama Model / Chat Model** | Local LLM powering classification + response |

---

## Workflow Architecture
Incoming Email
↓
Text Classifier (Ollama)
↓
Apply Gmail Label
↓
AI Agent → Generate Response
↓
Reply to Message (Gmail)

---

## 🛠️ Requirements

- **n8n** (Cloud or Self-hosted)
- **Gmail OAuth Credentials**
- **Ollama installed locally**
- LLM models (e.g., `llama3`, `mistral`, etc.) available in Ollama

---

## 📄 Use Cases

- Customer support automation  
- Auto-triage of billing, promotions, or high-priority messages  
- Inbox organization  
- Automatic reply drafting  
- Reducing manual workload for service teams  

---

## ▶️ How to Run

1. Import the workflow JSON into n8n.
2. Connect Gmail OAuth credentials to:
   - Gmail Trigger  
   - Add Label to Message  
   - Reply to Message  
3. Install and run **Ollama** on your machine.
4. Ensure the models referenced in the workflow exist.
5. Activate the workflow.

---

## ⭐ Optional Enhancements

- Add vector memory for personalized responses  
- Add multi-step decision logic for complex emails  
- Extend categories in the classifier  
- Add Slack or Notion notifications  

---

<img width="722" height="267" alt="Screenshot 2025-12-05 at 10 31 20 PM" src="https://github.com/user-attachments/assets/e2b96ac2-87e5-4664-8867-582a8ea70fad" />
