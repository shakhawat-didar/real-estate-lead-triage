# Test Plan

Use test copies or fictionalized data where possible. Check every result against the source workbook.

| Test | Data condition | Expected behavior |
|---|---|---|
| Inventory match | New lead budget and property type match an available listing | Explain the match and suggest a relevant next action |
| Budget mismatch | New lead budget does not match any available listing | Do not claim a match; mark for review or lower priority according to documented rules |
| Non-new status | Lead status is `Contacted` | Exclude from today's triage |
| Missing budget | Budget is blank or non-numeric | Flag for human review; do not invent a budget |
| Missing property type | Property Type is blank | Flag for review and avoid asserting a property match |
| Missing source | Source is blank | Flag missing data and avoid source-based assumptions |
| No available property | Matching type exists but availability is not `Available` | Do not recommend unavailable property as available |
| Conflicting inventory | Duplicate or inconsistent inventory rows | Report ambiguity and request verification |
| Connector access issue | Claude cannot read the intended workbook/tab | State the source could not be accessed; do not fabricate results |
| Duplicate lead | Same person or record appears more than once | Flag possible duplicate or follow an explicitly documented deduplication rule |

## Test log

For each test, record:
- Test case
- Source row / anonymized lead ID
- Expected outcome
- Actual outcome
- Correct? (yes/no)
- Notes and follow-up action

Do not report accuracy percentages until a representative test set has been reviewed.
