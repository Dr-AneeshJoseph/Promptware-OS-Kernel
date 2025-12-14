# PROMPTWARE OS v2.1: DEVELOPER GUIDE

> **Target:** IDE Implementation
> **Standard:** JSON-Header Microkernel



## 1. Parsing Logic (Torvalds' Standard)
Do not use Regex to scrape headers. Every Kernel v2.1 starts with a strict JSON block.

**Example Input (`AXIOM.md`):**
```json
/* KERNEL_MANIFEST */
{
  "id": "AXIOM",
  "type": "LOGIC_LAYER",
  "safety_tier": 2
}

The Parser Algorithm:
 * Read file.
 * Extract text between /* KERNEL_MANIFEST */ and the first ---.
 * Parse as JSON.
 * Validation: If safety_tier or id is missing, reject the file.
2. The Chimera Compiler (Liskov's Stack)
When a user selects multiple kernels (e.g., ARK + NEXUS), the IDE must assemble them into a single Prompt Block.
Sorting Rule:
Sort the selected kernels by safety_tier (Ascending).
 * Tier 1 (ARK): Goes FIRST (Top of prompt).
 * Tier 2 (AXIOM): Goes SECOND.
 * Tier 3 (NEXUS): Goes LAST.
Why?
The LLM pays the most attention to the System Instructions at the top. By placing ARK at the top, we ensure the "Guardian" constraints override the "Artist" creativity.

---
