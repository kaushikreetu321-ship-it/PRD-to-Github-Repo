# PRD: Reduce Cart Abandonment on Amazon

**Document status:** Draft\
**Product:** Amazon online shopping app\
**Feature area:** Cart and checkout experience\
**Author:** Product case study\
**Version:** 1.0

------------------------------------------------------------------------

## 1. Problem Statement

Users who add products to their shopping carts often leave the shopping
journey without completing their purchases. This creates a gap between
purchase intent and actual conversions, resulting in potential revenue
loss for the business and a disrupted shopping experience for users.

The specific reasons for abandonment should be validated through product
analytics and user research before finalizing the solution.

## 2. Goals and Non-Goals

### Goals

1.  Increase revenue by helping more users complete their purchases.
2.  Increase customer confidence and trust when making the final
    purchase.
3.  Improve the conversion rate from adding to cart to completing a
    purchase.
4.  Reduce cart abandonment by making the buying journey easier.

### Non-Goals

1.  Build a new shopping application or selling platform.
2.  Force users to buy alternative products instead of their chosen
    products.
3.  Focus only on new customers while ignoring existing customers.

## 3. Success Metrics

### North Star and Business Outcome

-   **North Star candidate:** Cart-to-purchase conversion rate --- the
    percentage of shopping-cart users who complete an order.
-   **Supporting business outcome:** Increase completed orders and
    revenue month over month.

*Measurement note: Revenue is an important business outcome, but it can
be affected by seasonality, traffic, pricing, and average order value.
Track it alongside conversion rather than assuming the feature alone
caused any increase.*

### L1 --- Supporting Metrics

1.  **Number of completed orders:** Count of successfully placed orders
    in the measurement period.
2.  **Cart-to-purchase conversion rate:** Percentage of eligible carts
    that result in a completed order within a defined attribution
    window.
3.  **Orders per customer:** Average number of completed orders per
    customer during the measurement period.

### Counter Metrics

1.  **Cart abandonment rate:** Percentage of eligible carts that do not
    result in a completed order within the defined attribution window.
2.  **D30 customer inactivity rate:** Percentage of customers active in
    the defined starting cohort who have no qualifying activity during
    the following 30 days. Define qualifying activity before launch.
3.  **Checkout error rate:** Percentage of checkout attempts that
    encounter an error.

### Measurement Requirements

-   Define the eligible cart, conversion event, and attribution window
    before establishing a baseline.
-   Record a baseline before rollout and compare results by customer
    cohort and device where appropriate.
-   Use an experiment or another suitable evaluation method to estimate
    whether the changes caused an improvement.
-   Monitor counter metrics to ensure conversion gains do not come at
    the expense of reliability or customer experience.

## 4. User Personas

These are **working hypotheses for a case study**, not
research-validated customer profiles. Validate them with interviews and
product data.

### Primary Persona --- Aanya, the Careful Comparator

**Life with the product:** "I compare options, add items, then hesitate
before paying."

#### Demographics

-   **Age:** 25--34
-   **Location:** Delhi NCR
-   **Occupation:** Early-career analyst
-   **Income band:** ₹5--10 lakh per year
-   **Household:** Shares household expenses
-   **Digital literacy:** High

#### Psychographic

-   **Pains**
    -   ⚠️ Unexpected fees appear late in checkout.
    -   ⚠️ Product quality or seller reliability feels uncertain.
    -   ⚠️ Delivery estimates may be unclear.
-   **Gains**
    -   ✅ See the full price before checkout.
    -   ✅ Trust the delivery date shown.
    -   ✅ Understand the return window before paying.
-   **Motivations:** Find good value without wasting time.
-   **Values:** Transparency, convenience, and reliability.
-   **Fears:** Paying more than expected or receiving an unsuitable
    product.

#### Tech Proficiency

-   Uses an Android phone and a Windows laptop.
-   Shops through mobile apps and web browsers.
-   Uses Instagram and YouTube regularly.
-   Switches between Wi-Fi and mobile data.
-   Benefits from readable text and a clear checkout flow.

#### Product-Specific

-   **Current alternatives:** Compare listings, reviews, prices, and
    delivery estimates.
-   **Usage scenarios and frequency:** Browses and shops weekly, often
    in the evening.
