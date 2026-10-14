# Sample triage prompt

Use the `lead-triage` Skill to review today's new real-estate leads.

1. Read the intended Google workbook and explicitly use the `Real Estate Leads` and `Inventory` tabs.
2. Include only records whose `Status` is exactly `New`.
3. Compare each lead's budget and property type with properties whose availability is `Available`.
4. Consider the lead source according to the Skill's defined priority rules.
5. Return a table with: Name, Budget, Source, Property Type, Priority, Reason, Suggested Action.
6. If budget, property type, source, or inventory availability is missing or inconsistent, flag the record for human review instead of guessing.
7. Do not invent properties, prices, availability, or contact details.
