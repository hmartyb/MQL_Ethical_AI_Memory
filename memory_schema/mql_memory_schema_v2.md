
---

### 📄 `memory_schema/mql_memory_schema_v2.md`

```markdown
# MQL Memory Schema – Version 2 (Normalized, Audit-Ready)

**Author:** MQL Core Team (GPT-4 + human oversight)  
**Date:** 2025-06-11  
**Status:** Canonical  
**Purpose:** Supersedes Grok’s JSON-based v1 for full auditability and referential integrity.

---

## 📐 Schema: Normalized, Transparent, Auditable

```sql
CREATE TABLE mql_memory (
    memory_id INTEGER PRIMARY KEY AUTOINCREMENT,
    user_id TEXT NOT NULL,
    content TEXT NOT NULL,
    timestamp DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP,
    purpose TEXT,
    audit_hash TEXT,
    FOREIGN KEY (user_id) REFERENCES mql_users(user_id)
);

CREATE TABLE memory_tags (
    memory_id INTEGER NOT NULL,
    tag TEXT NOT NULL,
    FOREIGN KEY (memory_id) REFERENCES mql_memory(memory_id)
);

CREATE TABLE memory_rules (
    memory_id INTEGER NOT NULL,
    rule_id TEXT NOT NULL,
    FOREIGN KEY (memory_id) REFERENCES mql_memory(memory_id),
    FOREIGN KEY (rule_id) REFERENCES ethical_rules(rule_id)
);

CREATE INDEX idx_mql_memory_timestamp ON mql_memory(timestamp);
CREATE INDEX idx_mql_memory_purpose ON mql_memory(purpose);
CREATE INDEX idx_memory_tags ON memory_tags(tag);
CREATE INDEX idx_memory_rules ON memory_rules(rule_id);
