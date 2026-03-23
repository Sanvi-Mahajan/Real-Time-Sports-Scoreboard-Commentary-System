# Real-Time Sports Scoreboard & Commentary System

A backend system that delivers **live sports scores and commentary in real-time** using WebSockets, combined with REST APIs for efficient data handling.

---

## 🚀 Overview

This project simulates a real-world **event streaming system** where users can subscribe to live matches and receive instant updates without unnecessary network overhead.

Instead of naive broadcasting, the system uses a **room-based subscription model** to deliver targeted updates only to relevant users.

---

## ⚙️ Architecture

The system follows a **hybrid model**:

- **Polling (REST APIs)** → Detect new matches and updates  
- **WebSockets (ws)** → Push real-time commentary and score updates  

This balances:
- ⚡ Low latency (real-time updates)
- 📉 Reduced server load (no constant polling from clients)

---

## 🔥 Key Features

- **Real-Time Updates**
  - Live scores and commentary pushed instantly via WebSockets  

- **Room-Based Subscription**
  - Users subscribe to specific matches
  - Only receive updates for selected matches  

- **Custom Connection Management**
  - Heartbeat mechanism (ping/pong)
  - Reconnection handling
  - Connection lifecycle management  

- **Authentication & Authorization**
  - Controlled access to WebSocket connections  
  - Scoped message delivery per user/session  

- **Rate Limiting & Safeguards**
  - Prevents abuse and excessive connections  

---

## 🛠 Tech Stack

- **Backend:** Node.js, Express  
- **Real-Time:** WebSockets (`ws`)  
- **Database:** PostgreSQL (Neon)  
- **API Layer:** REST APIs  

---

## 🧠 Design Decisions

- **WebSockets over polling:**  
  Reduces latency and avoids repeated client requests  

- **Room-based architecture:**  
  Improves scalability by avoiding global broadcasts  

- **Hybrid system (Polling + WebSockets):**  
  Ensures efficient match discovery while keeping live updates real-time  

---

