# Project Context

## Project

**Working title:** Checkout Clarity & Trust  
**Product context:** An existing Indian e-commerce shopping experience, as described in the source PRD for Amazon.  
**Portfolio prototype brand:** BharatCart, a fictional concept name used by the existing prototype screens. This is an independent case study, not an Amazon product or affiliation.

## Problem framing

People with purchase intent may abandon a cart before placing an order. The PRD proposes price uncertainty, unclear delivery or return expectations, and payment friction as possible contributors. These are hypotheses: the available documents do not include validated customer research, behavioral analytics, or a measured baseline.

The opportunity is to help shoppers understand what they will pay, when an order is expected, and what they can do if payment fails—without adding unnecessary checkout effort.

## Intended users

The PRD defines two illustrative personas:

- **Aanya, the Careful Comparator:** Values a complete price, trustworthy delivery expectations, and easily understood return information.
- **Rahul, the Time-Constrained Reorderer:** Values a quick repeat purchase, dependable availability and delivery, and recovery from payment problems without rebuilding the order.

These personas are working hypotheses, not research-validated profiles. Validate or revise them with customer research and product data before using them as a basis for launch decisions.

## Product outcomes

- Help more eligible cart sessions result in completed orders.
- Increase confidence by showing applicable cost, delivery, and return information before purchase.
- Reduce avoidable checkout friction while preserving a reliable recovery path.

The **north-star candidate** is cart-to-purchase conversion rate. Define eligible carts, the conversion event, and the attribution window before establishing a baseline. Track completed orders and orders per customer as supporting metrics; monitor cart abandonment, checkout errors, and D30 inactivity as guardrails. Treat revenue as a business outcome influenced by other factors, not proof of feature impact on its own.

## Proposed solution scope

1. **True Total (P0):** Present the current estimated order total and its applicable components, including item costs, fees, taxes, and discounts. Explain changes before order placement.
2. **Locked Delivery Promise (P1):** Show the estimated delivery date and return information when available. Keep the promise consistent through checkout unless its underlying details change; explain changes before order placement.
3. **Retry-Safe Payment (P2):** After a supported payment failure, preserve cart details and allow a clear retry or alternate payment method. Prevent duplicate orders and charges.

The portfolio artifacts currently include static cart, payment selection, payment failure/retry, and order confirmation concepts for web and mobile. See [README.md](README.md) for direct links.

## Out of scope

- Building a new shopping platform or production checkout service.
- Forcing customers to switch from their selected products.
- Implementing real payments, account/address access, inventory, delivery estimation, or order management.
- Claiming product impact before conducting an appropriate evaluation.

## Product and design constraints

- Cost, discounts, fees, inventory, delivery, and returns data must be accurate and timely.
- Material price or delivery changes must be clear before the customer commits.
- Payment recovery must be coordinated with payment and order-management systems to avoid duplicate transactions.
- Additional reassurance and disclosure must not make the cart harder to scan or checkout unnecessarily long.
- Payment and address information must be handled only by authorized services and users, in accordance with applicable security and compliance requirements.
- The PRD proposes cart total and delivery information within two seconds and payment retry initiation within three seconds under agreed test conditions; those conditions need to be defined.
- The PRD proposes delivery-promise attainment of at least 95% of eligible orders; the metric and eligibility rules need to be specified and operationally supported.

## Assumptions, dependencies, and risks

- The actual causes and distribution of cart abandonment are unknown and must be verified before solution commitment.
- The personas, qualitative priority ratings, and proposed concepts are preliminary.
- The experience depends on dependable pricing, discount, fee, inventory, delivery, and return information.
- Delivery estimates can change because of location, inventory, and logistics.
- Payment failure and retry behavior depends on the payment processor and order-management system.
- More details can increase cognitive load if hierarchy and timing are not handled carefully.

## Open questions to resolve

- What are current cart-to-purchase conversion and abandonment rates, and how are they defined?
- Where in the journey do shoppers leave, and how often do payment failures lead to abandonment?
- Which segments, devices, fees, or delivery details experience the most friction?
- What attribution window and experiment design will support a credible impact estimate?
- Which conditions, systems, and eligibility rules underlie delivery and payment performance targets?

## Source of truth

The requirements and assumptions originate in [PRD.md](PRD.md). Existing visual direction is in the web and mobile `DESIGN.md` files under `Prototype Screens`. Where the source PRD refers to Amazon and prototype screens refer to BharatCart, interpret Amazon as the product context and BharatCart as the fictional presentation brand for this independent case study.
