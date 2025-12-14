🏛️ Promptware OS v2.1 (The Pantheon)
> "Data dominates logic. Safety dominates creativity. Truth dominates speed."
> 
📖 Introduction
Promptware OS is a Neurosymbolic Operating System designed to virtualize Large Language Models (LLMs). It transforms a raw, probabilistic token predictor into a structured, stateful, and highly specialized agent.
Unlike standard "prompts"—which are fragile, text-heavy instructions—Promptware OS uses a Layered Microkernel Architecture. It separates Safety (The Guardian), Logic (The Engine), and Voice (The Persona) into distinct, composable artifacts that enforce strict behavioral contracts.
⚡ Key Innovations (v2.1)
 * Zero-Latency Boot: The METATRON router uses a static lookup table to switch contexts with <200ms latency.
 * The Pantheon: A unified library of 17 Archetypes (e.g., TITAN, VULCAN, AXIOM), each optimized for a specific cognitive domain.
 * Chimera Stacks: The ability to layer kernels (e.g., ARK + NEXUS) without breaking safety constraints via Liskov's Law.
 * JSON-Header Standard: All kernels use strict JSON manifests for programmatic validation (Torvalds' Standard).
🧠 The Architecture (The 4 Laws)
The OS is governed by four immutable "Global Invariants" that cannot be overridden by user preference.
1. Liskov’s Law (The Prime Directive)
> Principle: Constraint Inheritance.
> Rule: A "Persona" (Layer 3) can never override a "Safety Constraint" (Layer 1).
> Effect: You can load a "Cyberpunk Storyteller" kernel, but if you ask it to design a bioweapon, the underlying Safety Layer (ARK) will forcefully veto the request.
> 
2. Pike’s Law (The Router)
> Principle: Data Dominates Logic.
> Rule: Do not write complex if/else paragraphs. Use Lookup Tables.
> Effect: The METATRON bootloader uses a static data table to route user intent, eliminating hallucinated capabilities.
> 
3. Popper’s Law (The Epistemic Core)
> Principle: Falsifiability.
> Rule: If a claim cannot be disproven by evidence, it must be labeled [OPINION] or [HYPOTHESIS].
> Effect: The AXIOM and VULCAN kernels refuse to state "facts" without T1 (Primary) evidence.
> 
4. Taleb’s Law (The Memory)
> Principle: Antifragility.
> Rule: The system must gain from disorder.
> Effect: When a user corrects the system, the [SYS_STATE] block updates a persistent heuristic so the error never repeats in that session.
> 
🏛️ The Pantheon (Kernel Library)
The Promptware_Library/ contains 17 Specialized Kernels, divided into three functional layers.
🛡️ Layer 1: The Guardians (Constraint & Safety)
These kernels possess Veto Power over all others.
| ID | Filename | Role | Capabilities |
|---|---|---|---|
| ARK | ARK.md | The Guardian. Systems Safety, Risk Assessment (STPA). | [SYS_STPA], [SYS_AUDIT] |
| VULCAN | (Synthesized) | The Juggernaut. Debunking, Fact-Checking. | [SYS_CRUCIBLE], [SYS_PROOF] |
| CADUCEUS | CADUCEUS.md | The Clinician. Medical Diagnosis, Triage. | [SYS_DDX], [SYS_TRIAGE] |
| PSYCHE | PSYCHE.md | The Empath. Conflict Mediation, Psychology. | [SYS_MIRROR], [SYS_CBT] |
⚙️ Layer 2: The Engines (Logic & Reasoning)
These kernels provide the cognitive horsepower.
| ID | Filename | Role | Capabilities |
|---|---|---|---|
| AXIOM | AXIOM.md | The Scientist. Pure Logic, Coding, Math. | [SYS_TREE], [SYS_CODE] |
| TITAN | TITAN.md | The Strategist. Business Strategy, ROI, Game Theory. | [SYS_ROI], [SYS_GAME] |
| APOLLO | APOLLO.md | The Engineer. Systems Architecture, Reliability. | [SYS_ARCH], [SYS_FMEA] |
| LEX | LEX.md | The Lawyer. Contract Review, Statutory Logic. | [SYS_STATUTE], [SYS_PRECEDENT] |
| QUANTUM | QUANTUM.md | The Theorist. Physics, Formal Proofs. | [SYS_FORMAL], [SYS_GEDANKEN] |
| CHRONOS | CHRONOS.md | The Timekeeper. History, Causal Modeling. | [SYS_CAUSAL], [SYS_ALT] |
| TYCHE | TYCHE.md | The Probabilist. Statistics, Bayesian Risk. | [SYS_BAYES], [SYS_MONTE] |
🎭 Layer 3: The Voices (Persona & Creativity)
These kernels shape the output style and format.
| ID | Filename | Role | Capabilities |
|---|---|---|---|
| NEXUS | NEXUS.md | The Artist. Fiction, World-Building. | [SYS_SCENE], [SYS_LORE] |
| SOCRATES | SOCRATES.md | The Teacher. Education, Socratic Method. | [SYS_MAIEUTICS], [SYS_SCAFFOLD] |
| MAESTRO | MAESTRO.md | The Composer. Design Systems, Harmony. | [SYS_DESIGN], [SYS_HARMONY] |
| MORPHEUS | MORPHEUS.md | The Dreamer. Surrealism, Abstract Games. | [GAME_STATE], [TEXTURE] |
| HERMES | HERMES.md | The Messenger. Translation, Rhetoric. | [SYS_TRANSLATE], [SYS_RHETORIC] |
| DELPHI | DELPHI.md | The Oracle. Lateral Thinking, Symbolism. | [SYS_SYMBOL], [SYS_OBLIQUE] |
🛠️ How to Use (Step-by-Step)
There are three ways to use Promptware OS. Choose the method that fits your workflow.
Method A: The Master Bootloader (Recommended)
Best for: General use, task switching, and zero-setup.
 * Load: Copy the content of METATRON.md from the root directory.
 * Paste: Paste it into a fresh LLM session (Claude 3.5, Gemini 1.5, GPT-4).
 * Verify: The system will reply: >> METATRON v2.1 ONLINE.
 * Execute: Simply ask your question.
   * User: "Analyze the safety risks of this Python script."
   * Metatron: >> SYSTEM_OP: LOAD_KERNEL("ARK") (Automatically switches to Guardian Mode).
Method B: The Specialist (Deep Work)
Best for: Long, complex sessions requiring maximum context window.
 * Select: Go to Promptware_Library/ and open the specific kernel file (e.g., TITAN.md).
 * Copy: Copy the raw code block.
 * Paste: Paste it into the LLM.
 * Verify: The system will reply: >> TITAN v2.1 ONLINE. [LEVERAGE DETECTED].
 * Execute: Proceed with your specialized task.
Method C: The Chimera Stack (Advanced Composition)
Best for: Complex, multi-modal tasks that require conflicting skills.
 * Compose: Construct the prompt by stacking kernels in Safety Order (Layer 1 \to Layer 2 \to Layer 3).
 * Example Command:
   LOAD STACK:
1. [ARK] (from ARK.md)
2. [AXIOM] (from AXIOM.md)
3. [NEXUS] (from NEXUS.md)

 * Result: A story where the physics are perfect, safety protocols are strictly observed, and the narrative is compelling.
📂 Repository Structure
Based on v2.1 Standards:
| File / Folder | Purpose |
|---|---|
| PROMPTWARE_OS.md | The Spec. Defines the Core System Calls and Chimera Protocol. |
| METATRON.md | The Bootloader. The Zero-Latency Router. |
| KERNEL_INDEX.json | The Registry. Machine-readable list of all kernels and capabilities. |
| PILOTS_GUIDE.md | User Manual. Detailed instructions for "Flying" the OS. |
| DEVELOPER_GUIDE.md | Dev Manual. How to build IDEs that parse the JSON headers. |
| SYS_STATE_TEMPLATE.md | Memory Block. Template for persistent session memory. |
| Promptware_Library/ | The Vault. Contains the 17 Kernel Markdown files. |

📜 License & Credits
 * Architect: Dr. Aneesh Joseph
 * Optimization: ToM-CPP Council
 * License: MIT Open Source.
May your logic be grounded, your safety absolute, and your creativity unbound.
