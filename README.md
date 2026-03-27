# 🏛️ Nyaya Setu  
AI-assisted Legal Triage & Safety Support Platform

---

## 📌 Overview

Nyaya Setu is a civic-tech platform designed to improve early-stage dispute handling and access to justice in India.

It enables:
- Structured submission of disputes from both parties  
- AI-assisted neutral summaries and inconsistency detection  
- Faster case triage for reviewers/judges  
- Safety-first legal guidance for users in distress  

Nyaya Setu does not replace judges or lawyers. It helps reduce friction in the initial stages of legal processes and supports faster human decision-making.

---

## 🚨 Problem Statement

India’s legal system faces significant delays due to an overwhelming number of pending cases.

- ~5.5 crore pending cases across courts  
- >92,000 cases pending in the Supreme Court  

Key challenges:
- Lack of structured case intake  
- Time-consuming manual comparison of statements  
- Poor accessibility for common citizens  
- No immediate guidance for users in distress  

---

## 🔍 Existing Solutions

Current solutions are fragmented:

- Legal information websites → Static, not actionable  
- Lawyer platforms → Expensive and not accessible to all  
- Court databases → Complex and not user-friendly  
- Generic chatbots → Lack legal structure and safety focus  

---

## 🎯 Target Users

### Primary Users
- Citizens involved in disputes  
- Individuals facing harassment or threats  
- People needing help organizing facts and evidence  

### Secondary Users
- Legal aid volunteers  
- NGOs  
- Mediators and early-stage reviewers  

### Institutional Users
- Court support systems  
- Legal aid desks  

---

## ⚠️ Gap Analysis

Current systems fail because they are:
- Passive (information only, no action)
- One-sided (no comparison of both parties)
- Complex (not citizen-friendly)
- Unsafe (no distress-first support)

---

## 💡 Proposed Solution

Nyaya Setu introduces two core modules:

### 1. Case Triage Module
- Party A files a complaint  
- Party B submits a response  
- AI generates:
  - Neutral summaries  
  - Inconsistency detection  
  - Procedural recommendation  
  - Confidence score  

- Reviewer sees structured case in a dashboard  

---

### 2. Safety Guidance Module
A chat-based assistant that:
- Prioritizes user safety  
- Guides evidence preservation  
- Explains legal rights in simple language  
- Suggests next steps or escalation  

---

## ✨ Unique Value Proposition

Nyaya Setu is not a decision-maker — it is a decision accelerator.

It:
- Helps citizens express their case clearly  
- Reduces manual effort for reviewers  
- Provides calm, actionable guidance in distress  
- Bridges the gap between citizens and legal systems  

### One-line UVP:
"Nyaya Setu helps people file, compare, and triage disputes faster while keeping human judgment at the center."

---

## 🏗️ Technical Architecture

### Tech Stack

- Frontend: Next.js + TypeScript + Tailwind CSS  
- Backend: Supabase (PostgreSQL, Storage)  
- AI: Gemini API (Free Tier)  
- Deployment: Vercel (Frontend), Supabase (Backend)  
- Future: Indian Kanoon API, WhatsApp integration  

---

## 📊 Architecture Diagram

```mermaid
flowchart TD
    A[User / Citizen] --> B[Next.js Frontend]

    B --> C[Case Filing - Party A]
    B --> D[Case Response - Party B]
    B --> E[Safety Chat]
    B --> F[Judge Dashboard]

    C --> G[Supabase Database]
    D --> G

    E --> H[Gemini API]

    G --> I[AI Analysis Service]
    I --> H
    H --> G

    G --> F

    F --> J[Judge Decision]
