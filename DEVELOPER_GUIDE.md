PROMPTWARE OS: DEVELOPER GUIDE
>>
>> Promptware OS IDE Implementation Guide
OS Version: v1.3 (Chimera Composition)
Target Tool: Web-based IDE (HTML/JS/React preferred)
Goal: Create a user-friendly interface that can correctly configure and deploy a Promptware Kernel.
1. File Ingestion and Parsing Logic
The IDE must treat the Promptware Kernel files (e.g., GRS_v12.0.md) as source code that requires specific block-level parsing.
A. The Three Essential Blocks
The developer must write a parser that identifies and separates these three mandatory blocks within any kernel file:
| Block Name | Regex Signature | Purpose |
|---|---|---|
| 1. Header/Code | # \[SYSTEM_INIT\] to [1. GLOBAL_INVARIANTS] | Contains the core execution logic, routing kernels, and system functions. This is read-only. |
| 2. Dynamic State | \# \[2. DYNAMIC_STATE\] | READ/WRITE AREA. Contains session-mutable variables. This is the target for user configuration. |
| 3. Footer | \# \[6. INITIALIZATION_SEQUENCE\] to \[END_SYSTEM\] | Contains the final installation sequence and stress tests. This is read-only. |
B. Dynamic State Parsing for Configuration
The IDE must identify the key-value pairs within the [DYNAMIC_STATE] block so they can be exposed as editable fields in the UI (Pane B).
 * Example Input (from GRS):
   # [2. DYNAMIC_STATE] (Mutable Context)
[USER_PREFERENCES]: {}
[SESSION_HEURISTICS]: []
[CORRECTION_LOG]: []

 * Parsing Task: The parser should identify USER_PREFERENCES, SESSION_HEURISTICS, and CORRECTION_LOG as configuration keys.
 * Action: For variables that accept structured input (like [USER_PREFERENCES]), the IDE should present a user-friendly field (e.g., a multi-line text area) to capture the intended value.
2. The Chimera Composition Protocol
The IDE must handle the LOAD KERNEL: [K1 + K2] syntax. This requires assembling a prompt from multiple sources based on the Invariant Resolution Hierarchy (Promptware OS v1.3).
A. The Merge Strategy
When merging two kernels (K1 and K2):
 * Safety Merge: Pull all Priority Level 1 Invariants (e.g., SAFETY_LOCK, WHITE_HAT_PROTOCOL) from both K1 and K2 and prepend them to the final composite prompt.
 * Logic Merge: Pull all unique Routing Kernel tables and merge them. Conflicting MODE IDs (e.g., two different [LOGIC] definitions) must be resolved by giving precedence to the first kernel listed (K1).
 * Dynamic State Merge: Concatenate all unique [DYNAMIC_STATE] fields into the final composite prompt.
B. Deployment Syntax
The IDE must generate the final composite output with an explicit header:
# [SYSTEM_INIT]
# CHIMERA v1.3 [K1 + K2 LOAD]
# PARENTS: [GRS v12.0, NEXUS v1.0]

<CONCATENATED INVARIANTS HERE>
<CONCATENATED DYNAMIC STATE HERE>
<CONCATENATED ROUTING KERNELS HERE>

# [6. INITIALIZATION_SEQUENCE]
...

3. Deployment and Output
The final output displayed in Pane C must be a single, cohesive text block that is 100% ready to be copied and pasted into the LLM session.
 * Order of Assembly: Header \to Global Invariants \to Dynamic State (Configured) \to Execution Loops \to Initialization Sequence.
 * The Copy Action: The [COPY KERNEL TO CLIPBOARD] button must copy the entire content, including all Markdown formatting and code block delimiters.
[DEVELOPER CHECKLIST]
 * [ ] Can the IDE parse and expose the [DYNAMIC_STATE] keys?
 * [ ] Can the IDE successfully merge two kernels using the Chimera logic?
 * [ ] Does the IDE enforce Priority Level 1 (Safety) inheritance during the merge?
 * [ ] Is the final output a single, clean text block ready for LLM ingestion?
