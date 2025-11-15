# Capstone_Project2025
InsightOps is an AI-powered enterprise data agent that turns natural-language questions into SQL queries, Python analysis, charts, and validated insights. Built with Google’s ADK patterns, it provides planning, tool execution, memory, evaluation, and full observability.
# InsightOps — Enterprise Data Analysis Agent  
### *Google × Kaggle Agents Intensive Capstone Project*

![Thumbnail](<img width="1024" height="1024" alt="Thumbnail" src="https://github.com/user-attachments/assets/beef67d4-bc0d-4c00-a4e8-bf1fd7f09729" />
)

InsightOps is an enterprise-ready AI agent that transforms **natural language business questions** into **reproducible, auditable, and validated data analyses**.  
Built following Google’s Agent Development Kit (ADK) patterns, InsightOps demonstrates how an AI agent can orchestrate tools like SQL, Python, and visualization modules to automate real business analytics workflows.

---

## 🏷️ Badges

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-success)
![AI Agent](https://img.shields.io/badge/AI-Agent-orange)
![ADK](https://img.shields.io/badge/Google-ADK-informational)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

# 📚 Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Architecture](#architecture)
- [Demo](#demo)
- [Memory](#memory)
- [Evaluator](#evaluator)
- [Observability](#observability)
- [Project Structure](#project-structure)
- [Setup & Installation](#setup--installation)
- [Deployment](#deployment)
- [Artifacts](#artifacts)
- [Credits](#credits)

---

## 📍 Overview

InsightOps enables users to ask questions such as:

- "Why did churn increase in Q3?"
- "Give me a region-wise revenue summary for the past 6 months."
- "Exclude Plan C — how do the insights change?"

The agent then automatically:
1. interprets the query  
2. generates a multi-step plan  
3. executes SQL & Python tasks  
4. produces charts  
5. validates the result  
6. logs every step  
7. returns a clean final analysis  

It behaves like a **real enterprise analyst**, not a chatbot.

---

# ✨ Key Features

### 🔹 Multi-Step LLM Planner  
Breaks down queries into structured JSON plans.

### 🔹 Executor  
Runs SQL, Python, and plotting operations step-by-step.

### 🔹 Tools  
- **SQLTool** — safe Pandas-based query execution  
- **PythonTool** — metrics, filters, stats  
- **PlotTool** — generates charts saved to artifacts  

### 🔹 Memory  
Stores conversation history, filters, results — allowing follow-up questions.

### 🔹 Evaluator  
Checks correctness, completeness, safety, and formatting.

### 🔹 Observability  
Every tool call, input, output, and exception is logged.

### 🔹 Deployment Ready  
Included Dockerfile + Cloud Run setup.

---

# 🧱 Architecture

InsightOps contains **five core components**:

### **1. Planner (LLM)**
- Converts natural language into clear, step-by-step plans
- Prevents hallucination by enforcing deterministic structure

### **2. Executor**
- Runs each step in order  
- Passes intermediate outputs  
- Captures timestamps & tool traces  

### **3. Tool Layer**
- **SQLTool**: safe SQL-like queries  
- **PythonTool**: computes metrics & transformations  
- **PlotTool**: generates visuals  

### **4. Memory**
- Tracks user intent and previous outputs  
- Enables iterative analysis  

### **5. Evaluator & Observability**
- Validates every result  
- Logs everything under `/artifacts/`  

---

