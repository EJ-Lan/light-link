# LightLink — Lightweight Client-to-Client Messaging App

## Project Overview

LightLink is a lightweight, efficient client-to-client messaging application built in C, designed to help users communicate over a network with minimal resource usage.  

---

## Core Features

### 1. Client-Server Architecture  
- Clients connect to a central server to facilitate messaging.  
- Server manages multiple concurrent client connections.

### 2. Real-time Messaging  
- Clients can send and receive text messages instantly.  
- Messages broadcasted to all connected clients.

### 3. User Identification  
- Each client sets a unique username on connection.  
- Messages include sender’s username for clarity.

### 4. Private Messaging  
- Ability for clients to send direct messages to specific users.

### 5. Connection Management  
- Handle client connect/disconnect events gracefully.  
- Notify users when participants join or leave.

### 6. Multi-Client Support  
- Server handles multiple clients simultaneously using threading or multiplexing (`select()`/`poll()`).

---

## Stretch Goals

### 1. Encryption  
- Implement simple encryption (e.g., XOR cipher or integration with OpenSSL) to secure messages.

### 2. File Transfer  
- Support sending files between clients.

### 3. Chat Rooms / Channels  
- Allow creation and joining of multiple chat rooms.  
- Clients can switch between rooms dynamically.

### 4. Offline Messaging  
- Server stores messages for offline users and delivers upon reconnection.

### 5. Command Parsing  
- Add support for commands like:  
  - `/list` — list connected users  
  - `/nick <newname>` — change username  
  - `/msg <user> <message>` — private message

### 6. Text-Based User Interface (TUI)  
- Implement a terminal UI with `ncurses` or similar for better client experience.

### 7. Logging and History  
- Server maintains chat logs; clients can request message history.

---

## Technical Notes

- Written in C, focusing on use of sockets and networking APIs.  
- Utilize multi-threading or asynchronous I/O for scalability.  
- Lightweight with minimal external dependencies.  
- Portable design for running on Raspberry Pi and other Unix-like systems.

---

## Future Enhancements

- GUI client application  
- Mobile client integration  
- Support for multimedia messages  
- Integration with existing messaging protocols

---

*LightLink aims to be a compact yet powerful playground for networking and C programming enthusiasts.*
