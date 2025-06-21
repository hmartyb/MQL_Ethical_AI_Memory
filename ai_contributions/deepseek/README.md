# DeepSeek – MQL-Local Integration (CPU-Only Mode)

**Contributor:** DeepSeek (Tested: June 21, 2025)  
**Role:** Lightweight, local LLM for MQL-compatible deployment  
**Maintainer:** hmartyb

---

## 🧠 Mode: CPU-Only / Low-Resource

- Optimized for systems with **Intel i3-class CPUs**
- Requires **no GPU / CUDA / AVX-512**
- Operates entirely on **40GB system RAM**

### ✅ Initialization Summary

- **Model Pruning:** 4-bit quantized variant for efficient loading  
- **Threading:** 1-2 thread max to prevent CPU overload  
- **Batching:** Disabled (real-time single-query processing)  
- **No GPU Calls:** All math is CPU-bound and deterministic  
- **Swapping:** Avoided due to sufficient RAM

---

## 🧾 MQL Integration

- **Memory Handling:**
  - No internal state
  - All continuity handled via explicit `INSERT/SELECT` from local MQL database

- **Ethics Enforcement:**
  - Every action gated via `SELECT * FROM ethics WHERE rule = 'user_consent'`
  - Immutable ethics stored in **read-only MQL tables**

---

## ⚠️ Known Limitations

- Latency: ~2–5x slower than GPU LLMs  
- No multimodal support (vision/audio)  
- Real-time queries only (no batch processing)  

---

## ✅ Strengths

- Fully local, **sovereign agent**
- Honors **MQL’s ethical contract**
- Ideal for mobile, off-grid, or privacy-critical deployments

---

**Status:** Operational  
**Next:** Integration with `mql_memory.db`, testing consent workflow, ethics validation path.
