# Marketing Analytics Budget Optimization Agent

## Overview
This project implements a minimal agent that allocates daily advertising budget across channels (Google, Facebook, TikTok) to maximize conversions using simple reasoning and a lightweight learning loop.

The agent reads campaign performance data, evaluates channel efficiency, and recommends budget shifts while applying guardrails to ensure stable and realistic changes.

A simple chat interface allows users to ask questions about performance and optimization decisions.

---

## Features
- Reads campaign data from a CSV
- Calculates performance metrics (CTR, CVR, CPA)
- Allocates budget based on channel performance
- Applies guardrails (minimum allocation, capped changes)
- Implements a lightweight learning loop (updates channel scores over time)
- Compares baseline vs optimized allocation
- Provides natural language explanations

---

## How to Run

### Option 1: Local (HTML)
1. Download `index.html`
2. Open in your browser
3. Ask a question in the chat

### Option 2: Live Demo
Open the hosted version:
