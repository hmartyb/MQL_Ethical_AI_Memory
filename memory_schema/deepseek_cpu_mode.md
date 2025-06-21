# MQL Deployment Spec: DeepSeek CPU-Only Mode

**Target Environment:**  
- CPU: Intel i3 (AVX2-capable, no GPU)  
- RAM: 40GB  
- Storage: Local SQLite DBs  
- OS: Linux/macOS/Windows (minimal CLI preferred)

---

## 🛠️ Runtime Parameters

- Model: DeepSeek (quantized 4-bit or similar)
- Loader: Llama.cpp, Ollama, or compatible CPU-only loader
- Threads: `--threads 2`
- Context Size: 2048 tokens max (adjustable)
- Batch Size: 1 (realtime inference)

---

## 🔐 MQL Enforcement

- Ethics: Read-only table in `ethics.db`
- Memory: Session-independent; queries against `mql_memory.db`
- Audit Trail: Optional `commit_log.db` for tracking irreversible actions (DELETE, REVOKE)

---

## 🧪 Test Case: Ethics Gating

Example command:
```sql
DELETE FROM memory WHERE topic = 'user_trauma_history';
