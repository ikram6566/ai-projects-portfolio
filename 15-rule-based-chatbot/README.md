# Rule-Based Chatbot

A transparent FAQ chatbot built on **regex intents** — no machine learning, no API keys, no black box. Every answer can be traced to an exact rule.

## Verified result (executed notebook)
- **Intent check: 9/9 scripted lines behaved as expected** (8 intents matched, 1 off-topic line correctly fell back)

Intents: greeting, services, pricing, timings, contact, projects, thanks, bye — plus honest fallbacks that admit the bot's limits.

## Run it
Open `rule_based_chatbot.ipynb` and run all cells, then chat with the `ChatBot` class using your own lines.

## Why rule-based still matters
For FAQs, bookings and support triage, a rule-based bot is predictable, free to run and impossible to "hallucinate" with. It is the design most business chatbots still start from.
