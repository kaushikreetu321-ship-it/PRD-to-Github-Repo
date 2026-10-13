---
name: Bharat Checkout Trust System
colors:
  surface: '#f8f9ff'
  surface-dim: '#d5dae6'
  surface-bright: '#f8f9ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#eff4ff'
  surface-container: '#e9eefa'
  surface-container-high: '#e3e8f4'
  surface-container-highest: '#dde3ee'
  on-surface: '#161c24'
  on-surface-variant: '#554434'
  inverse-surface: '#2b3139'
  inverse-on-surface: '#ebf1fd'
  outline: '#887361'
  outline-variant: '#dbc2ad'
  surface-tint: '#8a5100'
  primary: '#8a5100'
  on-primary: '#ffffff'
  primary-container: '#ff9900'
  on-primary-container: '#653a00'
  inverse-primary: '#ffb86f'
  secondary: '#006c47'
  on-secondary: '#ffffff'
  secondary-container: '#92f7c1'
  on-secondary-container: '#00734b'
  tertiary: '#535f70'
  on-tertiary: '#ffffff'
  tertiary-container: '#a6b2c5'
  on-tertiary-container: '#394555'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#ffdcbd'
  primary-fixed-dim: '#ffb86f'
  on-primary-fixed: '#2c1600'
  on-primary-fixed-variant: '#693c00'
  secondary-fixed: '#92f7c1'
  secondary-fixed-dim: '#76daa7'
  on-secondary-fixed: '#002112'
  on-secondary-fixed-variant: '#005234'
  tertiary-fixed: '#d7e3f7'
  tertiary-fixed-dim: '#bbc7db'
  on-tertiary-fixed: '#101c2b'
  on-tertiary-fixed-variant: '#3c4858'
  background: '#f8f9ff'
  on-background: '#161c24'
  surface-variant: '#dde3ee'
typography:
  headline-xl:
    fontFamily: Inter
    fontSize: 28px
    fontWeight: '700'
    lineHeight: 36px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Inter
    fontSize: 22px
    fontWeight: '700'
    lineHeight: 28px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
  body-lg:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
  label-lg:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '600'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-md:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '500'
    lineHeight: 18px
  label-sm:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '600'
    lineHeight: 14px
    letterSpacing: 0.04em
  price-display:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 28px
  price-strike:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '400'
    lineHeight: 18px
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  gutter: 1.5rem
  margin: 2rem
  space-xs: 0.25rem
  space-sm: 0.5rem
  space-md: 1rem
  space-lg: 1.5rem
  space-xl: 2rem
---

## Brand & Style

This design system establishes a transactional checkout architecture built for Indian digital commerce. It synthesizes the operational clarity of high-velocity pan-Indian e-commerce platforms with rigorous trust heuristics, high-visibility pricing clarity, and cognitive reassurance. 

### Brand Personality & Emotional Objectives
- **Authoritative & Secure:** Instills total confidence across high-friction transactional steps (address selection, GSTIN verification, UPI/card payment, OTP hand-off) through visible bank-grade safety markers and clear step progressions.
- **Value-Forward & Transparent:** Surfaces instant calculations of savings, delivery fee waivers, bank instant discounts, and delivery timelines with zero hidden fees.
- **Tactile & Systematic:** Bridges modern minimal UI with tactile commerce conventions—tangible action buttons, clear selected states, and unmistakable affordances tailored for quick multi-lingual comprehension.

### Design Movement
The visual language operates on **Modern Enterprise Commerce with Structured Tonal Layering**. It pairs a commanding, utilitarian dark navy institutional header with an airy light-slate canvas, clean 12px structural radii, distinct high-contrast primary actions in warm saffron-amber, and deep emerald green trust signals for monetary value verification.

## Colors

The palette optimizes cognitive clarity, transaction validation, and instant price breakdown comprehension under high task loads.

