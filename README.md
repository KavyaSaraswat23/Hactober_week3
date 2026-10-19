# CraftList AI 🪵✨
> **Local E-Commerce Studio & Listing Engine Powered by Open-Weight Google Gemma 2**  
> *Built for the Hacktoberfest Open-Source AI Challenge: Week 2 (Side Hustle)*  
> *Target Category: Featured Prize — Best Use of Gemma*

CraftList AI is a privacy-first, client-side listing optimizer and margin engine for Etsy, eBay, and Shopify artisans. It turns product materials, dimensions, and craft heritage notes into high-converting SEO listings, exactly 13 Etsy tags (&le; 20 characters), and social launch copy—running entirely offline with **Google Gemma 2**.

---

## 🚀 Key Features

- **Local Open-Weight AI Core:** Powered by Google's Gemma 2 (2B / 9B) running locally via Ollama with zero cloud API token costs.
- **Strict Marketplace Algorithmic Compliance:** Generates 140-char Etsy titles, 80-char eBay specs, and audits exactly 13 Etsy tags to ensure every tag is 20 characters or fewer with zero keyword duplicates.
- **Side Hustle Profit & Margin Calculator:** Computes exact material cost, labor hours, artisan hourly rate, and marketplace transaction fees to recommend optimal retail prices and net margins.
- **Multi-Platform Adaptation:** Instant switching between **Etsy**, **eBay**, **Shopify**, and **Amazon Handmade**.
- **Social Commerce Suite:** Auto-generates Instagram reel captions, Pinterest SEO pin descriptions, and 15-second viral TikTok ASMR hook scripts.
- **Bulk Export:** One-click CSV and JSON exports for direct import into store management tools.

---

## 🏗️ Architecture & Tech Stack

| Layer | Technology | Details |
| :--- | :--- | :--- |
| **Frontend Framework** | React 19 + Vite | Instant HMR, responsive split-screen studio layout |
| **Design System** | Custom Vanilla CSS | Dark obsidian aesthetic, glassmorphism, responsive grid |
| **Open-Weight AI** | Google Gemma 2 (2B / 9B) | Local inference via Ollama or built-in client engine |
| **Icons & Effects** | Lucide-React & Canvas-Confetti | Modern UI icons and celebratory visual feedback |
| **Data Formats** | JSON & CSV | RFC 4180 compliant CSV export for marketplace bulk uploads |

---

## 🛠️ Quick Start

### 1. Install & Run Web App
```bash
cd dev_week_2
npm install
npm run dev
```
Open [http://localhost:5173](http://localhost:5173) in your browser.

### 2. Connect Local Gemma 2 (via Ollama)
```bash
# Pull and run Gemma 2 2B locally
ollama run gemma2:2b
```
CraftList AI will auto-detect the local daemon at `http://localhost:11434`. If Ollama is not running, the built-in deterministic client engine runs smoothly out-of-the-box.

---

## 💡 Why Open Innovation Matters

1. **Zero Recurring SaaS Tolls ($0 vs $40/mo):** Solo crafters operate on tight margins. Closed AI listing tools charge monthly subscriptions; running Gemma 2 on a laptop has zero marginal cost.
2. **Absolute Trade Secret Privacy:** Artisans keep unreleased prototypes, secret wood finishes, glaze chemistry, and supplier details off third-party servers.
3. **Deterministic Constraint Adherence:** Gemma 2 turn tokens (`<start_of_turn>user ...`) enable tight structured JSON formatting that never violates strict marketplace character limits.
4. **100% Offline Portability:** Works at flea markets, craft fairs, and rural studios without an internet connection.
