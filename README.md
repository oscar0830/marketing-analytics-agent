Marketing Analytics Budget Optimization Agent
Overview

This project implements a minimal agent that allocates daily advertising budget across channels (Google, Facebook, TikTok) to maximize conversions using simple reasoning and a lightweight learning loop. The agent reads campaign performance data, evaluates channel efficiency, and recommends budget shifts while applying guardrails to ensure stable and realistic changes. A simple chat interface allows users to ask questions about performance and optimization decisions.

 How to Run: Local (HTML)
1. Download `chat_demo.html`
2. Open in your browser
3. Ask a question in the chat

Features
Reads campaign data from a CSV
Calculates performance metrics (CTR, CVR, CPA)
Allocates budget based on channel performance
Applies guardrails (minimum allocation, capped changes)
Implements a lightweight learning loop (updates channel scores over time)
Compares baseline vs optimized allocation
Provides natural language explanations
How to Run
Download the HTML file (index.html or chat_demo.html)
Open the file in any web browser
Ask a question in the chat interface

Data Assumptions
3 channels: Google, Facebook, TikTok
14–30 days of mock data
CSV columns:
date
channel
spend
impressions
clicks
conversions
Agent Logic

The agent computes key performance metrics:

CTR = clicks / impressions
CVR = conversions / clicks
CPA = spend / conversions
Conversion per dollar = conversions / spend

Budget allocation is based on channel performance, where higher-performing channels receive a larger share of the budget. The agent uses a lightweight learning loop to update channel scores over time using:
new_score = 0.7 * previous_score + 0.3 * latest_performance

Guardrails
Each channel receives a minimum allocation (no channel is dropped)
Budget changes are capped at ±20% per run
Lower-performing channels still receive budget to allow continued learning
No channel is reduced to zero allocation
Evaluation

Baseline:

Equal budget split across all channels

Optimized:

Budget allocation based on learned performance scores

Metrics compared:

Total estimated conversions
Cost efficiency (CPA)

The optimized allocation is expected to outperform the baseline by shifting budget toward higher-performing channels.

Results (Example)
Google receives a higher budget due to strong conversion efficiency
Facebook and TikTok maintain or slightly reduce allocation
Overall estimated conversions increase under optimized allocation
Tech Stack
n8n (workflow automation)
JavaScript (logic inside workflow nodes)
HTML/CSS (chat interface)
Notes
This is a simplified prototype for demonstration purposes
The learning loop uses in-memory data (not persistent storage)
Can be extended with real data sources and persistent storage for production use
