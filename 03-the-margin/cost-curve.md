# Cost Curve & Pricing Strategy

Leader: Semantic search / MI retrieval (this is the current tools core capability. It understands the question and retrieves the most relevant approved medical information)

Filler: Generated answers (Builds on semantic search by turning the retrieved information into a concise, grounded answer, making it quicker and easier for users to get what they need)

Killer: Agentic workflows / actions (Moves beyond answering questions to taking actions, such as triggering downstream workflows or creating cases in other systems.)

% users using Killer: Not yet known / not yet measurable (The products agentic capabilities are not yet established enough to determine a meaningful usage percentage)

Decision: Add-on initially (workflows are likely to be more computationally intensive and relevant to specific use cases rather than every tool interaction. If usage eventually exceeds the 70% threshold, bundling could be reconsidered.)

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | $3.00 |Cost of semantic retrieval and generating grounded answers from approved MI content. |
| Inference (cascading/triage) |$0.50 |Lower-cost processing used to classify questions, select content or decide whether the primary model is required. |
| Infrastructure | $2.00|Hosting, APIs, monitoring and supporting services needed to operate AIMI. |
| Data/storage |$0.50 | Storage and processing of approved documents, embeddings, conversation data and logs.|
| Human-in-the-loop |$4.00 |Sample reviews, quality monitoring and investigation of incorrect or low-quality responses. |
| **Total AI COGS** |$10.00 |Illustrative monthly cost per active user. Human oversight is the largest cost until monitoring becomes more automated and risk-based. |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

Triage model: Small/mid model for straightforward questions, classification, retrieval and lower-complexity generation.

Frontier model: Most capable model reserved for complex, ambiguous or higher-risk MI questions requiring deeper reasoning.

Routing rule: Route simple questions to small models, standard MI questions to mid-tier models, and escalate complex or ambiguous questions to the frontier model.

Expected cascade ratio: 40% small / 40% mid / 20% frontier.

## Pricing Model

Current pricing: Internal product with no direct per-user charge.

Proposed AI pricing: Core semantic search and generated answers bundled; higher-cost agentic workflows treated separately.

Model: Hybrid. Core access plus usage/outcome-based charging for high-cost agentic functionality.

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x |AI COGS increases significantly, reducing margin | Route more appropriate requests to small/mid models, optimise prompts/context and use caching where appropriate|
| Heaviest segment doubles |Heavy users generate disproportionately higher AI COGS | Monitor cost per successful MI outcome; consider usage-based pricing/limits for very high-cost functionality|
| Model provider raises prices 50% | Blended cost/request rises and margin falls| Reduce frontier-model dependency and maintain ability to route suitable workloads to alternative/lower-cost models|

## Board One-Pager
Before (traditional SaaS):
The tool  primarily provides semantic search. Cost per additional interaction is relatively low and predictable.

After (AI-enabled):
The tool adds generated answers, conversational capabilities and potentially agentic workflows. This increases user value but introduces greater variable inference costs that grow with usage.

Net margin shift:
Margin percentage is likely to decrease as AI COGS increases, but this can still be economically attractive if AI creates enough additional value. Model cascading protects margin by reserving expensive frontier inference for the requests that genuinely need it.