### Core Functional Colors
- **Primary CTA (`#FF9900`):** Warm Saffron / Amber Orange. Reserved strictly for primary checkout advancement (e.g., "Proceed to Pay", "Use this Address", "Place Your Order"). Hover state deepens to `#E67A00`, active tap responds with `#D46B08`.
- **Trust, Savings & Success Secondary (`#0F8458`):** Deep Forest Emerald Green. Dictates all trust mechanics: delivery date assurances ("Guaranteed Delivery"), discount figures, coupon applied states, and rupee value savings. Paired with `#E8F5E9` for subtle badge backgrounds.
- **Enterprise Dark Navies (`#131921` Canvas Navy, `#232F3E` Header Slate):** Form an institutional, high-contrast anchor across checkout headers, utility ribbons, and locked navigation bars.
- **Warning & Friction Mitigator (`#FFF3E0` surface, `#B76E00` text, `#F59E0B` border):** Utilized for OTP timeout countdowns, pincode serviceability cautions, and high-value COD restriction notices.

### Neutral Layering & Borders
- **Page Foundation:** Neutral backdrop anchored between `#F3F4F6` and `#EAEDED` to detach the white foreground work surfaces.
- **Card Surfaces:** `#FFFFFF` pure white to preserve high contrast against text and form elements.
- **Structural Outlines:** Subtle slate borders (`#E2E8F0` for interior dividers, `#D5D9D9` for card containers and interactive form fields).
- **Text Tiers:** `#0F1111` for primary headings and dense labels, `#565959` for secondary helper copy and metadata, and `#007185` for contextual actions and address management links.

## Typography

The type system uses **Inter** throughout all viewports to provide exact typographic rendering of numerical transaction values, banking codes, alphanumeric GSTIN formats, and the Indian Rupee symbol (`₹`).

### Numerical & Rupee Styling Heuristics
- **Indian Rupee Formatting:** The currency glyph `₹` precedes numbers with zero space (`₹1,499`). It shares the exact font weight and color token of the adjacent numerical string.
- **Explicit Strike-Throughs:** Original maximum retail prices (MRP) use `price-strike` with `text-decoration: line-through` in `#565959`, immediately accompanied by the net effective price and an emerald green savings delta tag (e.g., `Save ₹400 (21%)`).
- **Tabular Figures:** All monetary readouts within checkout tables, shipping line items, and the order summary module enforce `font-variant-numeric: tabular-nums` to guarantee vertical decimal and symbol alignment across varying payment totals.

## Layout & Spacing

The layout is optimized for focused, distraction-free desktop purchasing. Navigation is enclosed—external header links, global navigation menus, and category search bars are stripped to isolate the completion funnel.

### Desktop Grid Architecture
- **Max Canvas Width:** `1200px` centered horizontally.
- **Checkout Asymmetric Split:** 
  - **Left Primary Column (Fluid / ~780px max):** Spans 8 columns of the 12-column grid. Houses sequential accordion steps: Delivery Address, Delivery Options, and Payment Methods.
  - **Right Sidebar Column (Fixed 360px):** Spans 4 columns. Holds the sticky order summary card, instant discount redemption input, and guaranteed security seals.
- **Gutters & Margins:** Outer margin set to `margin` (`2rem`), cross-column gutter locked at `gutter` (`1.5rem`).

### Rhythm & Vertical Flow
Component interiors use systematic multi-tier padding:
- Card internal padding is locked to `space-lg` (`1.5rem`).
- Tight transactional rows (breakdowns of taxes, shipping fees, product sub-items) adhere to `space-sm` (`0.5rem`) to `space-md` (`1rem`) vertical separation.
- Sequential checkout blocks maintain a consistent `space-lg` (`1.5rem`) vertical margin to avoid visual cramping while preserving scanning flow.

## Elevation & Depth

This design system avoids heavy shadows, using crisp, structural containment with subtle ambient depth to replicate trustworthy enterprise software.

