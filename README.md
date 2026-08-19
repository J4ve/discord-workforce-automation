# Enterprise Workforce Automation & Community Gateway Bot (Case Study)

> [!NOTE]
> **Confidentiality Disclaimer**: This repository is an architectural case study of an internal operations automation service built for a distributed digital media agency. Proprietary source code, specific business logic, internal database credentials, API keys, and company data have been omitted in compliance with non-disclosure agreements (NDA).

---

## Executive Summary
Engineered an asynchronous operational gateway service and Discord bot designed to automate contractor shift notifications, performance tracking, gamified milestone achievements, and cross-platform synchronization with an internal HR web service.

---

## Key System Modules & Engineering Contributions

### 1. Discord Gateway & Asynchronous Command Architecture
* **Modular Cog-Based System**: Structured slash commands using `discord.app_commands` and modular Cogs for clean separation of concerns between administration, notifications, and engagement features.
* **Non-Blocking Gateway Processing**: Built on `discord.py` and `asyncio`, maintaining a persistent low-latency connection with zero blocking I/O calls.

### 2. Operational Metrics & Gamification Engine
* **Performance Leaderboards**: Engineered an activity scoring engine backed by embedded SQLite to compute real-time leaderboards and engagement statistics.
* **Automated Milestone Competitions**: Built dynamic badge tracking and milestone verification logic, automatically granting recognition roles upon metric thresholds.

### 3. Cross-Platform API Integration
* **Outbound Asynchronous HTTP Client**: Integrated `aiohttp` to poll and sync schedule assignments, shift logs, and operational rosters from an external Next.js HR platform without hosting an exposed HTTP server.
* **Automated Shift & Schedule Reminders**: Background cron task workers dispatching direct alerts and channel pings for upcoming contractor shift transitions.

### 4. Data Layer & Storage
* **Lightweight Embedded Persistence**: Utilized SQLite with hand-optimized relational schemas for high-speed local read/write queries without ORM overhead.
* **Fail-Safe Logging & Diagnostics**: Standardized structured application logging with rotating file handlers for production reliability on Linux VPS environments.

---

## Tech Stack

| Domain | Technologies |
| :--- | :--- |
| **Language & Runtime** | Python 3.12, Asyncio |
| **API & Framework** | `discord.py` 2.6.4 (App Commands / Cogs) |
| **Database & Storage** | SQLite (`sqlite3` normalized relational tables) |
| **Networking & HTTP** | `aiohttp` (Asynchronous Client) |
| **Environment & Config**| `python-dotenv`, Structured Logging |
| **Deployment** | Linux Daemon (Systemd / Oracle Cloud VM) |

---

## Architectural Highlights
* **Pure Gateway Architecture**: Operates exclusively as a secure outbound client with zero open inbound HTTP ports, eliminating attack surface.
* **Resilient State Management**: SQLite transactions ensure reliable record-keeping for engagement events and notification history.
