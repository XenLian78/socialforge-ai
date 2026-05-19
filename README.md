# SocialForge AI 🚀

> AI-powered social media content generator — δώσε ένα θέμα, πάρε έτοιμο content για Facebook, Instagram, LinkedIn & TikTok.

[![Live Demo](https://img.shields.io/badge/Live-Demo-4f8ef7?style=flat-square)](https://xenlian78.github.io/socialforge-ai)
[![n8n](https://img.shields.io/badge/Built%20with-n8n-EA4B71?style=flat-square)](https://n8n.io)
[![Groq](https://img.shields.io/badge/LLM-Groq%20%2F%20Llama-00A67E?style=flat-square)](https://groq.com)

---

## Τι κάνει

Ο χρήστης δίνει ένα προϊόν ή θέμα (προαιρετικά και URL σελίδας) και το σύστημα παράγει αυτόματα:

- **Facebook** — 2 παραλλαγές A/B (Hook vs Benefit)
- **Instagram** — Caption με save trigger και SEO keywords
- **LinkedIn** — Thought leadership post με first comment strategy
- **TikTok** — Script outline με retention hook και text overlays
- **Visual** — AI-generated εικόνα μέσω Pollinations.ai

Τα αποτελέσματα εμφανίζονται στο UI **και** αποστέλλονται αυτόματα σε email της επιλογής σου.

---

## Αρχιτεκτονική

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

---

## Tech Stack

| Layer | Tool | Γιατί |
|---|---|---|
| Automation | n8n (self-hosted) | Visual workflow builder, open-source |
| LLM | Groq + Llama 4 Scout | Δωρεάν, γρήγορο, αξιόπιστο tool calling |
| Web Search | SerpApi | Real-time Google results για research |
| Image Gen | Pollinations.ai | Δωρεάν AI image generation API |
| Frontend | Vanilla HTML/CSS/JS | Zero dependencies, GitHub Pages ready |
| Email | Gmail API (OAuth2) | Native n8n integration |

---

## Features

- ✅ Multi-platform content (Facebook, Instagram, LinkedIn, TikTok)
- ✅ A/B testing copywriting για Facebook
- ✅ Real-time web research για κάθε προϊόν
- ✅ Product URL scraping για ακριβές περιεχόμενο
- ✅ Email delivery σε οποιοδήποτε inbox
- ✅ Copy buttons για κάθε section
- ✅ Demo mode για portfolio viewers
- ✅ Collapsible platform cards

---

## Πώς λειτουργεί locally

**Προαπαιτούμενα:**
- n8n εγκατεστημένο και τρέχει στο `localhost:5678`
- Groq API key (δωρεάν στο [console.groq.com](https://console.groq.com))
- SerpApi key (δωρεάν tier)
- Gmail OAuth2 credentials

**Βήματα:**
1. Import το n8n workflow
2. Ρύθμισε τα credentials (Groq, SerpApi, Gmail)
3. Activate το workflow
4. Άνοιξε το `index.html` ή το GitHub Pages URL

---

## Roadmap

- [ ] Καλύτερη εικόνα με Fal.ai (όταν μπει budget)
- [ ] Αφαίρεση SVG section
- [ ] Βελτίωση content quality — full marketing structure
- [ ] Carousel post generator για Instagram
- [ ] Scheduling integration (Buffer / Later API)

---

## Author

**Xenofon Lianos** — Strategic Marketing Specialist → Automation Architect

Χτίστηκε ως μέρος του automation portfolio μου που συνδυάζει marketing thinking με technical execution.

[![GitHub](https://img.shields.io/badge/GitHub-XenLian78-181717?style=flat-square&logo=github)](https://github.com/XenLian78)
[![Portfolio](https://img.shields.io/badge/Portfolio-xenlian78.github.io-4f8ef7?style=flat-square)](https://xenlian78.github.io)
