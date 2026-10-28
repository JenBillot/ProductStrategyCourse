# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.
> The four loops below are the M2 starting point - adapt if your product has 2 or 6 loops instead of 4.

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | __/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | __/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | __/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | __/5 |

### Correction Loop - 2/5
**What you capture today:**
We have user feedback, testing feedback and real-world examples of poor search behaviour, such as relevant documents ranking incorrectly or queries not retrieving the expected content. However, these signals are largely identified and investigated manually.

**How it compounds:**
Currently, not strongly. The opportunity is to turn real-world failures, successful searches and human judgements into a maintained evaluation dataset. Changes to search or generated answers could then be tested against that dataset before release and monitored after release.

### Preference Loop - 1/5
**What you capture today:** 
The tool does not currently appear to build a meaningful understanding of an individual user's preferences from repeated use.

**How it compounds:**
Very little today. However, I wouldn't necessarily treat this as a major weakness for the product. In the medical space, consistent, governed responses may matter more than deep individual personalisation. The stronger opportunity may be learning patterns by role, market, product or query type rather than tailoring answers to individual users which we already do 

### Domain Context Loop - 3/5
**What you capture today:**
The tool operates over specialist Medical content, with repeated usage exposing query patterns, terminology, products and information needs within that domain.

**How it compounds:**
Potentially strongly. Insights from one set of searches can help identify retrieval and answer-quality improvements that benefit similar MI queries for other product use cases. 

### Network Loop - 2/5
**What you capture today:**
More users create more searches and therefore more evidence about what people ask, where retrieval works and where it fails.

**How it compounds:**
Only weakly today because more users do not automatically make the tool better. It becomes a genuine flywheel only if those interactions are converted into quality signals, evaluation cases and product improvements that benefit subsequent users.

**Total Flywheel Score: 8/20**
**Weakest Loop:**
Preference, technically. But I wouldn't say it's the priority to fix. I would focus on the correction part 

**Fix for weakest loop:**
Build an evaluation flywheel so that we can do: 
real-world usage → identify quality signals → human evaluation → evaluation dataset → product/search improvements → measure whether quality improved → new usage data

---

## Encroachment Threat Assessment

### 1. Platform Encroachment
Attacker: Salesforce Agentforce

Vector: Native AI capabilities within salesforce could provide search and generated answers directly in the agents’ existing workflow, reducing the need for our tool as a seperate capability.

Time-to-threat: Near term

% of value at risk: ~40%

Rationale: primarily threatens one of our use cases (but doesn't replace other use cases not in Salesforce) 

### 2. Vertical Competitor
Attacker: MI Call Centre supplier 

Vector: They could provide its own search capability as part of its outsourced contact-centre service, reducing reliance on our in-house capability

Time-to-threat: Medium term

% of value at risk: ~30%

Rationale: significant exposure for the the use case that impacts them, but less direct impact on our owned use cases.

### 3. Adjacent Expansion
Attacker: In-house enterprise AI/search platforms

Vector: A broader AI platform could expand into enterprise knowledge retrieval and grounded answer generation, potentially making a dedicated Medical search capability less differentiated.

Time-to-threat: Medium–long term

% of value at risk: ~50%

Rationale: potentially broader because it could challenge the rationale for our product across multiple use cases.

---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:**
**Attack vector (target the weakest loop):**
**Weeks 1-4 - what they ship:**
**Weeks 5-8 - how they poach users:**
**Weeks 9-12 - why users don't come back:**
**Your defense:**
