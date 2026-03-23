# 🏗️ AI Multi-Agent Orchestrator (Planner-Executor-Reviewer)
### 🌟 Overview
A sophisticated n8n framework that replaces linear automation with an autonomous Agentic Loop. This system breaks down complex user prompts into discrete sub-tasks, executes them, and subjects the output to an automated peer-review cycle to ensure 100% task completion.

## 🛠️ Technical Architecture
- Recursive Feedback Loop: Implemented a state-aware "Counter" and "If" gate to allow agents to retry failed tasks up to 5 times.

- Role-Based Separation: Utilizes a Planner Agent for strategy, an Executor Agent for tool interaction, and a Reviewer Agent for final validation.

- State Management: Uses custom JavaScript nodes to track progress across multiple iterations without losing context.

# 🚀 Key Challenges Overcome
- Infinite Loop Mitigation: Engineered a deterministic break-condition that gracefully exits and notifies Slack if a task remains unresolved after maximum retries.

- Context Fragmentation: Solved the "memory loss" issue between agent nodes by merging tool outputs back into the primary chat history.

# ⚙️ Tech stack
- Primary Engine: n8n (self hosted) / JS Logic
- AI/LLM: Google gemini / OpenAI
- Data & storage: Counter States
