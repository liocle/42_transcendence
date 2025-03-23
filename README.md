# 🐝 Beepong – Real-Time Multiplayer Game with System Observability

A 42 School group project combining game development, real-time systems, and DevOps tooling.
Features real-time gameplay, tournaments, and full-stack observability via the ELK Stack.

![image](https://github.com/user-attachments/assets/495b5417-867f-4f07-bc99-bf950bea4e8d)
---

## 🧩 Project Overview
Beepong is a modular multiplayer Pong game with support for:

- AI opponents
- Tournament brackets
- Real-time play over WebSockets
- Frontend-backend separation
- Centralized log monitoring

I contributed to parts of the infrastructure and logging systems and helped bring the stack back to life in its final stages.
---
## Collaborators
- [Diego James](https://github.com/djames9)
- [Linh](https://github.com/linhtng)
- [Lionel Clerc](https://github.com/liocle)
- [Valeria](https://github.com/pixelsnow)
- [wengcychan](https://github.com/wengcychan)
---
## 🔧 Tech Stack

| Area        | Stack/Tool                                   |
|-------------|-----------------------------------------------|
| Frontend    | Vanilla JS                                    |
| Backend     | Django REST Framework, WebSockets             |
| Database    | PostgreSQL                                    |
| DevOps      | Docker, Docker Compose                        |
| Monitoring  | ELK Stack (Elasticsearch, Logstash, Kibana)   |
| Testing     | Cypress (E2E), Jest, Django tests             |

---

## Features

### Core Features
- **Multiplayer Pong Game**: Play in real-time against other players or an AI opponent.
- **Tournament Mode**: Create and join tournaments.
- **Lobby System**: Manage game lobbies.
- **AI Opponent**: Play against a AI in single-player mode.
  
### Infrastructure and Monitoring
- **ELK Stack Integration**: Provides real-time monitoring of game logs, player activity, and system performance.
  - **Elasticsearch** for indexing and searching logs.
  - **Logstash** for log processing and aggregation.
  - **Kibana** for visualizing logs and performance metrics.
- **PostgreSQL Database**: Backend database supporting persistent player data and game history.
- **Nginx Server**: Handles front-end requests, ensuring smooth game delivery and hosting static assets.

## System Architecture

The Beepong architecture is divided into multiple services running within Docker containers:

- **Frontend**: Vanilla javascript-based interface where users interact with the game.
- **Backend**: Django-based REST API that handles game logic, player management, and real-time communication.
- **Database**: PostgreSQL database stores persistent game data, user accounts, and match results.
- **ELK Stack**: Elasticsearch, Logstash, and Kibana work together to provide detailed logging and analytics for real-time monitoring.

 --- 
### 🔍 System Observability

Real-time monitoring using the ELK Stack:

- View **log levels over time** (INFO, DEBUG, FATAL)  
- Visualize **authentication success/failure rates**  
- Monitor **backend service behavior and events**  

Example Dashboard snapshots:  
![image](https://github.com/user-attachments/assets/f975ad18-e314-4603-93a2-26b5fa422402)

---
### Prerequisites
- **Docker** and **Docker Compose**: Ensure you have Docker installed to build and run the services.
- **Node.js**: For frontend development and testing.
- **Python 3.x**: For backend development (Django).
- **PostgreSQL**: As the primary database.

### Installation

1. Clone the repository:
   ```bash
   git clone git@github.com:liocle/42_transcendence.git
   cd beepong
   ```
2. Set up the environment variables:
   ```bash
   cp .env.example .env
   ```
3. Build and start the services:
   ```bash
   docker compose up_all 
   ```

## License:

This project is licensed under the MIT License.
