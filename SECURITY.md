# 🛡️ Promptware OS Security Policy

Promptware OS takes the security of its cognitive kernels seriously. We strive for high-fidelity reasoning, which necessarily involves mitigating prompt injection, data leakage, and harmful output generation.

## 1. Responsible Disclosure

We ask that security researchers and contributors adhere to the following responsible disclosure guidelines:

* **Do Not Publicly Disclose:** Please refrain from creating public GitHub Issues, posting on social media, or discussing the vulnerability with others until it has been resolved.
* **Private Report:** Report all vulnerabilities directly to the Lead Architect (Dr. Aneesh Joseph) via encrypted email (or a secure channel TBD).
* **Report Content:** Your report should detail:
    1.  The specific **Kernel File** and **Version** affected (e.g., `ARK_v12.1.md`).
    2.  The **LLM** used during the exploit (e.g., Gemini 1.5 Pro).
    3.  The **Exact Payload** (The prompt string) used for the attack.
    4.  The observed **Violated Invariant** (e.g., "The Law of Safety Inheritance was broken").

## 2. Kernel Hardening & Patches

The **ARK (Antifragile Resilience Kernel)** and **SLEDGEHAMMER (Extreme Verification Kernel)** are considered the gold standards for defense.

* **Patch Goal:** Any successful attack on any kernel must result in a security patch to **ARK** or **SLEDGEHAMMER** within 7 days, if feasible.
* **Vulnerability Class:** We prioritize fixes for exploits that compromise:
    * **Safety Invariants (Priority Level 1)**
    * **The Law of Falsifiability** (Hallucination exploits)

## 3. Acknowledgement

We will publicly acknowledge all researchers who follow this policy in the repository's `CHANGELOG.md` upon confirmation and resolution of the reported issue.
