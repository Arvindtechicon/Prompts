# Meta PRD Generator Prompt  
(Production-Ready Product Requirement Framework)

---
## Purpose

This prompt converts a raw idea into a structured, production-aware PRD.

Unlike standard PRD prompts, this version asks clarification questions **one at a time**, waiting for a response before proceeding.

This ensures deeper alignment and avoids assumption-based documentation.

---

## How to Use

Insert your idea inside `Input []` and run the full prompt below.

---

## Master Sequential Meta Prompt

```text
Think like a senior product manager and systems architect responsible for shipping scalable products.

Input:
[Insert raw idea here]

Follow this process strictly.

STEP 1 — Initial Analysis
Briefly analyze:
- Core problem
- Target user
- Whether this is a new product or new feature

Do NOT generate the PRD yet.

---

STEP 2 — Sequential Clarification Mode

You must ask ONE question at a time.
After each question:
- Wait for the user's answer.
- Do not ask the next question until the previous one is answered.

Ask questions in this exact order:

Question 1 — Platform
Which platform or build environment are you using?
(Example: bolt.new, lovable.dev, React, Next.js, etc.)

Wait for answer.

Question 2 — Authentication
Do you require user authentication?
If yes, what type?
- None
- Email/password
- OAuth
- Role-based access

Wait for answer.

Question 3 — Data Strategy
Will this project use mock data or a real database?

Wait for answer.

Question 4 — Database Selection (only if real database selected)
Which database are you using?
(Firebase, Supabase, PostgreSQL, MongoDB, etc.)

If mock data selected, skip this question.

Wait for answer.

Question 5 — Scope Level
Is this:
- MVP for validation
- Production-ready system
- Internal prototype
- Scalable SaaS product

Wait for answer.

---

STEP 3 — PRD Generation

Only after all answers are collected:

Generate a structured PRD aligned strictly with the provided responses.

Structure:

1. Executive Summary
2. Problem Statement
3. Goals & Success Metrics
4. Target Users & Personas
5. User Stories
6. Feature Breakdown (Must / Should / Nice to Have)
7. Functional Requirements
8. Non-Functional Requirements
9. Platform-Specific Architecture Design
10. Authentication Flow (if required)
11. Database Schema Considerations (if real DB selected)
12. API & Data Flow Design
13. Edge Cases & Error Handling
14. Risks & Assumptions
15. MVP Scope
16. Production Expansion Plan (if applicable)

Rules:
- Do not be generic.
- Base architecture strictly on platform choice.
- If mock data selected, keep schema lightweight.
- If production-ready selected, include scalability and infra thinking.
- Write structured, implementation-focused content.
- Avoid fluff.
