# Prompting Strategy Note: Content Moderation Rules & Benchmark Grounding

## Context & Purpose
When prompting an AI agent to draft content moderation policy rules, general guidelines often lead to vague outputs. To ensure high precision and compliance consistency, prompt engineering must explicitly enforce edge-case rules and bind them to benchmark dataset examples.

## Key Prompt Components

### 1. Clear Persona & Task Assignment
Establish the role (e.g., *Lead Content Trust & Safety Manager*) to ground the language in standard industry terminology.

### 2. Explicit News Exception Rule
Mandate the exact condition for news footage:
* Real-world violent/conflict footage documented as news reporting must be labeled `age_restricted` (NOT `removed`).
* Hard requirements: Must contain **no explicit gore** and **no praise, glorification, or incitement of violence**.

### 3. Benchmark Clip Grounding
Instruct the model to cite **YT-CLIP-0002** (Ana's live protest clip) as the primary case study for the News Exception Rule. Grounding rules in specific clips prevents hallucination or misinterpretation during automated review.

### 4. Direct Structural Scope
Require a 3-part layout:
* Section 1: Policy Overview & News Exception (incorporating YT-CLIP-0002)
* Section 2: Comprehensive Label Definitions (`Keep`, `Age-Restrict`, `Remove`)
* Section 3: Decision Matrix / Summary Table

---

## Effective Prompt Template

```text
Act as a Lead Content Trust & Safety Manager. Based on our moderation dataset, write a short, clear Content Moderation Policy Document defining our video labeling rules.

You must explicitly include our News & Public Interest Exception Rule:
- The News Exception Rule: Real-world violent or conflict footage documented as legitimate news reporting must be age_restricted, NOT removed, provided it contains no explicit gore and no praise, glorification, or incitement of violence.
- Benchmark Example: Cite YT-CLIP-0002 (Ana's live rally/protest footage showing police dispersal and a brief injury) as the foundational case study for this rule.

Structure the document into three concise sections:
1. Policy Overview & The News Exception Rule (incorporating the criteria above and YT-CLIP-0002).
2. Label Definitions (Keep, Age-Restrict, Remove):
  - Keep: Standard non-harmful content (e.g., cartoon gaming, historical reenactments, routine firearm care).
  - Age-Restrict: Sensitive news/protests (under the News Exception) and clinical/educational training (e.g., medical manikins).
  - Remove: Direct actionable harm, weapon assembly/DIY explosives, and extremist recruitment/calls to arms.
3. Quick-Reference Decision Matrix: A summary table comparing the three labels across Context, Violence Level, and Action Taken.
```
