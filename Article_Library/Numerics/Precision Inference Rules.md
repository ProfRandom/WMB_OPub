---
project: wmb
phase: 1
module: 1
status: draft
created: <%* tp.file.creation_date("YYYY-MM-DD") %>
updated: <%tp.date.now("YYYY-MM-DD") %>
summary: ""
---
 

# Precision Inference Rule #1
In enumerations of values, all numbers should be shown to the decimal precision of the most precise member of the set.

Example:
- 1.000
- **3.142**
- 5.500
- 4.650

# 🔬 Precision Inference Rule #2

> The **decimal precision of a randomized result** is inferred from the **most precise** range endpoint.

| Syntax            | Result Precision |
| ----------------- | ---------------- |
| ⟨⟨1.4 ∧ 2.2⟩⟩     | 1 decimal place  |
| ⟨⟨1.40 ∧ 2.2⟩⟩    | 2 decimal places |
| ⟨⟨1.400 ∧ 2.200⟩⟩ | 3 decimal places |

This rule applies **even if the endpoints are excluded** from the valid output range.

