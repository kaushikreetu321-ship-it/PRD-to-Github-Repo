# Project Plan

This plan turns the draft PRD and existing concepts into a portfolio-ready case study. The work should remain hypothesis-led until the underlying customer problem is validated. Priorities below follow the PRD's qualitative order and are not calculated RICE scores.

## 1. Validate the problem and baseline

**Goal:** Determine whether price uncertainty, delivery uncertainty, checkout friction, or payment failure materially contributes to cart abandonment.

- Define eligible cart, checkout attempt, completed-order, abandonment, and attribution-window events.
- Review funnel and payment-error data by journey step, customer cohort, and device where feasible.
- Conduct customer research to test the personas and understand how shoppers interpret totals, delivery promises, returns, and failure messages.
- Record baseline conversion and guardrail metrics before evaluating changes.
- Document the evidence, limitations, and any revised problem statement.

**Exit checks**

- Problem causes and affected segments are supported by research or clearly marked as unverified.
- Metric definitions and baseline period are documented.
- The team has an evaluation approach appropriate to rollout and traffic.

## 2. Refine requirements and interaction flows

**Goal:** Convert the three opportunity hypotheses into testable, consistent behaviors across web and mobile.

- Detail when fees, taxes, discounts, delivery dates, and return information are known and displayed.
- Define behavior and customer messaging when a total or delivery estimate changes.
- Map payment success, decline, timeout, retry, alternate-method, and interrupted-session paths.
- Define duplicate-order and duplicate-charge safeguards with payment and order-management owners.
- Review accessibility, readable pricing, error recovery, and minimal-step requirements.

**Exit checks**

- Requirements cover the eight functional requirements and relevant non-functional requirements in the PRD.
- Edge cases and data/system dependencies are understood by the responsible teams.
- Price and delivery information stay consistent across cart, checkout, and confirmation unless source data changes.

## 3. Prioritize and prototype the concepts

**Goal:** Make the proposal understandable and testable without presenting static mockups as a working commerce product.

1. **P0 — True Total:** Show the estimated total and itemized applicable charges, discounts, and explanations.
2. **P1 — Locked Delivery Promise:** Surface delivery and return expectations early and communicate meaningful changes.
3. **P2 — Retry-Safe Payment:** Preserve cart context and provide clear, safe recovery after payment failure.

- Keep web and mobile content, calculations, terminology, and states aligned.
- Use the current BharatCart-branded static screens as concept artifacts; document the brand distinction from the Amazon context.
- Mark unavailable, changed, or conditional data honestly rather than implying guarantees the underlying systems cannot support.

**Exit checks**

- Each concept addresses an identified user need and has a testable requirement.
- The key happy paths and material exception states are represented on both form factors.
- Prototype limitations and assumptions are explicit.

## 4. Test usability and iterate

**Goal:** Check comprehension and recovery before implementation decisions.

- Test whether shoppers can identify the total, its components, delivery expectations, and return information.
- Ask participants to respond to a changed delivery date or total and to recover from a failed payment.
- Observe task completion, misunderstandings, unnecessary effort, and trust-related concerns.
- Iterate the design and requirements based on observed evidence; do not treat stated preference alone as impact evidence.

**Exit checks**

- Critical misunderstandings and blockers have been resolved or documented.
- Shoppers can identify material changes and understand a next step after payment failure.
- The design remains scannable and usable on web and mobile.

## 5. Prepare delivery and measurement

**Goal:** Ensure the experience is feasible, safe, and measurable before any release.

- Confirm data owners and freshness for price, fees, discounts, inventory, delivery, and returns.
- Specify payment retry idempotency and order/charge reconciliation behavior.
- Define performance test conditions for the PRD's proposed two-second information-load and three-second retry-start targets.
- Define eligibility and measurement for the proposed 95% delivery-promise attainment target.
- Finalize experiment or rollout design, guardrails, monitoring, and rollback criteria.

**Exit checks**

- Technical, security, privacy, operations, and analytics dependencies have owners and acceptance criteria.
- Baseline, success metrics, guardrails, and rollout decision rules are agreed before launch.
- No production claim is made from static prototype behavior.

## 6. Publish the portfolio case study

**Goal:** Present the reasoning and evidence clearly in GitHub.

- Explain the problem, evidence status, users, scope, prioritization, and design decisions.
- Link the PRD, context, plan, web/mobile HTML prototypes, image previews, and design systems.
- Distinguish measured findings from assumptions and proposed outcomes.
- State that BharatCart is the fictional prototype brand and the case study is not affiliated with Amazon.

**Exit checks**

- Repository landing page clearly explains the project and links to all relevant artifacts.
- Every outcome claim is supported by evidence or explicitly labeled as a hypothesis/proposal.

## Current status

The draft PRD, initial web/mobile static prototype screens, and design-system documents already exist. The documents in this repository organize that starting point; they do not imply that research validation, usability testing, implementation, or impact measurement has been completed.
