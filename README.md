# AI-Powered Customer Complaint Management & Escalation System

An intelligent, automated customer complaint management system built using **n8n, AI, RAG, Google Sheets, and Telegram** to analyze complaints, generate relevant responses, retrieve customer transaction records, and escalate critical issues to managers.

## Project Overview

This project automates customer support operations by combining AI-based complaint analysis with Retrieval-Augmented Generation (RAG) and database integration.

The system automatically classifies incoming complaints into three priority levels:

- 🟢 **LOW:** Handles general queries, FAQs, and basic troubleshooting using RAG. Customer-specific database records are retrieved only when required.
- 🟡 **MEDIUM:** Investigates customer issues using knowledge-base information and transaction records when necessary. Complaints are optionally registered in Google Sheets for further tracking.
- 🔴 **HIGH:** Handles critical complaints, checks relevant records, registers the complaint, generates a response, and immediately alerts the manager through a dedicated Telegram bot.

## Key Features

- AI-powered complaint analysis and priority classification
- Automated customer responses using RAG
- Customer transaction verification through Google Sheets
- Dynamic database lookup using `need_database`
- Conditional complaint registration using `need_database_append`
- Automatic ticket ID generation and complaint tracking
- High-priority escalation through a dedicated Manager Telegram Bot
- Structured, real-time complaint notifications

## Technology Stack

- **n8n:** Workflow automation and orchestration
- **AI/LLM:** Complaint analysis and response generation
- **RAG + Qdrant:** Knowledge retrieval from approved support documentation
- **Ollama:** Embedding generation
- **Google Sheets:** Transaction records and complaint storage
- **Telegram Bot API:** Customer communication and manager alerts
- **JavaScript:** Data processing, routing, and notification formatting

## Workflow Architecture

Customer Complaint → AI Complaint Analyzer → Priority Classification → RAG/Database Retrieval → AI Response → Conditional Complaint Registration → Manager Escalation (HIGH only)

## Project Objective

To reduce manual customer support workload, improve complaint resolution efficiency, and ensure critical issues receive timely managerial attention through intelligent, automated workflows.
