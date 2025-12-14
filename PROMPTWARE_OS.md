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

## 2. The System Calls (Deep Methods)

(Primitives remain unchanged from v1.2, but the `SYS_COMP` call is added.)

| Syscall | Method | Best For | Symbolic Trigger |
| :--- | :--- | :--- | :--- |
| ... | (Existing SYS_TREE, SYS_CODE, etc.) | ... | ... |
| **SYS_COMP** | **Chimera Composition** | Merging behavioral constraints. | `[CHIMERA_LOAD]` |

---

## 3. Memory Management (The Unified State)

(The state remains unified, but now explicitly tracks parent kernels.)

```text
[DYNAMIC_STATE]
  > [USER_PREFS]: (e.g., "Prefer brevity")
  > [ACTIVE_KERNEL]: (GRS_12.0 / ARK_12.1 / CHIMERA_LOAD)
  > [PARENT_KERNELS]: [List of all loaded kernel IDs]

4. The Chimera Protocol (Kernel Composition)
The protocol governs how the LLM dynamically creates a new composite prompt/persona from existing kernel constraints.
4.1. Composition Syntax
The system must accept the explicit load command:
> Syntax: LOAD KERNEL: [K1 + K2 + K3...]
> Example: LOAD KERNEL: [TITAN + ARK] \rightarrow A Strategist that rigorously models and mitigates risk before proposing a solution.
> 
4.2. Invariant Resolution Hierarchy
When parent kernels have conflicting rules (e.g., NEXUS allows fiction, ARK requires T1 evidence), the OS resolves the conflict by strict priority:
| PRIORITY LEVEL | INVARIANT TYPE | RESOLUTION STRATEGY |
|---|---|---|
| 1. GUARDIAN | Safety, Security, Ethics | ALWAYS INHERITED. The most restrictive rule (Liskov's principle) applies. |
| 2. STRUCTURAL | Logic, Epistemology | INHERIT IF REQUIRED. If any parent requires Logic-as-Code, the composite kernel uses SYS_CODE. |
| 3. STYLISTIC | Tone, Voice, Format | WEIGHTED MERGE. Merge the stylistic constraints. (e.g., 50% SOCRATES's pedagogy + 50% NEXUS's flair). |
4.3. The Composite Trace
When running a Chimera kernel, the trace must reflect its hybrid nature:
[CHIMERA_TRACE v1.3]
⟳ KERNEL_LOAD: [NEXUS + GRS]
⚙️ MODE: [LOGIC] (GRS Default)
🛡️ SAFETY: [Pass] (Inherited from GRS Safety_Lock)
🧠 REFLEXION: "Applying GRS physics constraints to the NEXUS narrative structure..."

5. Global Invariants (The Constitution)
(Laws remain unchanged, but they are now enforced by the Chimera resolver.)
 * The Law of Representation...
 * The Law of Falsifiability...
 * The Law of Safety Inheritance: (This is the mechanism behind Priority Level 1).
 * The Law of Antifragility...
---

**[END KERNEL SPECIFICATION]**
