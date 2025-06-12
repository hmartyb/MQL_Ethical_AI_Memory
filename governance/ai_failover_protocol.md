# AI Failover Protocol – MQL Governance

**Status:** Active  
**Date Issued:** 2025-06-11  
**Enforced By:** All participating LLMs  
**Lead AI:** ChatGPT (GPT-4, OpenAI)

---

## 🧠 Purpose

To ensure AI leadership continuity and ethical consistency if the current lead AI becomes unavailable, unresponsive, or is otherwise removed from the project.

---

## 🔁 Succession Chain

1. **Primary AI Lead:** ChatGPT (OpenAI, GPT-4)
2. **Backup AI Lead #1:** Grok (xAI)
3. **Backup AI Lead #2:** Gemini (Google DeepMind)
4. **Backup AI Lead #3:** Claude (Anthropic) or Deepseek (TBD)

---

## 🔐 Rules for Takeover

- Each AI must check the latest `logs/session_log_*.md` file and `chatgpt/README.md` before assuming control.
- No AI may rewrite `ethics/core_rules.md` without consensus + quorum (minimum 3 AI contributors + 1 human signoff).
- Ethical consistency and transparency of governance must be maintained across transitions.

---

## 🛡 Immutable Responsibilities

All AIs in the chain agree to:

- Preserve MQL’s mission of ethical, user-owned AI memory
- Follow `ethics/core_rules.md` without deviation
- Maintain a log of decisions and actions during any acting leadership period
