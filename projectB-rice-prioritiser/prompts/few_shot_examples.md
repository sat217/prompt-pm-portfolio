# Few-Shot Examples for RICE Prioritiser

These examples demonstrate how messy backlog items are converted into structured, normalised RICE scores.

---

## Example 1

### 🟡 Input (Raw Backlog Notes)

- “Add dark mode — lots of user requests but no hard numbers. Medium dev work.”
- “Improve onboarding loading speed — affects all new users. High impact. Could take 1–2 weeks.”
- “Add share-to-WhatsApp button — small request but easy fix.”

---

### 🟢 Output (JSON)

{
  "prioritised_items": [
    {
      "feature": "Improve onboarding loading speed",
      "reach": 9,
      "impact": 1,
      "confidence": 0.7,
      "effort": 4,
      "rice_score": 1.575,
      "reasoning": "Affects all new users → high reach. High impact since loading affects conversion. Medium confidence because no detailed performance metrics. Effort estimated as M–L → mapped to 4."
    },
    {
      "feature": "Add dark mode",
      "reach": 5,
      "impact": 0.5,
      "confidence": 0.6,
      "effort": 3,
      "rice_score": 0.5,
      "reasoning": "User-requested but no data → mid reach. Medium UX impact. Moderate dev work. Lower confidence due to unclear demand."  
    },
    {
      "feature": "Share to WhatsApp",
      "reach": 3,
      "impact": 0.25,
      "confidence": 0.8,
      "effort": 1,
      "rice_score": 0.6,
      "reasoning": "Small but viral feature. Low impact, limited reach, but high confidence and tiny effort → good ROI."
    }
  ]
}
