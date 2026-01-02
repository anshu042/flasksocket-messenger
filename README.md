# FlaskSocket Messenger

A real-time chat application built with **Flask**, **Socket.IO**, and **SQLAlchemy**. This application allows users to register, create private chat rooms, and exchange instant messages with a modern "Dark Glass" UI.

## 🚀 Features

* **Real-time Messaging:** Instant bi-directional communication using WebSockets (Flask-SocketIO).
* **User Authentication:** Secure Signup and Login system with password hashing (PBKDF2 SHA256).
* **Private Chat Rooms:** Create distinct chat rooms between users via email invitation.
* **Persistent Chat History:** Messages are stored in a SQLite database and retrieved upon loading the chat.
* **Chat Management:**
    * Clear chat history for a specific room.
    * Remove chats/users from your sidebar.
* **Modern UI:** Custom CSS featuring a responsive split-pane login and a glassmorphism-styled chat interface.

## 🛠️ Tech Stack

* **Backend:** Python, Flask
* **WebSockets:** Flask-SocketIO
* **Database:** SQLite (Default), SQLAlchemy ORM
* **Frontend:** HTML5, CSS3, JavaScript (Socket.IO client, jQuery)
* **Data Analysis (Planned):** Pandas, Matplotlib
* **Server:** Gunicorn (Configuration provided)

## 📂 Project Structure

```text
FlaskSocket-Messenger/
├── myapp/
│   ├── __init__.py          # App factory and DB initialization
│   ├── config.py            # App configuration variables
│   ├── database.py          # Database models (User, Chat, Message)
│   ├── views.py             # HTTP routes (Auth, Chat logic)
│   ├── static/              # CSS, JS, and Images
│   └── templates/           # HTML Templates (auth.html, chat.html, etc.)
├── instance/
│   └── database.db          # SQLite Database (generated on run)
├── .env                     # Environment variables
├── gunicorn_config.py       # Production server config
├── requirements.txt         # Python dependencies
└── server.py                # Application entry point
