---
title: "CraftList AI: Why Open Innovation Powers My 100% Local E-Commerce Listing Studio with Gemma 2"
published: false
tags: devchallenge, hf26challenge, gemma, opensource
---

*This is a submission for the [Hacktoberfest Open-Source AI Challenge Week 2: Side Hustle](https://dev.to/challenges/hacktoberfest-week2-2026-10-12)*

## What I Built

I built **CraftList AI** — a privacy-first, zero-cloud e-commerce studio and profit margin engine designed for independent artisans, vintage thrifters, and handmade makers selling on Etsy, eBay, and Shopify.

### Who Would Pay For It & Why?
Solo makers and creative side-hustlers love crafting their products, but they universally hate writing listings. For every handmade mug, leather wallet, or carved wooden utensil, a seller must spend 45–60 minutes agonizing over:
1. **Algorithmic Titles & Descriptions:** Cramming high-volume search phrases into 140 characters without sounding robotic.
2. **The 13-Tag Etsy Matrix:** Generating exactly 13 unique tags under Etsy's strict rule of **20 characters or fewer** per tag.
3. **Pricing & Margin Anxiety:** Underpricing their labor or forgetting platform take-rates (6.5% transaction + payment processing + listing fees), accidentally working for less than minimum wage.
4. **Multi-Channel Social Promotion:** Writing Instagram captions, Pinterest SEO pins, and TikTok hooks.

Existing commercial listing generators charge $30–$50/month on subscription, meter tokens aggressively, and upload unreleased product designs to proprietary cloud servers. **CraftList AI** runs **100% locally on the seller's computer with Google Gemma 2**, costing $0.00 to run and guaranteeing complete data sovereignty.

---

## Demo

- **Live Application:** [http://localhost:5173](http://localhost:5173) (Vite + React)
- **Features Included:**
  - One-click sample presets (Hand-Carved Walnut Knife, Speckled Ceramic Mug, Horween Leather Wallet, Botanical Soy Candle).
  - Multi-marketplace selector (Etsy, eBay, Shopify, Amazon Handmade).
  - Built-in Side-Hustle Profit Calculator (Materials + Labor Hours × Rate + Marketplace Fees = Suggested Retail Price & Margin %).
  - Real-time Tag Auditor (13 tags, character count counter, duplicate detection).
  - Social Commerce Launch suite (Instagram, Pinterest, TikTok ASMR scripts).
  - Bulk CSV and JSON export for instant store importing.

---

## Code

The code is open-source and structured with a modern React + Vite architecture:
- GitHub Repository: [https://github.com/KavyaSaraswat23/Hactober_week3](https://github.com/KavyaSaraswat23/Hactober_week3)
- Tech Stack: React 19, Vite, Lucide Icons, Canvas-Confetti, Local Ollama / Gemma 2 API integration.

---

## How I Built It

CraftList AI is architected around **open-weight models and local inference**:

1. **Model of Choice: Google Gemma 2 (2B / 9B)**
   - Gemma 2 was chosen for its remarkable instruction-following capabilities, low memory footprint, and rapid generation speed on standard consumer laptops.
   - The 2B variant (`gemma2:2b`) runs blazingly fast even on CPU with zero dedicated GPU requirements, making it universally accessible to any non-technical maker.
2. **Turn-Token Prompt Formatting:**
   - We utilize Gemma's native turn structure:
   ```text
   <start_of_turn>user
   You are CraftList AI, an expert e-commerce listing optimizer.
   [CONSTRAINTS]
   - Strictly 13 tags, each <= 20 chars.
   - 140-char title limit for Etsy.
   - Profit Margin: 68%
   <end_of_turn>
   <start_of_turn>model
   ```
3. **Dual-Mode Inference Resilience:**
   - The app natively probes `http://localhost:11434` for a live Ollama daemon running Gemma 2.
   - If Ollama is offline or the user is on an unsupported device, a deterministic local client engine provides instant, high-quality listings with zero downtime or setup friction.

---

## Why Does Open Innovation Matter?

Open-source AI isn't just an alternative to closed APIs like GPT-4 or Claude—for a side-hustle business, **it is the only architecture that makes economic and operational sense**:

1. **Zero Marginal COGS ($0 vs $40/mo):**
   A small maker selling ten $30 items a month cannot afford a $40/month software subscription. With open weights, their AI runs on the hardware they already own. Zero API keys, zero surprise credit card charges.
2. **Protection of Artisan Trade Secrets:**
   Makers invent secret wood finishing mixtures, ceramic glaze recipes, and proprietary silhouettes months before public launch. Sending raw sketches and formulas to a closed cloud API puts proprietary IP at risk of model retraining. Local Gemma 2 inference guarantees complete data privacy.
3. **Rigid Rule Compliance Without Drift:**
   Closed APIs update unpredictably and frequently ignore strict constraints like Etsy's "maximum 20 characters per tag." Open-weight models can be evaluated, controlled, and temperature-locked for deterministic compliance.
4. **Complete Offline Autonomy:**
   Artisans source materials at flea markets, work in barn studios, and sell at craft fairs where cell service is non-existent. CraftList AI works 100% offline on laptop battery power.

---

## 🌐 Community Wisdom

Before building CraftList AI, we researched how fellow developers tackled local e-commerce and open-weight model integration on DEV:

- In [ShelfScribe: Local AI Listing Writer for Etsy Sellers](https://dev.to/yellowvoid/shelfscribe-local-ai-listing-writer-for-etsy-sellers-open-weight-ai-side-hustle-1hc5) by @yellowvoid, the author demonstrated how small open-weight models easily outperform generic assistants when given tight domain constraints.
- In [Ollama Cheat Sheet: Local LLMs, Models, API & Integration (2026)](https://dev.to/cooldashing24/ollama-cheat-sheet-local-llms-models-api-integration-2026-5a0f) by @cooldashing24, community discussions highlighted the importance of structuring prompt turn-tokens specifically for Gemma 2 to prevent token hallucination and ensure strict JSON schema outputs.

---

## My Agent Session

This project was built and debugged pair-programming with Antigravity and DevRelay:

`{% agent_session b07531a1-e075-41f2-bb93-ce0b43b1ab87 %}`

---

## My First User

I showed CraftList AI to my friend Maya, an independent ceramist who sells speckled stoneware mugs and planter pots at weekend pop-up markets. 

- **Her Reaction:** *"Wait, I don't have to think of 13 tags myself? And it counted the characters so Etsy doesn't reject them in red text?!"*
- **The Test:** We plugged in her 14 oz speckled mug, material cost ($4.80), and labor time (50 mins). The calculator instantly showed she was undercharging at $26 (barely 1.8x markup). CraftList AI recommended $38 based on her $26/hr target rate and platform fees, and generated an aesthetic story description highlighting her hand-pulled three-finger handle.
- **Did She Pay / Would She?** She offered to buy me lunch on the spot to keep the tool permanently on her MacBook, saying: *"I would easily pay a $29 one-time download fee for this because I refuse to pay another monthly subscription."*

---

## Prize Categories

- **Featured Category: Best Use of Gemma** (Built specifically for Google Gemma 2 2B/9B open weights running locally via Ollama with strict turn-token conditioning).
