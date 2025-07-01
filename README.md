# 🧠 AI Automation Suite 

A collection of intelligent automation flows powered by **n8n**, integrated with **AI agents** to streamline user interactions and daily workflows. This project showcases real-world applications of AI-powered agents handling natural language instructions.

---

## 🔧 Project Structure
```
├── PromptAgent_Tool.json/ # n8n workflow to generate agent system prompts
├── Calender_scheduling.json/ # n8n flow for calendar task automation
├── README.md
```

---

## 📌 1. AI Prompt Generator for AI Agents

### 🔍 Description:
This automation enables users to **generate context-rich prompts** for AI agents based on a single user instruction. It dynamically constructs a well-formed system prompt that defines how the AI agent should behave.

### ⚙️ Features:
- Accepts a natural language instruction like:  
  `"You are a software engineer that helps with Go, TypeScript, and Rust."`
- Converts it into a detailed `system message` ready for use with OpenAI or LangChain agents
- Built with n8n's **Webhook → OpenAI → Response** flow

### 💡 Use Case:
Perfect for dynamically spawning agents in multi-agent frameworks like LangGraph, CrewAI, or Agent-LLM with purpose-specific behavior.

### 🧪 Example Output:
```json
{
  "role": "system",
  "content": "You are an assistant developed by Siddhant Munjamkar. You are helpful, creative, and expert in Go, TypeScript, and Rust. Respond concisely and solve code-related problems efficiently."
}

## 📆 Module 2: AI Calendar Scheduler

### 📝 Description

Handles **Create, Read, Update, and Delete** operations on calendar events using natural language inputs interpreted by an AI agent.

This module enables users to manage their schedule without technical commands — just plain English.

---

### 💡 Example Inputs

- `"Schedule a project review call with Meera on Tuesday at 11 AM"`
- `"Delete the standup on Friday"`
- `"Reschedule the marketing sync to 4 PM tomorrow"`

---

### 🧠 Workflow Logic

- 🛰️ **Webhook Trigger**  
  Receives user input via API or form

- 🧠 **OpenAI Node**  
  Interprets the user's intent and extracts:
  - Action (create/update/delete/fetch)
  - Event title
  - Date & time

- 🔁 **Switch / Router Node**  
  Routes to appropriate action logic (CRUD)

- 📅 **Calendar Action Nodes**  
  Executes on:
  - Google Calendar API  
  - Notion API *(optional, if integrated)*

- 📤 **Respond Node**  
  Sends user a confirmation or error message

---

### 🧾 Example Parsed Output (From AI Parser)
```json
{
  "intent": "create",
  "title": "project review call",
  "date": "2025-07-04",
  "time": "11:00",
  "platform": "Google Calendar"
}
