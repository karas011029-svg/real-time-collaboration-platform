# Revo is an open-source real-time collaboration platform.

---
<div align="center">

![Revo Banner](./public/revo-showcase.png)

# 🚀 Revo

### Connect. Collaborate. Create.

A modern real-time collaboration platform for teams. Chat instantly, share files, and work together seamlessly — all in one place.

[![Next.js](https://img.shields.io/badge/Next.js-16.0.10-black?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4.0-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Prisma](https://img.shields.io/badge/Prisma-7.0-2D3748?style=for-the-badge&logo=prisma&logoColor=white)](https://www.prisma.io/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE)


</div>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Environment Variables](#-environment-variables)
- [Database Setup](#-database-setup)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

---

## 🌟 Overview

**Revo** is a next-generation team collaboration platform designed for modern remote and hybrid teams. Built with cutting-edge technologies, it offers real-time messaging, threaded discussions, file sharing, and AI-powered features — all wrapped in a beautiful, responsive interface.

### Why Revo?

- ⚡ **Blazing Fast** — Built on Next.js 16 with React 19 for optimal performance
- 🔒 **Secure** — Enterprise-grade security with Arcjet protection and Kinde authentication
- 🤖 **AI-Powered** — Integrated AI assistance powered by OpenRouter
- 🌐 **Real-time** — WebSocket-powered instant messaging via PartyKit
- 📱 **Responsive** — Beautiful UI that works seamlessly across all devices

---

## ✨ Features

<table>
  <tr>
    <td align="center" width="33%">
      <br><strong>Channel Management</strong>
      <br><sub>Create organized spaces for teams, projects, or topics</sub>
    </td>
    <td align="center" width="33%">
      <br><strong>Team Collaboration</strong>
      <br><sub>Invite teammates and collaborate in real-time</sub>
    </td>
    <td align="center" width="33%">
      <br><strong>Instant Messaging</strong>
      <br><sub>Send messages, share ideas, and stay connected</sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <br><strong>Threaded Discussions</strong>
      <br><sub>Keep detailed conversations organized with threads</sub>
    </td>
    <td align="center" width="33%">
      <br><strong>Reactions & Engagement</strong>
      <br><sub>React with emojis to quickly respond and engage</sub>
    </td>
    <td align="center" width="33%">
      <br><strong>AI Assistant</strong>
      <br><sub>Get help with writing, summarizing, and more</sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <br><strong>File Sharing</strong>
      <br><sub>Upload and share files seamlessly with UploadThing</sub>
    </td>
    <td align="center" width="33%">
      <br><strong>Rich Text Editor</strong>
      <br><sub>Format messages with TipTap's powerful editor</sub>
    </td>
    <td align="center" width="33%">
      <br><strong>Dark/Light Mode</strong>
      <br><sub>Beautiful themes that adapt to your preference</sub>
    </td>
  </tr>
</table>

---

## 🛠 Tech Stack

### Core Framework
| Technology | Purpose | Version |
|------------|---------|---------|
| [Next.js](https://nextjs.org/) | React Framework | 16.0.10 |
| [React](https://react.dev/) | UI Library | 19.2.0 |
| [TypeScript](https://www.typescriptlang.org/) | Type Safety | 5.x |

### Styling & UI
| Technology | Purpose |
|------------|---------|
| [Tailwind CSS](https://tailwindcss.com/) | Utility-first CSS |
| [shadcn/ui](https://ui.shadcn.com/) | Component Library |
| [Radix UI](https://www.radix-ui.com/) | Headless Components |
| [Framer Motion](https://www.framer.com/motion/) | Animations |
| [Lucide](https://lucide.dev/) | Icons |

### Backend & Database
| Technology | Purpose |
|------------|---------|
| [Prisma](https://www.prisma.io/) | ORM |
| [PostgreSQL](https://www.postgresql.org/) | Database |
| [Neon](https://neon.tech/) | Serverless Postgres |
| [oRPC](https://orpc.dev/) | Type-safe API Layer |

### Real-time & Infrastructure
| Technology | Purpose |
|------------|---------|
| [PartyKit](https://www.partykit.io/) | Real-time WebSockets |
| [Cloudflare Workers](https://workers.cloudflare.com/) | Edge Runtime |
| [Wrangler](https://developers.cloudflare.com/workers/wrangler/) | CF CLI |

### Authentication & Security
| Technology | Purpose |
|------------|---------|
| [Kinde](https://kinde.com/) | Authentication |
| [Arcjet](https://arcjet.com/) | Security & Rate Limiting |

### AI & Content
| Technology | Purpose |
|------------|---------|
| [AI SDK](https://sdk.vercel.ai/) | AI Integration |
| [OpenRouter](https://openrouter.ai/) | AI Model Gateway |
| [TipTap](https://tiptap.dev/) | Rich Text Editor |
| [UploadThing](https://uploadthing.com/) | File Uploads |

### Developer Experience
| Technology | Purpose |
|------------|---------|
| [TanStack Query](https://tanstack.com/query) | Data Fetching |
| [Zod](https://zod.dev/) | Validation |
| [React Hook Form](https://react-hook-form.com/) | Form Management |
| [Sonner](https://sonner.emilkowal.ski/) | Toast Notifications |

---

## 🏗 Architecture

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                                   CLIENT                                    │
│  ┌─────────────────────────────────────────────────────────────────────┐    │
│  │                         Next.js 16 App Router                       │    │
│  │  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌────────────┐  │    │
│  │  │   React 19  │  │  TanStack   │  │   shadcn/ui │  │   Motion   │  │    │
│  │  │ Components  │  │    Query    │  │  + Radix UI │  │ Animations │  │    │
│  │  └─────────────┘  └─────────────┘  └─────────────┘  └────────────┘  │    │
│  └─────────────────────────────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────────────────────────────┘
                                      │
                    ┌─────────────────┼─────────────────┐
                    ▼                 ▼                 ▼
        ┌───────────────────┐ ┌───────────────┐ ┌───────────────────┐
        │    oRPC Client    │ │  PartySocket  │ │    UploadThing    │
        │   (Type-safe)     │ │  (Real-time)  │ │   (File Upload)   │
        └─────────┬─────────┘ └───────┬───────┘ └─────────┬─────────┘
                  │                   │                   │
┌─────────────────┼───────────────────┼───────────────────┼─────────────────┐
│                 │                   │                   │      EDGE       │
│                 ▼                   ▼                   ▼                 │
│  ┌──────────────────────────────────────────────────────────────────┐     │
│  │                        Cloudflare Workers                        │     │
│  │  ┌─────────────────┐  ┌─────────────────┐  ┌──────────────────┐  │     │
│  │  │   PartyServer   │  │     Wrangler    │  │   Edge Runtime   │  │     │ 
│  │  │   (WebSocket)   │  │   (Deployment)  │  │   (Low Latency)  │  │     │
│  │  └─────────────────┘  └─────────────────┘  └──────────────────┘  │     │
│  └──────────────────────────────────────────────────────────────────┘     │
└──────────────────────────────────────────────────────────────────────────-┘
                                      │
┌─────────────────────────────────────┼────────────────────────────────────┐
│                                     │              SERVER                │
│  ┌──────────────────────────────────┼───────────────────────────────┐    │
│  │                         Next.js API Layer                        │    │
│  │  ┌─────────────────┐  ┌─────────────────┐  ┌──────────────────┐  │    │
│  │  │   oRPC Server   │  │     Arcjet      │  │   Kinde Auth     │  │    │
│  │  │  (Procedures)   │  │   (Security)    │  │ (Authentication) │  │    │
│  │  └────────┬────────┘  └─────────────────┘  └──────────────────┘  │    │
│  └───────────┼──────────────────────────────────────────────────────┘    │
│              │                                                           │
│              ▼                                                           │
│  ┌──────────────────────────────────────────────────────────────────┐    │
│  │                         Prisma ORM                               │    │
│  │  ┌─────────────────┐  ┌─────────────────┐  ┌──────────────────┐  │    │
│  │  │     Models      │  │    Migrations   │  │  Query Builder   │  │    │
│  │  └────────┬────────┘  └─────────────────┘  └──────────────────┘  │    │
│  └───────────┼──────────────────────────────────────────────────────┘    │
│              │                                                           │
│              ▼                                                           │
│  ┌──────────────────────────────────────────────────────────────────┐    │
│  │                      Neon PostgreSQL                             │    │
│  │  ┌─────────────────┐  ┌─────────────────┐  ┌──────────────────┐  │    │
│  │  │   Serverless    │  │    Branching    │  │   Auto-scaling   │  │    │
│  │  └─────────────────┘  └─────────────────┘  └──────────────────┘  │    │
│  └──────────────────────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────────────────────┘
                                      │
┌─────────────────────────────────────┼────────────────────────────────────┐
│                                     │           AI SERVICES              │
│  ┌──────────────────────────────────┼───────────────────────────────┐    │
│  │  ┌─────────────────┐  ┌─────────────────┐  ┌──────────────────┐  │    │
│  │  │     AI SDK      │  │   OpenRouter    │  │   LLM Models     │  │    │
│  │  │   (Vercel)      │  │    (Gateway)    │  │ (GPT, Claude...) │  │    │
│  │  └─────────────────┘  └─────────────────┘  └──────────────────┘  │    │
│  └──────────────────────────────────────────────────────────────────┘    │
└──────────────────────────────────────────────────────────────────────────┘
```

### Data Flow

```
User Action → React Component → TanStack Query → oRPC Client
                                                      │
                                                      ▼
                                              oRPC Server (API)
                                                      │
                    ┌─────────────────────────────────┼─────────────────────────────────┐
                    │                                 │                                 │
                    ▼                                 ▼                                 ▼
            Arcjet (Security)                  Kinde (Auth)                    AI SDK (OpenRouter)
                    │                                 │                                 │
                    └─────────────────────────────────┼─────────────────────────────────┘
                                                      │
                                                      ▼
                                              Prisma ORM
                                                      │
                                                      ▼
                                              Neon PostgreSQL
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed:

- **Node.js** 20.x or higher
- **pnpm** (recommended) or npm/yarn
- **Git**

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/karas011029-svg/real-time-collaboration-platform.git
cd revo
```

2. **Install dependencies**

```bash
pnpm install
# or
npm install
```

3. **Set up environment variables**

```bash
cp .env.example .env.local
```

4. **Set up the database**

```bash
pnpm prisma generate
pnpm prisma db push
```

5. **Run the development server**

```bash
pnpm dev
```

6. **Open your browser**

Navigate to [http://localhost:3000](http://localhost:3000)

---

## 📁 Project Structure

```
revo/
├── app/                          # Next.js App Router
│   ├── (auth)/                   # Authentication routes
│   ├── (main)/                   # Main application routes
│   ├── api/                      # API routes
│   │   ├── orpc/                 # oRPC handlers
│   │   ├── uploadthing/          # File upload handlers
│   │   └── ai/                   # AI endpoints
│   ├── layout.tsx                # Root layout
│   └── page.tsx                  # Landing page
│
├── components/                   # React components
│   ├── ui/                       # shadcn/ui components
│   ├── auth/                     # Authentication components
│   ├── chat/                     # Chat components
│   ├── channels/                 # Channel components
│   ├── editor/                   # TipTap editor components
│   └── theme/                    # Theme provider
│
├── lib/                          # Utility functions
│   ├── orpc/                     # oRPC configuration
│   │   ├── client.ts             # Client setup
│   │   ├── server.ts             # Server setup
│   │   └── router.ts             # API router
│   ├── prisma.ts                 # Prisma client
│   ├── auth.ts                   # Kinde helpers
│   ├── ai.ts                     # AI SDK setup
│   └── utils.ts                  # Utility functions
│
├── server/                       # Server-side code
│   ├── procedures/               # oRPC procedures
│   └── party/                    # PartyKit server
│
├── prisma/                       # Database
│   └── schema.prisma             # Database schema
│
├── public/                       # Static assets
│   ├── revo-showcase.png         # OG image
│   └── favicon.ico               # Favicon
│
├── types/                        # TypeScript types
│
├── .env.example                  # Environment template
├── next.config.ts                # Next.js config
├── tailwind.config.ts            # Tailwind config
├── tsconfig.json                 # TypeScript config
├── wrangler.toml                 # Cloudflare config
└── package.json                  # Dependencies
```

---

## 🔐 Environment Variables

Create a `.env.local` file in the root directory:

```env
# ===========================================
# DATABASE
# ===========================================
DATABASE_URL="postgresql://user:password@host:5432/revo?sslmode=require"

# ===========================================
# KINDE AUTHENTICATION
# ===========================================
KINDE_CLIENT_ID="your_kinde_client_id"
KINDE_CLIENT_SECRET="your_kinde_client_secret"
KINDE_ISSUER_URL="https://your-domain.kinde.com"
KINDE_SITE_URL="http://localhost:3000"
KINDE_POST_LOGOUT_REDIRECT_URL="http://localhost:3000"
KINDE_POST_LOGIN_REDIRECT_URL="http://localhost:3000/workspace"
KINDE_DOMAIN=https://your-domain.kinde.com
KINDE_MANAGEMENT_CLIENT_ID="your_kinde_management_id"
KINDE_MANAGEMENT_CLIENT_SECRET="your_kinde_management_secret"

# ===========================================
# UPLOADTHING
# ===========================================
UPLOADTHING_TOKEN="your_uploadthing_token"

# ===========================================
# AI / OPENROUTER
# ===========================================
OPENROUTER_LLM_KEY="your_openrouter_api_key"

# ===========================================
# ARCJET (Security)
# ===========================================
ARCJET_KEY="your_arcjet_key"

# ===========================================
# APP
# ===========================================
NEXT_PUBLIC_APP_URL="http://localhost:3000"
```

---

## 🗄 Database Setup

### Using Neon (Recommended)

1. Create a free account at [Neon](https://neon.tech)
2. Create a new project
3. Copy the connection string
4. Add it to your `.env.local` file

### Run Migrations

```bash
# Generate Prisma client
pnpm prisma generate

# Push schema to database
pnpm prisma db push

# Open Prisma Studio (optional)
pnpm prisma studio
```

---

## 🚀 Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Import your repository on [Vercel](https://vercel.com)
3. Add environment variables
4. Deploy!

```bash
# Or use Vercel CLI
npm i -g vercel
vercel
```

### Cloudflare Workers (PartyKit)

```bash
# Login to Cloudflare
pnpm dlx wrangler login

# Deploy wrangler server
pnpm dlx wrangler deploy
```

---

## 🧪 Scripts

| Command | Description |
|---------|-------------|
| `pnpm dev` | Start development server |
| `pnpm build` | Build for production |
| `pnpm start` | Start production server |
| `pnpm lint` | Run ESLint |
| `pnpm prisma studio` | Open Prisma Studio |
| `pnpm prisma generate` | Generate Prisma client |
| `pnpm prisma db push` | Push schema to database |

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add amazing feature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open a Pull Request**

### Code Style

- Follow the existing code style
- Use TypeScript strictly
- Write meaningful commit messages
- Add comments for complex logic

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

<div align="center">

**Karas**


</div>

---

<div align="center">

### ⭐ Star this repo if you find it useful!

Made with ❤️ and ☕

</div>


### `LICENSE` (MIT)

```
MIT License

Copyright (c) 2024 Karas

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
