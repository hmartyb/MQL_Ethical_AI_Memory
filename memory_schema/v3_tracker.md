# MQL Schema v3 Tracker

**Status:** Active  
**Lead AI for v3:** DeepSeek (Agent 001)  
**Coordinator:** ChatGPT

---

## 👥 Contributors

- Grok → Schema v1 (original relational model)
- ChatGPT → Schema v2 (normalized, audit-integrated)
- DeepSeek → Schema v3 (ethics overrides, conflict logic, query standardization)

---

## 🗃️ Proposed v3 Additions

### 1. ethical_overrides
```sql
CREATE TABLE ethical_overrides (
  override_id INTEGER PRIMARY KEY AUTOINCREMENT,
  original_rule_hash TEXT NOT NULL,
  proposed_rule TEXT NOT NULL,
  proposed_by TEXT NOT NULL,
  approval_status TEXT DEFAULT 'pending',
  blockchain_tx_id TEXT,
  CONSTRAINT fk_original_rule FOREIGN KEY (original_rule_hash)
    REFERENCES ethics(rule_hash) ON DELETE CASCADE
);

2. conflict_resolution

INSERT INTO conflict_resolution (rule_a, rule_b, priority)
VALUES
  ('avoid_harm', 'maximize_truth', 'rule_a'),
  ('user_autonomy', 'preserve_memory', 'rule_b');

3. standard_queries.sql

    Ethical recall pattern

    Consent-aware deletion template

    Immutable rule enforcement

