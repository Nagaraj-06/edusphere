<div align="right">
<a target="_blank" href="https://www.linkedin.com/in/nagaraj-r-4265272b8/">
  <img src="https://img.shields.io/badge/-0d1117?logo=linkedin" width="40" height="30">
</a>
<a target="_blank" href="https://github.com/Nagaraj-06">
  <img src="https://img.shields.io/badge/-0d1117?logo=github" width="40" height="30">
</a>
</div>

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=220&section=header&text=%F0%9F%93%98%20EduSphere&fontSize=72&fontColor=ffffff&fontAlignY=38&desc=Collaborative%20Course%20Discussion%20Platform&descAlignY=58&descSize=20&animation=fadeIn" />

<br/>

[![Repo](https://img.shields.io/badge/Repository-Dicuss--Forum-181717?logo=github)](https://github.com/Nagaraj-06/Dicuss-Forum)
[![Commits](https://img.shields.io/github/last-commit/Nagaraj-06/Dicuss-Forum.svg)](https://github.com/Nagaraj-06/Dicuss-Forum/commits/main)
[![Issues](https://img.shields.io/github/issues/Nagaraj-06/Dicuss-Forum.svg)](https://github.com/Nagaraj-06/Dicuss-Forum/issues)
[![PRs](https://img.shields.io/github/issues-pr/Nagaraj-06/Dicuss-Forum.svg)](https://github.com/Nagaraj-06/Dicuss-Forum/pulls)

<br/>

<p>
  <img src="https://img.shields.io/badge/Architecture-React%20SPA%20%2B%20Express-7C3AED?style=for-the-badge&logo=react&logoColor=white" />
  <img src="https://img.shields.io/badge/Database-MySQL-00758F?style=for-the-badge&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Auth-JWT%20%2B%20Google%20OAuth-22c55e?style=for-the-badge&logo=google&logoColor=white" />
</p>

<br/>

*A structured learning forum where students ask doubts, share answers, and collaborate across languages, levels, and topics.*

[🚀 **Live Demo**](https://project-omega-lime-69.vercel.app/)

</div>

<hr/>

## ⏩ Quick Links

- [📦 What is Included](#-what-is-included)
- [🔥 Key Features](#-key-features)
- [🛠️ Tech Stack](#️-tech-stack)
- [📐 Architecture Overview](#-architecture-overview)
- [⚙️ Setup & Installation](#️-setup--installation)
- [📂 Folder Structure](#-folder-structure)
- [🔮 Roadmap](#-roadmap)

<hr/>

## 📦 What is Included

**EduSphere** is a full-stack discussion forum focused on course-based learning.

- **🔐 Authentication Layer** - Email/session flow with JWT cookie handling and Google OAuth (`passport-google-oauth2`).
- **🧠 Forum Taxonomy** - Language -> Level -> Discussion hierarchy for organized discovery.
- **💬 Discussion Engine** - Create and edit posts, replies, and sub-replies with optional image uploads.
- **⭐ Interaction System** - Likes, saved posts/replies, views, and recent activity feeds.
- **👤 Profile Module** - User profile data, created topics, replies, favorites, and activity summaries.

---

## 🔥 Key Features

- **Course-oriented discussions** with language and level segmentation.
- **JWT-protected APIs** using cookie or bearer token validation.
- **Google sign-in flow** with Passport-based OAuth callback handling.
- **Nested conversations** via main replies and sub-replies.
- **Media support** for discussion/reply image uploads using Multer.
- **Engagement tooling** including likes, saved items, and view tracking.
- **Forum analytics** endpoints for total languages, levels, and posts.

---

## 🛠️ Tech Stack

### ⚙️ Core Technologies
| Frontend | Backend | Database | Authentication | Styling/UI |
| :---: | :---: | :---: | :---: | :---: |
| React 18, React Router | Node.js, Express | MySQL (`mysql2`) | JWT, Cookies, Google OAuth | CSS, MUI, BlueprintJS |

### 🛠️ Supporting Libraries
| Networking | Security | Uploads | Utilities |
| :---: | :---: | :---: | :---: |
| Axios | bcrypt, cookie-parser, express-session | Multer | dotenv, body-parser |

---

## 📐 Architecture Overview

```mermaid
graph TD
    subgraph Frontend["Frontend (React SPA)"]
        UI["Pages + Components"]
        CTX["User Context"]
        API["Axios Client (withCredentials)"]
        UI --> CTX
        UI --> API
    end

    subgraph Backend["Backend (Express API)"]
        MW["JWT Middleware"]
        AUTH["Auth + Google OAuth"]
        FORUM["Languages / Levels / Posts"]
        REPLY["Replies / Subreplies"]
        META["Likes / Saves / Views / Profile"]
    end

    subgraph Data["Persistence + Storage"]
        DB[("MySQL")]
        IMG["public/images (uploads)"]
    end

    API --> AUTH
    API --> MW
    MW --> FORUM
    MW --> REPLY
    MW --> META
    AUTH --> DB
    FORUM --> DB
    REPLY --> DB
    META --> DB
    FORUM --> IMG
    REPLY --> IMG
```

---

## ⚙️ Setup & Installation

### Prerequisites
- Node.js `v18+`
- MySQL Server
- npm

### 1. Clone

```bash
git clone https://github.com/Nagaraj-06/Dicuss-Forum.git
cd Dicuss-Forum
```

### 2. Backend Setup

```bash
cd backend
npm install
```

Create `backend/.env` (see env section below), then run:

```bash
npm start
```

Backend runs on: `http://localhost:2000`

### 3. Frontend Setup

```bash
cd ../client
npm install
npm start
```

Frontend runs on: `http://localhost:4000`

---

## 📂 Folder Structure

```text
Dicuss-Forum/
├── backend/
│   ├── app.js
│   ├── passport-setup.js
│   ├── public/images/
│   └── src/
│       ├── config/
│       ├── middleware/
│       ├── Controllers/
│       └── Routes/
├── client/
│   ├── public/
│   └── src/
│       ├── Pages/
│       ├── Account_Pages/
│       ├── componants/
│       ├── api/
│       └── assets/
└── README.md
---

## 🔮 Roadmap

- [ ] Add test coverage for API routes and critical UI flows
- [ ] Add pagination and filters for large discussions
- [ ] Add role-based moderation (admin/moderator)
- [ ] Improve notification system for reply and mention events
- [ ] Add Docker compose for one-command local setup

---

<div align="center">

**Star this repo if it helped you.**

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-Nagaraj--06-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Nagaraj-06)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Nagaraj%20R-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nagaraj-r-4265272b8/)

<br/>

*Built by Nagaraj R*

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=120&section=footer" />

</div>
