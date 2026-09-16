# AI Calendar Assistant — Telegram Bot with n8n

An AI-powered Telegram bot that lets you **view, create, and update your Google Calendar events** just by chatting in plain language. No need to open the Calendar app — just send a message on Telegram, and the AI Agent handles the rest.

Built with **n8n**, **Google Gemini**, and the **Google Calendar API**.

---
###  Project Screenshots

* 🔗 [View Bot Welcome Screen](assets/2jpeg)
* 🔗 [View n8n Workflow Architecture](assets/image_4bb21ba%20(1).jpg)
* 🔗 [View LinkedIn Demo Screenshot](assets/linkedin2.PNG)
##  Overview

This project is an automated workflow (built in n8n) that connects **Telegram** to **Google Calendar** through an **AI Agent**. The agent understands natural language requests and decides which calendar action to perform — checking your schedule, adding a new event, or updating an existing one — then replies back to you on Telegram.

---

##  Features

- 💬 **Chat naturally** — talk to your calendar like you're texting a friend
- 📅 **View events** — ask what's on your schedule
- ➕ **Create events** — add new events by just describing them
- ✏️ **Update events** — change the date, time, or details of an event
- 🧠 **Conversation memory** — the agent remembers earlier messages in the chat for context
- 🤖 **Powered by Google Gemini** — for understanding and responding to user requests

---

##  Tech Stack

| Component            | Tool / Service          |
|-----------------------|--------------------------|
| Workflow Automation   | [n8n](https://n8n.io)   |
| Chat Interface        | Telegram Bot API         |
| AI Model              | Google Gemini            |
| Calendar Integration  | Google Calendar API      |

---

##  How It Works

1. **Telegram Trigger** — listens for new incoming messages from the user
2. **Normalize Input** — cleans and formats the message before it reaches the AI
3. **AI Agent** — the core of the workflow, which:
   - Uses **Google Gemini Chat Model** to understand what the user wants
   - Uses **Simple Memory** to remember the ongoing conversation
   - Has access to three calendar tools:
     - **Get Calendar Events** — fetches existing events
     - **Create Calendar Event** — adds a new event
     - **Update Calendar Event** — edits an existing event
4. **Send a Text Message** — sends the AI Agent's reply back to the user on Telegram

---

##  Setup & Installation

1. **Import the workflow**
   - Download `workflow.json` from this repo (or copy it) and import it into your n8n instance.
2. **Create a Telegram Bot**
   - Talk to [@BotFather](https://t.me/BotFather) on Telegram and create a new bot to get a bot token.
3. **Connect credentials in n8n**
   - Add your **Telegram** bot token as a credential.
   - Add your **Google Gemini** API key as a credential.
   - Add your **Google Calendar** account using OAuth2.
4. **Activate the workflow**
   - Turn the workflow to "Active" in n8n so it starts listening for Telegram messages.
5. **Start chatting**
   - Open your bot on Telegram and start sending messages.

---

##  Example Commands

- "What's on my calendar tomorrow?"
- "Schedule a meeting with Ali at 3 PM on Friday."
- "Move my dentist appointment to next Monday at 10 AM."

---

##  Future Improvements

- Add a "delete event" tool
- Support multiple calendars (work / personal)
- Add voice message support
- Add reminders before events start

---

##  License

This project is open source and available under the [MIT License](LICENSE).

---

##  Author

Built by **[Raffia Batool]** — feel free to connect or contribute!
