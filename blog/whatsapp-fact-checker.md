---
layout: default
title: Building a WhatsApp Fact Checker with LLM
date: 2025-06-26
---

[← Back to Blog](/blog)

# Building a WhatsApp Fact Checker with LLM

*June 26, 2024*

Misinformation is a growing problem, especially in local communities where WhatsApp is the primary communication channel. In this post, I'll walk you through how I built an AI-powered fact-checking bot that combats false information in real-time.

## The Problem

In many Indian communities, WhatsApp groups are the primary source of news and information. Unfortunately, this also makes them a breeding ground for misinformation...

## The Solution

I decided to build a bot that could automatically fact-check claims...

[Continue with your content...]

## Technical Implementation
```python
# Example code snippet
def process_message(message):
    # Claude analyzes the claim
    analysis = claude_api.analyze(message)
    
    # Perplexity fact-checks
    facts = perplexity_api.search(analysis.claim)
    
    return generate_response(facts)
```

## Lessons Learned

1. **Rate limiting is crucial** - WhatsApp has strict limits
2. **Context matters** - Short messages need smart interpretation
3. **Testing is essential** - Unit tests caught many edge cases

## Results

The bot has successfully...

---

*Questions? Connect with me on [LinkedIn](https://linkedin.com/in/akshen)*