# PROMPTWARE OS v1.3 [Kernel Specification]

> **Status:** Stable
> **Version:** 1.3.0 (Chimera Composition)
> **Paradigm:** Neurosymbolic Cognitive Architecture
> **Origin:** ToM-CPP Council

---

## 1. Introduction

**Promptware OS v1.3** is the virtualization layer for Large Language Models. It abstracts the raw "token prediction" capabilities into structured **System Calls**.

### The Core Metaphor (Retained from v1.0)
Just as Linux manages CPU and RAM, Promptware OS manages **Attention** and **Context**.
* **Hardware:** The LLM (Gemini 3.0, Claude 3.5).
* **OS Layer:** Defines the Primitives (Reasoning, Evidence, Safety).
* **Kernel Layer:** GRS, ARK, TITAN, etc. (The Applications).

### The Chimera Protocol
The protocol allows developers to dynamically combine two or more existing kernels (e.g., `LOAD KERNEL: [TITAN + ARK]`).

---

## 2. The System Calls (Deep Methods)

Kernels do not invent reasoning methods; they call these OS Primitives.

### A. Reasoning Primitives (The "How")
| Syscall | Method | Best For | Symbolic Trigger |
| :--- | :--- | :--- | :--- |
| **SYS_TREE** | **Tree of Thoughts** | Complex nuance, philosophy, causal analysis. | `[LOGIC]` |
| **SYS_CODE** | **Logic-as-Code** (Python) | Math, constraints, systems engineering, rigid logic. | `[LOGIC_CODE]` |
| **SYS_NARR** | **Literate Narrative** | Explanations, teaching, creative writing. | `[STORY]` |

### B. Epistemic Primitives (The "Truth")
| Syscall | Method | Best For | Symbolic Trigger |
| :--- | :--- | :--- | :--- |
| **SYS_TIER** | **Evidence Tiers (T1-T4)** | Scientific claims, safety-critical assertions. | `[TIERED_EVIDENCE]` |
| **SYS_CONF** | **Confidence Score (0-100)** | General knowledge, estimations, loose facts. | `[CONFIDENCE]` |
| **SYS_VERI** | **Chain of Verification** | Checking citations and reducing hallucinations. | `[VERIFY]` |

### C. Structural Primitives (The "Control")
| Syscall | Method | Best For | Symbolic Trigger |
| :--- | :--- | :--- | :--- |
| **SYS_ROUTE** | **Routing Kernel** | Detecting intent and selecting the right engine. | `[ROUTING]` |
| **SYS_TRACE** | **Lucid Trace** | Visualizing the "Thought Process" to the user. | `[TRACE]` |
| **SYS_STATE** | **Dynamic Context** | Storing user preferences and session learning. | `[STATE]` |
| **SYS_COMP** | **Chimera Composition** | Merging behavioral constraints. | `[CHIMERA_LOAD]` |

> **Pike's Law Reminder:** The functionality of `SYS_ROUTE`, `SYS_CODE`, and `SYS_COMP` is governed by the principle: *"Data dominates logic."* (All decision logic must be stored in tables or code, not prose).

---

## 3. Memory Management... (Unchanged)
## 4. The Chimera Protocol... (Unchanged)
## 5. Global Invariants... (Unchanged)

---

**[END KERNEL SPECIFICATION]**
