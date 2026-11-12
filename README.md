# Restaurant Task Automation System

A workflow automation project built with **n8n**, **Telegram**, **Google Gemini AI**, and **Gmail** to streamline task communication and coordination within a restaurant.

## Project Overview

This project simulates a restaurant management communication system involving three roles:

- **Manager (Salta3):** Sends main instructions through Telegram.
- **Supervisor (Chfiq):** Receives instructions via email and Telegram notifications, then sends operational tasks.
- **Executor (Spongebob):** Receives the final task instructions via email.

The goal is to reduce manual communication, improve task distribution, and make internal coordination more organized.

## Architecture

The system consists of two automated workflows:

### 1. Unified Telegram Router

- Receives incoming Telegram messages through a single Telegram Trigger.
- Uses a Switch node to route messages based on Telegram Chat ID.
- Processes manager instructions using Google Gemini AI.
- Sends structured instructions to the supervisor via Gmail.
- Processes supervisor messages through a separate AI chain.
- Sends final operational tasks to the executor via Gmail.
- Sends Telegram confirmation messages after processing.

### 2. Email-to-Telegram Notifier

- Monitors the supervisor's Gmail inbox using Gmail Trigger.
- Detects incoming unread task emails.
- Sends Telegram notifications when new instructions arrive.
- Marks processed emails as read.

## Technologies Used

- n8n
- Telegram Bot API
- Google Gemini AI
- Gmail
- LLM Chains
- Switch Node
- Workflow Automation

## Key Concepts Demonstrated

- Workflow design and automation
- Conditional routing
- AI-powered text processing
- API integrations
- Event-driven automation
- Multi-workflow architecture
- Automated notifications
- Email-based task distribution

## Project Status

**Learning Project — First Automation Portfolio Project**

This project is a practical learning exercise demonstrating how multiple services can be connected to automate a business communication process.

## Future Improvements

- Add error handling and retry mechanisms.
- Implement sender authentication and access control.
- Prevent duplicate email processing.
- Validate AI-generated outputs.
- Add task tracking using Google Sheets.
- Improve workflow monitoring and reliability.

---

*Built as part of my journey into AI Automation and workflow engineering.*
