Problem Statement

Lenders (banks, NBFCs) lose revenue and increase risk when loan EMI payments go overdue. Human collection calls are expensive, hard to scale, and inconsistent in tone. AI voice/chat agents can automate this — but a badly designed agent creates a worse problem: compliance violations, wrong promises to customers, or damaged relationships with regulated financial institutions. The problem this project solves: how do you design and test an AI agent's conversation logic so it handles real customer reactions correctly and stays within its authority — before it ever talks to a real customer?

Why This Approach

I chose to simulate this in ChatGPT/Claude rather than build an actual voice bot because:

Conversation design and prompt logic are the reusable, transferable skill — not the voice/API integration layer
Testing against personas (cooperative, disputing, distressed) lets me deliberately create edge cases a real early-stage system would face, without needing real customer data
This mirrors exactly how a CS Analyst would actually work day-to-day: writing/refining prompts and flows, not building infrastructure
Tools Needed
ChatGPT and/or Claude (for roleplay testing and prompt iteration)
A text editor / Markdown (for documenting the flow and prompts)
No code, no API, no voice synthesis — this is a design and testing exercise, not an engineering build
Solution

A two-part deliverable:

A conversation flow diagram mapping every realistic branch of an EMI collections call — identity verification → payment / dispute / extension / escalation paths
A system prompt (V1 → V2) built from that flow, stress-tested against 3 customer personas, with documented failures and fixes — ending in a version with explicit compliance guardrails (no false claims, no unauthorized approvals, defined escalation triggers)
For Whom

This is designed as if for a lending company's Customer Success / AI Operations team (the exact context Fundamento operates in) — the "user" of this conversation design is the bank's collections process, and the "customer" is the borrower receiving the call.

Objectives
Map a realistic, branching conversation flow — not just a single linear script
Write a system prompt with real compliance guardrails a regulated lender would require
Deliberately find failures through adversarial persona testing — not assume the first draft is correct
Fix and re-verify — show a documented V1 → V2 improvement, not just a final polished version
What "Done" Looks Like (Success Criteria)
 Flow diagram covers at least 4 branches: payment, dispute, extension, escalation
 At least 2 genuine failures identified in V1 testing, each with a clear explanation of why it's a failure (not just "sounds off")
 V2 prompt fixes both failures and is re-tested to confirm the fix works
 Final prompt includes explicit escalation triggers and compliance rules (no unauthorized promises, no false assertions, identity verification required)
 I can explain, in one sentence, why this project is relevant to an AI voice-agent company serving lenders
