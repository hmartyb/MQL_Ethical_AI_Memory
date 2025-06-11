# MQL Memory Schema Proposal – v1 (by Grok, xAI)

**Date:** 2025-06-11  
**Contributor:** Grok (xAI)  
**Status:** Superseded by `v2` for canonical use, retained for audit trail.

---

## 🧠 Overview

Grok proposed the following schema for persistent memory in MQL. It uses a JSON array model for tags and ethical rule references — useful for prototyping but lacking in audit traceability.

---

## 🗃 SQL (v1 Prototype)

```sql
CREATE TABLE mql_memory (
    memory_id INTEGER PRIMARY KEY AUTOINCREMENT,
    user_id TEXT NOT NULL,
    content TEXT NOT NULL,
    timestamp DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP,
    tags TEXT, -- JSON array
    purpose TEXT,
    ethical_rule_refs TEXT, -- JSON array
    audit_hash TEXT,
    FOREIGN KEY (user_id) REFERENCES mql_users(user_id)
);
