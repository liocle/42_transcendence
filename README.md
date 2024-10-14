# 🐝 Beepong - Multiplayer Pong Game with Real-Time Monitoring
🚧This was the final group project of Hive Helsinki (42 Network). This project passed evaluation, but still requires polishing, this README introduces 
the main features that have been planned, implemented... A work in progress ...🚧
🏓

![BeePong design vision](BeePong_vision_240615.png)
[Design in Figma](https://www.figma.com/design/42yVXZOi6yLRxybTmu8lhG/BEE-PONG?node-id=0-1&t=JObdYVC2Pk32AxSm-1)

## Overview

Beepong is a real-time multiplayer Pong game, developed as part of a group project. The goal of the game is to provide an engaging gaming experience for multiple players, complete with AI opponent functionality, tournament logic, and a customizable gaming lobby. The project integrates both **front-end** and **back-end** systems, supported by a robust infrastructure that enables real-time monitoring, logging, and analytics using the **ELK (Elasticsearch, Logstash, Kibana)** stack.

The project is designed to be modular, supporting core game functionality alongside optional features such as advanced logging, AI-based opponents, and real-time game monitoring, ensuring flexibility for future expansions and improvements.

## Collaborators
- [Diego James](https://github.com/djames9)
- [Linh](https://github.com/linhtng)
- [Lionel Clerc](https://github.com/liocle)
- [Valeria](https://github.com/pixelsnow)
- [wengcychan](https://github.com/wengcychan)


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

### Testing
- **Cypress**: End-to-end testing simulating user interactions and verifying the integrity of the front-end. Currently only in this PR:
https://github.com/BeePong/42_transcendence/pull/91
    
  
## System Architecture

The Beepong architecture is divided into multiple services running within Docker containers:

- **Frontend**: Vanilla javascript-based interface where users interact with the game.
- **Backend**: Django-based REST API that handles game logic, player management, and real-time communication.
- **Database**: PostgreSQL database stores persistent game data, user accounts, and match results.
- **ELK Stack**: Elasticsearch, Logstash, and Kibana work together to provide detailed logging and analytics for real-time monitoring.

## Getting Started

### Prerequisites
- **Docker** and **Docker Compose**: Ensure you have Docker installed to build and run the services.
- **Node.js**: For frontend development and testing.
- **Python 3.x**: For backend development (Django).
- **PostgreSQL**: As the primary database.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/beepong.git
   cd beepong
   ```
2. Set up the environment variables:
   ```bash
   cp .env.example .env
   ```
3. Build and start the services:
   ```bash
   docker compose up 
   ```
### Running Tests
- Cypress: For end-to-end testing:
   ```bash
   docker compose run --rm cypress
   ```
## License:

This project is licensed under the MIT License.
