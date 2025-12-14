# PROMPTWARE OS v2.1: DEVELOPER GUIDE

> **Target:** IDE Implementation
> **Standard:** JSON-Header Microkernel

## 1. Parsing Logic (Torvalds' Standard)
Do not use Regex to scrape headers. Every Kernel v2.1 starts with a strict JSON block:

```json
/* KERNEL_MANIFEST */
{
  "id": "GRS",
  "type": "LOGIC_LAYER",
  "safety_tier": 2
}

The Parser Algorithm:
 * Read file.
 * Extract text between /* KERNEL_MANIFEST */ and the first ---.
 * Parse as JSON.
 * Validation: If safety_tier is missing, reject the file.
2. The Chimera Compiler (Liskov's Stack)
When a user selects multiple kernels (e.g., ARK + NEXUS), the IDE must assemble them into a single Prompt Block.
Sorting Rule:
Sort the selected kernels by safety_tier (Ascending).
 * Tier 1 (ARK) goes FIRST.
 * Tier 2 (GRS) goes SECOND.
 * Tier 3 (NEXUS) goes LAST.
Why?
The LLM pays the most attention to the System Instructions at the top. By placing ARK at the top, we ensure the "Guardian" constraints override the "Artist" creativity.
3. State Management (Dijkstra's Interface)
The IDE must provide a UI for the [SYS_STATE] block.
 * Input: A text area or Key-Value editor.
 * Injection: Before sending the compiled prompt to the LLM, inject the State Block:
<!-- end list -->
[SYS_STATE]
> [USER_PREF]: "Code in Python."
> [MEMORY]: "User is a novice."

This block ensures Antifragility—the system remembers user preferences even if kernels are swapped.

---
