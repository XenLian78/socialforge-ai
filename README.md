# SocialForge AI 🚀

> AI-powered social media content generator — give a topic, get ready-made content for Facebook, Instagram, LinkedIn & TikTok.

[![Live Demo](https://img.shields.io/badge/Live-Demo-4f8ef7?style=flat-square)](https://xenlian78.github.io/socialforge-ai)
[![n8n](https://img.shields.io/badge/Built%20with-n8n-EA4B71?style=flat-square)](https://n8n.io)
[![Groq](https://img.shields.io/badge/LLM-Groq%20%2F%20Llama-00A67E?style=flat-square)](https://groq.com)

---

# What it does

The user provides a product or topic (optionally with a page URL) and the system automatically generates:

- **Facebook** — 2 A/B variations (Hook vs Benefit)
- **Instagram** — Caption with save trigger and SEO keywords
- **LinkedIn** — Thought leadership post with first comment strategy
- **TikTok** — Script outline with retention hook and text overlays
- **Visual** — AI-generated image via Pollinations.ai

Results are displayed in the UI **and** automatically sent to an email of your choice.

---

## Architecture

```
UI (HTML/CSS/JS)
│
│ HTTP POST (JSON)
▼
n8n Webhook Trigger
│
├─► HTTP Request      (fetch product page content)
├─► SerpApi           (Google Search για trends)
│
▼
Market Research Agent   (Groq / Llama 4 Scout)
│
▼
Copywrite & Image Agent (Groq / Llama 4 Scout)
│
▼
Code Node               (JavaScript — parse & structure output)
│
▼
Gmail Node              (αποστολή σε email της επιλογής)
│
▼
Respond to Webhook      (JSON response → UI)

```
---

## Tech Stack

| Layer | Tool | Why |
|---|---|---|
| Automation | n8n (self-hosted) | Visual workflow builder, open-source |
| LLM | Groq + Llama 4 Scout | Free, fast, reliable tool calling |
| Web Search | SerpApi | Real-time Google results for research |
| Image Gen | Pollinations.ai | Free AI image generation API |
| Frontend | Vanilla HTML/CSS/JS | Zero dependencies, GitHub Pages ready |
| Email | Gmail API (OAuth2) | Native n8n integration |

---

## Features

- ✅ Multi-platform content (Facebook, Instagram, LinkedIn, TikTok)
- ✅ A/B testing copywriting for Facebook
- ✅ Real-time web research for each product
- ✅ Product URL scraping for accurate content
- ✅ Email delivery to any inbox
- ✅ Copy buttons for each section
- ✅ Demo mode for portfolio viewers
- ✅ Collapsible platform cards

---

## How to run locally

**Prerequisites:**
- n8n installed and running at `localhost:5678`
- Groq API key (free at [console.groq.com](https://console.groq.com))
- SerpApi key (free tier)
- Gmail OAuth2 credentials

**Steps:**
1. Import the n8n workflow
2. Configure the credentials (Groq, SerpApi, Gmail)
3. Activate the workflow
4. Open `index.html` or the GitHub Pages URL

---

## Roadmap

- [ ] Better image generation with Fal.ai (when budget allows)
- [ ] Remove SVG section
- [ ] Improve content quality — full marketing structure
- [ ] Carousel post generator for Instagram
- [ ] Scheduling integration (Buffer / Later API)

---

## Author

**Xenofon Lianos** — Marketing Professional & AI-Assisted Builder

Built as part of my automation portfolio, combining marketing thinking with technical execution.

[![GitHub](https://img.shields.io/badge/GitHub-XenLian78-181717?style=flat-square&logo=github)](https://github.com/XenLian78)
[![Portfolio](https://img.shields.io/badge/Portfolio-xenlian78.github.io-4f8ef7?style=flat-square)](https://xenlian78.github.io)
