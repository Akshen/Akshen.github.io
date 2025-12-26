---
layout: default
title: WhatsApp Fact Checker Bot
---

[← Back to Portfolio](/)

# WhatsApp Fact Checker Bot

![Project Status](https://img.shields.io/badge/Status-Live-success)
![Tech](https://img.shields.io/badge/Tech-Python-blue)
![AI](https://img.shields.io/badge/AI-Claude%20%7C%20Perplexity-orange)

## 🎯 Overview

AI-powered WhatsApp bot that detects and debunks misinformation in real-time using Claude and Perplexity APIs. Built to combat the spread of false information in local communities.

## 🔍 Problem Statement

Misinformation spreads rapidly through WhatsApp groups, especially in local communities where fact-checking resources are limited. This leads to:
- Distrust among community members
- Poor decision-making based on false information
- Social tensions and conflicts

## 💡 Solution

Built an automated fact-checking bot that:
1. Receives messages via WhatsApp Business API
2. Analyzes content using Claude for context understanding
3. Fact-checks claims using Perplexity's real-time search
4. Returns verified information with sources
5. Handles high-volume traffic through MAKE.com orchestration

## 🏗️ Architecture
```
WhatsApp Message → Webhook → MAKE.com → Claude API (Analysis) 
                                       ↓
                              Perplexity API (Fact-check)
                                       ↓
                              Response Processing → WhatsApp Reply
```

## 🛠️ Tech Stack

- **Backend:** Python 3.9+
- **APIs:** WhatsApp Business Cloud API, Claude API, Perplexity API
- **Automation:** MAKE.com (workflow orchestration)
- **Infrastructure:** Webhooks, REST APIs
- **Version Control:** Git with unit testing

## ✨ Key Features

- ⚡ **Real-time fact-checking** - Instant responses to user queries
- 🔄 **Queue management** - Handles high-volume traffic efficiently
- 🎯 **Context-aware** - Claude understands nuanced claims
- 📊 **Source verification** - Provides credible sources via Perplexity
- 🧪 **Tested & reliable** - Comprehensive unit test coverage

## 🎬 How It Works

1. **User sends message** to WhatsApp bot with a claim or question
2. **Webhook triggers** MAKE.com workflow
3. **Claude analyzes** the message for key claims and context
4. **Perplexity searches** for factual information and sources
5. **Response generated** with fact-check results and sources
6. **User receives** verified information within seconds

## 🚀 Impact

- Improved information quality in local communities
- Reduced spread of misinformation
- Increased trust among community members
- Scalable solution for fact-checking at scale

## 🧠 Challenges & Solutions

### Challenge 1: Rate Limiting
**Problem:** WhatsApp API has strict rate limits  
**Solution:** Implemented queue system with MAKE.com to batch process messages

### Challenge 2: Context Understanding
**Problem:** Short messages lack context  
**Solution:** Used Claude's advanced reasoning to infer context from minimal information

### Challenge 3: Source Reliability
**Problem:** Not all sources are trustworthy  
**Solution:** Perplexity API prioritizes authoritative sources in its search results

## 📈 Future Enhancements

- [ ] Multi-language support (Hindi, Marathi, etc.)
- [ ] Image fact-checking using vision models
- [ ] User feedback loop for accuracy improvement
- [ ] Analytics dashboard for tracking misinformation trends
- [ ] Integration with local news verification services

## 🔗 Links

- GitHub Repository (Coming Soon)
- Technical Documentation (Coming Soon)

---

**Built with ❤️ for safer online communities**