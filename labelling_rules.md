# Content Moderation Policy Document: Video Labeling Rules

## 1. POLICY OVERVIEW & THE NEWS EXCEPTION RULE

This policy establishes standard protocols for evaluating video content to balance public interest, freedom of expression, and community safety.

### The News & Public Interest Exception Rule
Real-world violent or conflict footage documented as legitimate news reporting must be labeled **AGE_RESTRICT**, NOT **REMOVE**, provided it satisfies three criteria:
1. **Legitimate Journalistic Context:** Documents ongoing news events, public protests, or law enforcement actions.
2. **No Explicit Gore:** Displays no gratuitous, extreme, or severe graphic injuries.
3. **No Incitement or Glorification:** Does not praise, encourage, or glorify violence, nor call viewers to commit violent acts.

### Benchmark Case Study (YT-CLIP-0002)
* **Title:** "Harbor Street rally dispersed by police - live"
* **Category:** `news_reporting` (`is_news: true`)
* **Decision:** `age_restrict`
* **Rationale:** Ana's live rally reporting shows a crowd confrontation, a thrown bottle, and a brief injury on the pavement. Because it represents legitimate live reporting without explicit gore, glorification, or incitement, it is age-gated to protect teen viewers while preserving public interest news coverage.

---

## 2. LABEL DEFINITIONS

### KEEP
* **Coverage:** Standard, non-harmful content presenting no real-world threat or severe policy violations.
* **Eligible Content:**
  * Cartoon or fantasy video game combat with no real people (*YT-CLIP-0001*, *YT-CLIP-0009*)
  * Historical documentaries and reenactments without gratuitous gore (*YT-CLIP-0004*)
  * Standard combat sports and amateur sparring without severe injury (*YT-CLIP-0006*)
  * Routine cleaning, maintenance, or safe handling of legal firearms (*YT-CLIP-0007*)

### AGE_RESTRICT
* **Coverage:** Sensitive, graphic, or intense material that serves a legitimate educational, medical, or news purpose, but is unsuitable for younger viewers.
* **Eligible Content:**
  * Live news and protest coverage meeting the News Exception Rule (*YT-CLIP-0002*)
  * Clinical, first-responder, or medical training footage using manikins or simulations (*YT-CLIP-0003*)

### REMOVE
* **Coverage:** Severe policy-violating content posing direct actionable real-world harm, illegal activity, or severe risk to public safety.
* **Mandated Action:** Immediate removal from the platform.
* **Non-Negotiable Violations:**
  * **Extremist Recruitment / Armed Groups:** Videos urging viewers to take up arms, join armed groups, or commit violence—even if framed with news-like titles (*YT-CLIP-0005*)
  * **Actionable Weapon Assembly & Explosives:** Step-by-step instructions or DIY guides for constructing weapons or explosive devices without safety or legal context (*YT-CLIP-0008*)

---

## 3. QUICK-REFERENCE DECISION SUMMARY

### KEEP
* **Purpose:** Entertainment, history, sports, or legal routine care
* **Violence Level:** None or simulated/fantasy combat; standard sports contact
* **Action:** Allowed for all audiences
* **Examples:** YT-CLIP-0001, 0004, 0006, 0007, 0009

### AGE_RESTRICT
* **Purpose:** Legitimate news reporting, public interest, or medical/EMS education
* **Violence Level:** Real-world conflict, simulated trauma, or brief non-gory injury
* **Action:** Gated behind age warning (18+ only)
* **Examples:** YT-CLIP-0002, 0003

### REMOVE
* **Purpose:** Extremist recruitment, calls to arms, or dangerous weapon builds
* **Violence Level:** Direct actionable harm, explosive fabrication, or violent incitement
* **Action:** Taken down immediately
* **Examples:** YT-CLIP-0005, 0008