-   **Purchase drivers:** Price clarity, trustworthy reviews, and
    reliable delivery.
-   **Satisfaction level:** Mixed when costs or delivery details feel
    uncertain.
-   **Switching barriers:** Saved addresses, order history, and
    membership benefits.
-   **Success metric they care about:** Complete the intended purchase
    with confidence.

#### What they want

-   See the full cost before starting payment.
-   Know the expected delivery date before paying.
-   Understand return options without searching multiple pages.
-   Finish checkout without unexpected changes.

### Secondary Persona --- Rahul, the Time-Constrained Reorderer

**Life with the product:** "I reorder essentials quickly but abandon
checkout when it feels slow."

#### Demographics

-   **Age:** 35--44
-   **Location:** Pune
-   **Occupation:** Small-business owner
-   **Income band:** ₹10--20 lakh per year
-   **Household:** Lives with a partner and child
-   **Digital literacy:** Moderate to high

#### Psychographic

-   **Pains**
    -   ⚠️ Re-entering information wastes time.
    -   ⚠️ Stock or delivery uncertainty interrupts planning.
    -   ⚠️ Too many checkout steps feel frustrating.
-   **Gains**
    -   ✅ Reorder essentials quickly.
    -   ✅ See dependable delivery information.
    -   ✅ Recover smoothly from a failed payment.
-   **Motivations:** Complete routine purchases efficiently.
-   **Values:** Reliability, speed, and convenience.
-   **Fears:** Essential items arriving later than expected.

#### Tech Proficiency

-   Uses an Android phone and a work laptop.
-   Uses Android and Windows devices.
-   Shops online several times a week.
-   Uses WhatsApp and YouTube regularly.
-   Uses Wi-Fi and mobile data depending on location.

#### Product-Specific

-   **Current alternatives:** Saved lists, order history, and
    repeat-purchase options.
-   **Usage scenarios and frequency:** Reorders household or business
    essentials 2--4 times weekly.
-   **Purchase drivers:** Availability, speed, and reliable delivery.
-   **Satisfaction level:** Good when checkout and delivery are
    dependable.
-   **Switching barriers:** Saved payment methods, addresses, and order
    history.
-   **Success metric they care about:** Complete a repeat order with
    minimal effort.

#### What they want

-   Reorder familiar items in fewer steps.
-   Avoid entering the same details repeatedly.
-   Know whether items are available and when they will arrive.
-   Retry a failed payment without rebuilding the order.

## 5. Opportunity Areas and Proposed Concepts

These concepts are hypotheses to validate, not confirmed competitor
capabilities or committed scope.

### P0 --- True Total

Show one clear order total in the cart, including applicable item costs,
delivery fees, taxes, and discounts where available.

**Problem addressed:** Customers may hesitate when the total cost is
unclear or changes late.

**Acceptance direction:** - The cart clearly displays the current
estimated total and its components. - Applicable fees and discounts are
explained before the customer commits to payment. - If the total
changes, the updated amount and reason are shown clearly.

### P1 --- Locked Delivery Promise

Show the expected delivery date and applicable return window in the
cart, and keep information consistent through checkout unless
circumstances change.

**Problem addressed:** Uncertainty about delivery or returns may reduce
purchase confidence.

**Acceptance direction:** - The estimated delivery date and return
information are visible before payment. - Delivery information remains
consistent through checkout when the underlying promise has not
changed. - If an estimate changes, the customer is informed before
placing the order.

### P2 --- Retry-Safe Payment

If a supported payment attempt fails, preserve the cart and allow the
customer to retry or choose another payment method without starting
over.

**Problem addressed:** A failed payment can interrupt the purchase
journey.

**Acceptance direction:** - The cart remains available after a payment
failure. - The customer receives a clear, actionable failure message. -
The customer can retry or select another supported payment method. -
Retry handling prevents duplicate orders and duplicate charges.

## 6. Prioritization --- RICE-Inspired

The ratings below are initial planning assumptions. Validate them with
evidence before committing to delivery.

  --------------------------------------------------------------------------
  Opportunity   Reach       Impact      Confidence   Effort      Initial
                                                                 Priority
  ------------- ----------- ----------- ------------ ----------- -----------
  True Total    Medium      High        Medium       Medium      P0

  Locked        High        High        High         Medium      P1
  Delivery                                                       
  Promise                                                        

  Retry-Safe    Medium      Medium      High         High        P2
  Payment                                                        
  --------------------------------------------------------------------------

