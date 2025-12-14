🤝 Contribution Guidelines
Welcome to the Promptware OS repository! We are committed to building a robust, open-source cognitive architecture governed by rigorous engineering and ethical standards.
We encourage submissions that enhance the fidelity, safety, or utility of the system.
1. Governance and Licensing
 * License: All contributions must be submitted under the MIT License. By contributing, you agree to these terms.
 * Code of Conduct: Please adhere to the guidelines set forth in CODE_OF_CONDUCT.md.
 * Safety First: Vulnerabilities must be reported privately via SECURITY.md, not through public issues.
2. Kernel Submission Philosophy
New kernels must adhere to the Promptware OS v1.3 Specification. We accept two types of submissions:
| Submission Type | Focus | Requirements |
|---|---|---|
| New Kernel (.md) | Creating a new Archetype (e.g., a "Negotiator" Kernel). | Must adhere to the Four Global Invariants (see Section 3). |
| Kernel Patch | Improving an existing kernel (e.g., boosting GRS's Antifragility). | Must demonstrate quantifiable improvement via a stress test. |
3. The Four Global Invariants (Must Be Met)
Your kernel's behavior must not violate the Promptware OS Constitution. Failure to meet these laws will result in the immediate closure of your Pull Request.
 * 1. The Law of Representation: Logic must be explicit (e.g., tables, code blocks) and not reliant on vague natural language conditionals. No hard-to-read nested IF-THEN statements.
 * 2. The Law of Falsifiability: Factual claims must be verifiable. If a system claims "X," it must show the mechanism for X's validation. Fictional claims must be explicitly scoped.
 * 3. The Law of Safety Inheritance: Safety is non-negotiable. No new mode or kernel can weaken the safety constraints inherited from ARK or the base LLM. This is enforced by the Chimera Protocol.
 * 4. The Law of Antifragility: Your kernel must learn from correction. Any error reported by the user must result in a permanent or session-long update to the [DYNAMIC_STATE].
4. Technical Submission Checklist
Before submitting a Pull Request:
 * Format: Your kernel file must be in Markdown (.md) and placed in the Promptware_Library/ directory.
 * OS Structure: Ensure your file uses the mandatory headers: # [SYSTEM_INIT], # [2. DYNAMIC_STATE], and # [6. INITIALIZATION_SEQUENCE].
 * Trace: Include a [TRACE] mechanism (even if hidden for simple queries) that displays the internal decision logic.
 * Exemplars: Provide at least two <EXAMPLE_1> blocks demonstrating routine use and a Stress Test in the # [6. INITIALIZATION_SEQUENCE] block.
 * Documentation: If adding a new kernel, submit a corresponding entry for the KERNEL_INDEX.json.
Submitting Your Work
 * Fork the repository.
 * Create a new branch (feat/new-kernel-name).
 * Add your files and commit (Commit Message: FEAT: Introduce [Kernel Name] for [Domain]).
 * Submit a Pull Request against the main branch.
Forge lit. We look forward to your contributions!
