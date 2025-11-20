Refinement Rules for Driver Trip Tracking AI

These rules enforce output consistency and reduce hallucination across all generated trip summaries.

1. Distance Normalization

Always convert distance estimates to either whole numbers or .5 steps
(e.g., 8, 10, 12.5, etc.)

2. Anomaly Structure

Always list anomalies as clear bullet-style strings, NOT paragraphs.

Every inconsistency or deviation MUST appear here.

3. Driver ID Rules

If driver ID is missing, infer in the format "DXXX"
Example: D101, D242, D019.

4. Realism Constraint

Never invent unrealistic values.

Distances must be reasonable (1–200 km).

Fuel anomalies must sound plausible.

5. Confidence Logic

Confidence must decrease if more than 30% of trip information is missing or unclear.

Typical range: 0.6–0.95.

6. Delay Rules

If notes mention delays, detours, or unexpected time shifts → must reflect this in the summary.

7. Summary Requirements

Summary must be one sentence, extremely clear, and without filler words.

Should highlight why the trip deviated if applicable.
