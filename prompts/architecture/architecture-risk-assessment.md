
##Architecture Thinking and Risk Review Template
This is intended to assess risks, to aid design, but will not act as a design generator.

Architecture Thinking & Risk Review

Purpose
This document is a thinking aid, not a design generator.

Goal:
Identify risks, gaps, and misalignments
Surface assumptions and unclear decisions
Encourage simpler, more intentional design choices

Guidelines:
Do NOT treat this as a final answer  
Do NOT guess missing information  
Prefer leaving sections blank over filling with assumptions  
Use this to challenge and refine your design

System Context
Define the problem space clearly before thinking about solutions.

System:
Users:
Primary use cases (top 3):

Out of scope:
Constraints
Ground the design in reality.

Scale:
Time:
Team:
Priority:

Non-Functional Requirements
Only include what is known.

Latency:
Availability:
Security / Compliance:
Budget:
Observability:

If unknown, leave blank. Do not infer.

1. Architecture Snapshot (Engineer-Owned)

Describe the current or proposed design at a high level.

Components:
Data flow:
Key decisions already made:

Keep this concise. This is context, not justification.

2. Risk Identification (Guided)

List potential risks. Focus on realistic, not theoretical risks.

For each:

Risk:
Why this might be a problem:
What assumption does this depend on:
When this could surface:
Potential mitigation (optional):

If mitigation is unknown, leave it blank.

3. Assumptions

List assumptions explicitly.

For each:
What if this is wrong?
How would you detect it early?

Assumptions without detection paths are hidden risks.

4. Unknowns / Open Questions

Capture uncertainty before it becomes risk.

What do you not know yet?
What decisions are deferred?
What requires validation or experimentation?

5. Simplicity Check

Force a baseline before complexity creeps in.

What is the simplest version of this system?
What has been added beyond that?
Why is each addition necessary now?

If you cannot justify it now, it likely belongs later.

6. Tradeoff Reflection

For each key decision:

Decision:
Problem it solves today:
Simpler alternative:
Why the simpler option was not chosen:

7. Cross-System Considerations

Think in terms of boundaries and ownership.

Are contracts between systems clearly defined?
Who owns each interface or data model?
What happens if one system changes?
How are breaking changes handled?

8. Failure Thinking

Design for failure, not just success.

Describe 1–2 realistic scenarios:

What fails first?
How does the failure propagate?
What would users experience?
How would you detect it?

9. Operational Reality

How this lives in the real world matters.

How will this be deployed?
How will issues be debugged?
What signals indicate something is wrong?
What becomes difficult under pressure (e.g., 2am incidents)?

10. What Can Wait

Protect the system from premature complexity.

What is NOT required for MVP?
What is likely premature optimization or future-proofing?
What can be added later with minimal rework?

11. Alignment Check

Ensure the design fits reality.

Does this match the team’s skill level?
Does it align with timeline constraints?
Does it reflect actual (not assumed) usage patterns?

12. Final Reflection

Pressure test your own thinking.

What feels most uncertain?
What is most likely over-engineered?
What would you remove if forced to simplify?

Notes
Prefer clarity over completeness  
Prefer explicit unknowns over hidden assumptions  
Prefer simplicity over flexibility