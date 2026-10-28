# Kill Switch Audit

Provider

Current state: The product relies on a primary external AI/model provider for core AI capabilities.

Risk level: Medium

48-hour action: Identify which capabilities depend directly on the provider and which could continue if the provider became unavailable.

Abstraction

Current state: Some application capabilities are separated from the underlying AI provider

Risk level: Medium

48-hour action: Map provider-specific dependencies and assess the effort required to substitute an alternative model or provider.

Routing

Current state: The product does not currently rely on active routing across multiple AI providers or models.

Risk level: Medium/High

48-hour action: Identify viable alternative models/providers and assess whether the same medical search and answer requests could be routed to them.

Eval

Current state: Quality is assessed through testing and user feedback, with an opportunity to establish a more systematic evaluation framework using representative medical queries and defined scoring criteria.

Risk level: Medium

48-hour action: Establish a provider-independent evaluation set that can compare output quality consistently across different models or providers.

Portability Score: 2.5/5

The product has some portable components, but changing the underlying AI provider could currently require technical changes and additional quality validation.

If the primary vendor doubles pricing tomorrow:
 Evaluate alternative providers against the same medical search use cases, quality criteria and evaluation dataset before deciding whether to switch.

If the primary vendor ships a competing product:
 Differentiate through the specialist medical context surrounding the AI rather than the underlying model itself, including domain-specific content, workflows, governance, evaluation criteria and learning from real-world usage.

The strategic principle: retain control of the medical context, data, evaluation framework and product learning, so the underlying AI technology can change without losing the product's core value.
