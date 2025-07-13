Here is your **complete and ready-to-copy `README.md`** for the **Bondwise** project — clean, fully connected, real-world, and includes your name (**Rohit**) for personal attribution.

---

````markdown
# Bondwise

A scalable mentorship platform by Rohit, powered by AI-based content moderation and context-aware security.

![UI-community](https://raw.githubusercontent.com/nz-m/SocialEcho/main/resources/UI-community.png)

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies](#technologies)
- [Schema Diagram](#schema-diagram)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [License](#license)

---

## Project Overview

**Bondwise** is a MERN-stack mentorship platform built by Rohit to help juniors connect with seniors across institutions. It enables real-time chats, Q&A forums, and community interactions — all moderated through AI-based content filtering and secured using context-aware authentication.

### 🔐 Context-Aware Security

Bondwise collects contextual data like device info, location, and IP address to fingerprint user sessions. This data is encrypted using AES and securely stored. Suspicious logins trigger OTP verification to prevent unauthorized access.

### 🧠 AI-Based Content Moderation

To ensure a safe and respectful environment, Bondwise integrates a flexible AI moderation pipeline with:

- **Perspective API** – Detects toxicity, harassment, and spam.
- **Hugging Face BART-MNLI** – Used for zero-shot classification of post content.
- **TextRazor** (optional) – Adds semantic understanding and category tagging.

A unified Flask-based interface handles these services modularly, allowing easy integration and switching.

### 👥 User Roles

Bondwise supports three user roles with defined responsibilities:

- **Admin** – Controls platform configuration, community rules, and moderator assignments.
- **Moderators** – Manage flagged content, oversee discussions, and ensure community guidelines.
- **General Users** – Ask questions, mentor others, chat, and participate in forum discussions.

---

## Features

- [x] Secure JWT-based authentication and session management
- [x] Real-time one-on-one and group messaging with Socket.io
- [x] Academic and professional profile creation
- [x] Q&A-style discussion forums
- [x] AI moderation for toxic/spam detection
- [x] Context-aware login with AES-encrypted device fingerprinting
- [x] Role-based dashboards for admin and moderators
- [x] Manual review flow for reported content
- [x] OTP/email verification for security alerts

---

## Technologies

- React.js + Redux
- Node.js + Express.js
- MongoDB
- Socket.io
- Flask (moderation gateway)
- Hugging Face Transformers (BART-MNLI)
- Perspective API
- TextRazor API (optional)
- Tailwind CSS
- JWT & Passport.js
- Nodemailer
- Crypto-js (AES encryption)
- Azure Blob Storage (for media uploads)

---

## Schema Diagram

![Schema Diagram](https://raw.githubusercontent.com/nz-m/SocialEcho/main/resources/Schema-Diagram.png)

---

## Getting Started

### Prerequisites

- Node.js (v16+)
- MongoDB or MongoDB Atlas
- (Optional) Python 3.8+ for Flask moderation server

### Installation

```bash
git clone https://github.com/nz-m/SocialEcho.git
````

Install client and server dependencies:

```bash
cd client
npm install

cd ../server
npm install
```

Create a `.env` file in both `client/` and `server/` folders using `.env.example` as reference.

Start both servers:

```bash
cd server
npm start
```

```bash
cd client
npm start
```

---

## Configuration

To set up the admin account and initial roles, run:

```bash
./admin_tool.sh
```

### Required `.env` Variables

For email service (OTP and alerts):

```env
EMAIL=
PASSWORD=
EMAIL_SERVICE=
```

For AI moderation services:

```env
PERSPECTIVE_API_KEY=
INTERFACE_API_KEY=
TEXTRAZOR_API_KEY=
```

> 🔗 API Keys:
>
> * [Perspective API](https://developers.perspectiveapi.com/s/docs-get-started)
> * [TextRazor](https://www.textrazor.com/)
> * [Hugging Face (BART MNLI)](https://huggingface.co/facebook/bart-large-mnli)

The Flask-based moderation gateway can be run locally from the `classifier_server/` directory.

> ⚠️ Note: You can run Bondwise without these keys, but moderation and security features will be disabled.

---

## Usage

### Admin Panel

* Access at `/admin`
* Manage moderators, configure APIs, and monitor flagged content

### Moderator Accounts

* Use email ending with `@mod.bondwise.com` to auto-assign moderator role
* Admin can reassign or promote users manually

### Demo

📺 [Watch Demo](https://youtu.be/Tmncayg7FeU)

---

## License

This project by **Rohit** is licensed under the [MIT License](https://github.com/nz-m/SocialEcho/blob/main/LICENSE).

```

---

