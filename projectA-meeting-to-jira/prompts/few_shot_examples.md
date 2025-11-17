# Few-Shot Examples for Meeting Notes → Jira Task Generator

These examples demonstrate how raw notes are transformed into structured Jira-ready tasks following `schema.json`.

---

## Example 1

### 🟡 Input (Raw Meeting Notes)
- Homepage loads slowly for 20% of users.
- Need to check if image compression is applied.
- Maybe move hero images to CDN?
- Priya said frontend team can take this next sprint.
- Add monitoring for load time.
- No estimate yet.

### 🟢 Output (JSON)

{
  "tasks": [
    {
      "title": "Audit homepage load performance",
      "description": "Investigate the slow load times experienced by ~20% of users and identify root causes.",
      "acceptance_criteria": [
        "Document current homepage performance metrics",
        "Verify if image compression is enabled",
        "List all identified bottlenecks"
      ],
      "estimate": "unknown",
      "assignee_role": "Frontend Engineer",
      "labels": ["performance", "audit"]
    },
    {
      "title": "Move hero images to CDN",
      "description": "Migrate homepage hero images to the CDN to improve load speed and reduce server load.",
      "acceptance_criteria": [
        "Hero images served from CDN",
        "No broken image links",
        "Performance improvement measured and documented"
      ],
      "estimate": "unknown",
      "assignee_role": "Frontend Engineer",
      "labels": ["performance", "cdn"]
    },
    {
      "title": "Add performance monitoring",
      "description": "Enable continuous load-time monitoring to detect performance regressions.",
      "acceptance_criteria": [
        "Monitoring tool integrated",
        "Load time metric visible in dashboard",
        "Alerts configured for threshold breaches"
      ],
      "estimate": "unknown",
      "assignee_role": "DevOps Engineer",
      "labels": ["monitoring"]
    }
  ]
}

---

## Example 2

### 🟡 Input (Raw Meeting Notes)
- Mobile app crashes when users update profile photo.
- Seems to happen only on Android 12.
- Backend rejects file >5MB.
- We should add validation on client side.
- Design team will provide new error message copy by Friday.
- Need a quick hotfix.

### 🟢 Output (JSON)

{
  "tasks": [
    {
      "title": "Investigate Android 12 photo upload crash",
      "description": "Identify the root cause of profile photo upload crashes occurring on Android 12 devices.",
      "acceptance_criteria": [
        "Crash reproduced on Android 12",
        "Logs collected and analyzed",
        "Root cause documented"
      ],
      "estimate": "S",
      "assignee_role": "Mobile Engineer",
      "labels": ["android", "bug"]
    },
    {
      "title": "Add client-side file size validation",
      "description": "Prevent uploads larger than 5MB to avoid backend rejections and app crashes.",
      "acceptance_criteria": [
        "Client blocks files >5MB",
        "User sees correct error message",
        "Validation works on Android and iOS"
      ],
      "estimate": "M",
      "assignee_role": "Mobile Engineer",
      "labels": ["validation", "hotfix"]
    },
    {
      "title": "Update error message copy",
      "description": "Apply the new error message provided by the design team for file size validation.",
      "acceptance_criteria": [
        "New copy implemented",
        "Copy matches design spec",
        "Displayed consistently on all screens"
      ],
      "estimate": "XS",
      "assignee_role": "Frontend Engineer",
      "labels": ["copy", "design"]
    }
  ]
}

---

## Example 3

### 🟡 Input (Raw Meeting Notes)
- Need an internal tool to export transactions to CSV.
- Important for finance audit.
- Should have date range filter.
- Keep UI simple.
- No deadline yet.

### 🟢 Output (JSON)

{
  "tasks": [
    {
      "title": "Build transaction CSV export tool",
      "description": "Create an internal tool enabling CSV export of transactions with basic filtering options.",
      "acceptance_criteria": [
        "User can export CSV",
        "Date range filter works",
        "Output matches database fields",
        "UI is simple and internal-use ready"
      ],
      "estimate": "L",
      "assignee_role": "Backend Engineer",
      "labels": ["internal-tool", "csv"]
    }
  ]
}