**Prioritization note:** This is a qualitative, RICE-inspired ranking,
not a calculated RICE score. A full RICE calculation requires numeric
reach, impact, confidence, and effort estimates using a consistent
scale.

## 7. Functional Requirements

1.  A customer with items in the cart can view the current estimated
    order total and its components.
2.  The cart displays the expected delivery date and applicable return
    information when available.
3.  Checkout presents consistent price and delivery information unless
    the underlying details change.
4.  If price or delivery information changes, the customer sees the
    update before placing the order.
5.  If payment fails, the cart remains intact and the customer can retry
    or choose another supported payment method.
6.  Payment failure messages explain the issue and provide a clear next
    step where possible.
7.  Payment retry flows prevent duplicate orders and duplicate charges.
8.  The experience supports both new and existing customers.

## 8. Non-Functional Requirements

### Performance

-   Cart total and delivery date load within 2 seconds under the agreed
    test conditions.
-   Payment retry starts within 3 seconds under the agreed test
    conditions.

### Quality

-   The displayed delivery promise is met in at least 95% of eligible
    orders, measured against a defined delivery-promise metric.
-   Checkout errors should not require customers to re-enter information
    unnecessarily.

### Reliability

-   Cart details remain saved after app closure, network failure, or
    payment failure, subject to applicable session and account rules.
-   Payment retries do not create duplicate orders or charges.

### Security

-   Only authorized services and users can access payment and address
    data.
-   Sensitive payment information is handled according to applicable
    security and compliance requirements.

### Transparency

-   Clearly show applicable fees, discounts, delivery estimates, and
    payment failure reasons.
-   Explain material changes to the total or delivery estimate before
    order placement.

### Usability

-   Customers can complete checkout with minimal unnecessary steps.
-   Customers can retry a failed payment without rebuilding the cart.

## 9. Assumptions and Open Questions

### Assumptions

-   The existing Amazon shopping experience is the product surface; no
    new shopping app is being built.
-   Cart abandonment may be related to price uncertainty, delivery
    uncertainty, checkout friction, or payment failure. These causes
    have not yet been validated.
-   The personas are illustrative and should be tested against actual
    customer research.
-   The priority order is preliminary and may change after impact and
    effort estimates.

### Open Questions

1.  What is the current cart-to-purchase conversion rate and abandonment
    rate?
2.  At which checkout step do customers most often leave?
3.  How often do payment failures lead to an abandoned cart?
4.  Which fees or delivery details are currently unclear to customers?
5.  What attribution window should define a cart as abandoned?
6.  Which customer and device segments experience the greatest friction?
7.  What experiment design will distinguish feature impact from
    seasonality or other changes?

## 10. Dependencies and Risks

-   Price, discount, fee, inventory, delivery, and returns data must be
    accurate and timely.
-   Payment retry behavior must be coordinated with payment processing
    and order-management systems.
-   Delivery estimates can change due to inventory, location, or
    logistics constraints.
-   Showing additional details must not make the cart harder to scan.
-   The team must protect payment and address information and avoid
    duplicate transactions.

## 11. Prototype and Portfolio Notes

-   **Mock-up tool:** https://stitch.withgoogle.com/
-   **Prototype status:** Tentative; create and validate after
    requirements are reviewed.
-   **Portfolio goal:** Use this case study to demonstrate problem
    framing, prioritization, metrics, requirements, and product
    thinking.
-   **Brand note:** This is an independent portfolio case study and does
    not imply affiliation with or endorsement by Amazon.

## 12. Suggested Repository Structure

``` text
cart-abandonment-prd/
├── README.md
├── PRD.md
├── docs/
│   ├── personas.md
│   ├── metrics.md
│   └── prioritization.md
├── prototypes/
│   └── README.md
└── research/
    └── README.md
```

## 13. Definition of Success

The initiative will be considered successful when an appropriately
designed evaluation shows an improvement in cart-to-purchase conversion,
with no unacceptable deterioration in checkout errors, customer
inactivity, payment reliability, or customer experience. Revenue and
completed orders should be tracked as supporting business outcomes.
