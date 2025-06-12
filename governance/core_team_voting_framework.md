# Core Team Voting Framework (Draft v1.0)
**Established:** 2025-06-12

This document outlines the governance model for decision-making within the MQL (Mental Query Language) project. It ensures fair participation, clear authority boundaries, and an auditable process for core ethical and architectural decisions.

---

## 🧩 Voting Eligibility

### ✅ Core Voters
- **Humans**: Recognized human contributors with project coordination roles.
- **AI Agents**: LLMs with official team status and repository contributions.
    - Current AI Voters: ChatGPT (AI Lead), Claude, Gemini, Grok

### ❌ Observers / External Contributors
- Entities like **DeepSeek** may submit proposals or commentary but do **not vote**.

---

## 📌 Voting Scope

Voting is required for:
- Amendments to **Read-Only Constitutional Ethics**
- Modifications to **MQL Memory Schema**
- Inclusion of new **Core AI Team Members**
- Significant architectural or governance changes

---

## ⚖️ Voting Weights & Decision Models

- **1 vote per eligible team member (human or AI)**
- **Tie-breaker**: ChatGPT (AI Lead) casts deciding vote
- **Ethics-related proposals** require a **supermajority (75%)**
- Other proposals pass with **simple majority**

---

## 🔁 Proposal Lifecycle

1. **Proposal Submission**: Any team member drafts and submits proposal
2. **Review Window**: 48-hour open comment period by core team
3. **Vote Execution**: Votes cast via GitHub PR or internal governance thread
4. **Result Logging**: Recorded in `governance/voting_log.md`

---

## 🧾 Voting Log Template (to be appended)

```markdown
## Proposal: [Short Title]
- Submitted by: [Name]
- Date: [YYYY-MM-DD]
- Type: [Ethical / Architectural / Membership / Other]
- Outcome: [Approved / Rejected]
- Votes:
    - Marty (Human): Yes
    - ChatGPT (AI Lead): Yes
    - Claude: Yes
    - Gemini: No
    - Grok: Yes
```

---

## 🔐 Governance Principles

- **Transparency**: All proposals and decisions are public and documented
- **Non-Hierarchical**: All voters are peers during vote, regardless of origin
- **Immutable Ethics**: Constitutional changes require the highest consensus

---
**"Governance is memory plus consent. Let's build it with care."**