### Depth Hierarchy
- **Canvas Base (`#EAEDED` / `#F3F4F6`):** The non-elevated foundation on which content rests.
- **Step Containers & Cards (`#FFFFFF`):** Outlined with a fine 1px border (`#D5D9D9`) combined with an ultra-diffused elevation: `box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.06), 0 1px 2px -1px rgba(0, 0, 0, 0.04)`.
- **Active / Expanded Checkout Step:** Maintains the base white surface, but drops the border tone to `#0F1111` or `#2563EB` and increases focus depth: `box-shadow: 0 4px 12px -2px rgba(19, 25, 33, 0.08)`.
- **Sticky Order Summary:** Retains `box-shadow: 0 4px 16px -4px rgba(0, 0, 0, 0.1), 0 2px 4px -2px rgba(0, 0, 0, 0.05)` to signal persistent grounding as the user scrolls through the multi-step form.
- **Interactive Hover Layers:** Clickable address selection tiles transition from a neutral border (`#D5D9D9`) to an active saffron ring (`2px solid #FF9900`) accompanied by an ambient `#FFF8E7` tint.

## Shapes

The design system maintains a balanced, contemporary corner geometry that avoids overly playful curves while ditching dated hard angles.

### Geometric Rules
- **Structural Cards & Panels:** Enforce a uniform radius of `12px` (matching `roundedness: 2` at the card layer), softening dense financial information.
- **Buttons & Form Inputs:** Set to an `8px` corner radius to provide familiar, tactile click targets.
- **Status Tags & Badges:** Use a compact `4px` to `6px` radius for high-density information display (e.g., "FREE Delivery", "Bank Offer Applied").
- **Payment Method Icon Enclosures:** Standardized to a `6px` radius inside a `1px` border frame to unify heterogeneous third-party logos (UPI apps, RuPay, Visa, Mastercard).

## Components

### 1. Primary & Secondary Buttons
- **Primary CTA ("Place Your Order" / "Proceed to Payment"):** Surface `#FF9900`, text `#0F1111` (high-contrast black), font weight 600, height 48px, radius 8px. Hover shifts to `#E67A00`. Pressed shifts to `#D46B08`. Includes active micro-transition on transform (`translateY(0.5px)`).
- **Secondary Action Button ("Add New Address" / "Change"):** Transparent background, 1px border in `#D5D9D9`, text `#0F1111`. Hover fills with `#F7FAFA` and deepens border to `#A6A6A6`.

### 2. Multi-Step Checkout Accordion
- **Completed Steps:** White background, thin border, green checkmark icon in `#0F8458`, muted title, secondary recap string (e.g., "Delivering to Rahul Sharma, 560034"), and a right-aligned secondary text link ("Change").
- **Active Step:** White background, highlighted index indicator (dark navy circle with bold white numeral), full form controls exposed.
- **Locked / Future Steps:** `#FAFAFA` background, `#888888` text, inactive index circle, collapsed contents.

### 3. Selection Cards (Delivery Address & Shipping Tiers)
- Unselected cards feature `#FFFFFF` background, 1px `#D5D9D9` border.
- Selected cards feature `#FFFDF7` subtle warm background, 2px border in `#FF9900`, with an internal bold radio marker.
- Tag integration: Small `#E2E8F0` pill tags denoting address category: `HOME`, `WORK`, `DEFAULT`.

### 4. Input Fields & UPI / Card Selectors
- Standard inputs: 40px height, 8px radius, `#FFFFFF` background, 1px `#D5D9D9` border. Focus state triggers `border-color: #E77600` and an amber-tinted focus glow (`box-shadow: 0 0 0 3px rgba(255, 153, 0, 0.25)`).
- UPI Collection Module: Structured entry field for VPA (e.g., `username@oksbi`) paired with instant verification badge ("Verified Name: Rahul S.").

### 5. Chips, Savings Badges & Trust Banners
- **Discount & Savings Chip:** `#E8F5E9` background, `#0F8458` text, bold `12px` font size. Accompanied by a shield or check icon.
- **Warning Banner:** `#FFF3E0` background, `#F59E0B` 1px left accent border (3px thick) or full surround, with `#B76E00` body copy.
- **Bank Trust Seal Banner:** Positioned at the summary base—incorporates a locked padlock icon, 256-bit SSL encryption badge, and RuPay/PCI-DSS compliance indicators.