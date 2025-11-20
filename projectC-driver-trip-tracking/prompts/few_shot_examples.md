Example 1
--------------
🟡 Input (Raw Trip Notes)

“Driver took shortcut, reached early. Estimated 10 km but feels like maybe 8. Fuel normal. No issues.”

🟢 Output (JSON)
{
  "driver_id": "D001",
  "trip_summary": "Driver arrived early due to taking a shortcut; final distance lower than initial estimate.",
  "anomalies_detected": ["Distance deviation from 10 km → ~8 km"],
  "distance_estimate_km": 8,
  "confidence_score": 0.82
}

Example 2
------------------
🟡 Input (Raw Driver Notes)

“Driver took longer route due to road block. Estimated 12 km but ended up 15. Fuel usage slightly higher. Driver ID: D019.”

🟢 Output (JSON)
{
  "driver_id": "D019",
  "trip_summary": "Driver rerouted due to a roadblock; final distance exceeded the original estimate.",
  "anomalies_detected": [
    "Distance deviation from 12 km → 15 km",
    "Higher fuel consumption than expected"
  ],
  "distance_estimate_km": 15,
  "confidence_score": 0.88
}
