# PRODUCT-BUILD-11 — STORE / CHECKOUT

Дата: 24.09.2026

## Status

PRODUCT-BUILD-11: 100% — STORE / CHECKOUT SPECIFICATION + CURRENT PLATFORM RESEARCH

Важно:
это коммерческая спецификация и исследование текущих условий платформ. Реальные store accounts, listings и checkout transactions ещё не созданы/не протестированы.

## 1. CHANNEL STRATEGY

Primary launch channel:
Payhip.

Secondary:
Gumroad.

Later discovery channel:
Notion Marketplace.

Future/optional:
Etsy.

Причина:
Payhip позволяет начать с Free plan за $0/month + 5% transaction fee, при этом заявляет все функции и unlimited products/revenue. Stripe/PayPal processing fees остаются отдельными. Payhip также указывает, что автоматически собирает и перечисляет EU VAT и UK VAT. citeturn0search3

## 2. PAYHIP

Current published pricing:

Free:
$0/month + 5% transaction fee.

Plus:
$29/month + 2%.

Pro:
$99/month, 0% transaction fee.

Payment processor fees remain separate. citeturn0search3

Launch recommendation for this zero-fixed-cost project:
Free plan.

## 3. PAYHIP PRODUCT STRUCTURE

Products:

FREE — 7-Day Life Reset
CORE — Personal Life Command Center
AI — Personal Life Command Center + AI
COMPLETE — Full Life Command Center

Initial launch price hypotheses:

CORE:
$14.99 launch
$19.99 regular

AI:
$24.99 launch
$29.99 regular

COMPLETE:
$34.99 launch
$39.99–44.99 regular

These are pricing hypotheses, not revenue forecasts.

## 4. GUMROAD

Current published direct-sale fee:
10% + $0.50 per transaction, plus applicable taxes; credit-card processing and PayPal fees may also apply according to Gumroad's current fee documentation.

Gumroad Discover marketplace sales are subject to 30% fee. There are no monthly payments. citeturn0search7

Therefore:
Gumroad is a secondary channel, not the only checkout.

## 5. ETSY

Etsy currently charges a 6.5% transaction fee on the total order amount. Etsy Payments processing fees are additional and vary by country. Etsy also has listing and other possible fees. citeturn0search6turn0search10

Therefore:
Etsy should be treated as a separate marketplace listing, with pricing/fees checked at activation.

No assumption is made about the exact Italy payment-processing percentage until the seller account displays the applicable current rate.

## 6. NOTION MARKETPLACE

Notion Marketplace supports paid templates.

Current official process:
- creator profile;
- submit paid template for review;
- payment onboarding through Stripe if selling directly;
- Notion approval required;
- ongoing commercially reasonable customer support required.

Notion currently states:
8% + $0.40 per transaction;
additional 1% FX fee for creators outside the US receiving payouts in local currency;
14-day holding period;
minimum $20 payout balance in general.

Notion is merchant of record for Marketplace transactions and handles regional sales tax/VAT. citeturn0search0turn0search2

Italy is currently listed among eligible countries for direct Marketplace selling. citeturn0search1

## 7. MARKETPLACE ACCESS LOCKING

Notion Marketplace provides access locking.

For a paid template:
Restricted should be evaluated for the commercial product to reduce redistribution through supported Marketplace controls.

If using third-party checkout, a separate Notion Site/template copy should be maintained for that channel because Notion explains that Marketplace payment onboarding can change duplication behavior of existing template URLs. citeturn0search0

## 8. CHANNEL SEPARATION

Maintain separate delivery/template endpoints:

PAYHIP TEMPLATE
GUMROAD TEMPLATE
NOTION MARKETPLACE TEMPLATE

Reason:
prevent one channel's access/locking rules from unintentionally breaking another channel.

Use identical product architecture but separate duplicate endpoints.

## 9. PRODUCT LISTING

Title:

Personal Life Command Center — Notion Life Planner & Productivity System

Short description:

A simple, mobile-first Notion system to organize life areas, goals, projects, tasks and reviews — with optional AI workflows and five language editions.

Feature bullets:

- Mobile-first organization system
- Goals → Projects → Tasks
- Today / This Week / Overdue views
- Weekly / Monthly / Quarterly / Yearly Reviews
- Quick Capture inbox
- Optional AI workflows
- Sample + Blank workspaces
- English, Italian, French, German and Russian
- Printable review pack
- Personal-use license

## 10. LISTING CLAIM POLICY

Allowed:
describe included features.

Not allowed:
- guaranteed productivity;
- guaranteed life transformation;
- guaranteed success;
- "AI manages your life automatically";
- unsupported compatibility claims;
- claims that physical mobile QA passed before it actually passes.

## 11. CHECKOUT FLOW

Preferred Payhip flow:

Listing
→ Product page
→ Checkout
→ Payment
→ Automatic delivery
→ Customer opens START-HERE
→ Sample
→ Blank
→ Setup.

Gumroad follows equivalent digital delivery flow.

Notion Marketplace:
Listing
→ Notion checkout
→ Template access/duplication according to Marketplace rules.

## 12. CHECKOUT TEST

Before launch test:

C1 product page opens.
C2 price is correct.
C3 product description is correct.
C4 checkout opens.
C5 payment succeeds in controlled test.
C6 delivery occurs.
C7 customer receives correct version.
C8 links work.
C9 Sample works.
C10 Blank works.
C11 license is included.
C12 support path works.
C13 refund process is documented.

## 13. DIGITAL DELIVERY RULE

Customer must receive:

START-HERE
LICENSE
correct Notion template endpoint
AI package
Printables
language resources
support information.

No internal research files.

## 14. FREE LEAD PRODUCT

FREE — 7-Day Life Reset.

Purpose:
allow customers to experience the system before buying the complete product.

It should be genuinely useful and not simply a sales brochure.

CTA:
Explore the full Personal Life Command Center.

## 15. OFFER LADDER

FREE
↓
CORE
↓
CORE + AI
↓
COMPLETE
↓
future BUNDLE

No artificial feature duplication.

Each higher tier adds real utility.

## 16. BUNDLE

Future:
Personal Command Center Bundle.

Potential:
Money
Productivity
Life
Freelancer
Home
Goals/Habits

Do not launch bundle until individual products are stable.

## 17. REFUND POLICY DRAFT

Draft principle:

Because this is a digital product, refunds should follow the applicable platform rules and local law.

The final store-specific refund wording must be adapted to the selected platform's current policy and the seller's legal/tax setup.

Do not promise a universal refund policy across platforms without checking their current terms.

## 18. SUPPORT

Support should provide:

- setup help;
- broken link troubleshooting;
- template access help;
- language guidance;
- AI prompt help;
- platform-specific delivery issues.

Support does not include:
custom life coaching;
custom database construction;
personal productivity consulting.

## 19. STORE ASSET CHECKLIST

Required:

1. Hero image
2. Desktop screenshot
3. Mobile screenshot
4. Sample screenshot
5. Goals/Projects screenshot
6. Today screenshot
7. Reviews screenshot
8. AI screenshot
9. Language screenshot
10. What's included graphic

Screenshots must reflect the actual final product after physical QA.

## 20. PLATFORM COMPARISON

| Channel | Current fee model | Role |
|---|---|---|
| Payhip Free | $0/mo + 5% | Primary zero-fixed-cost checkout |
| Gumroad | 10% + $0.50 direct sale | Secondary checkout |
| Etsy | 6.5% transaction + payment/listing fees | Marketplace discovery |
| Notion Marketplace | 8% + $0.40; possible 1% FX outside US | Native Notion discovery/sales |

Sources: official platform documentation. citeturn0search3turn0search7turn0search6turn0search0

## 21. LAUNCH ORDER

Phase 1:
Payhip.

Phase 2:
Gumroad.

Phase 3:
Notion Marketplace application/listing.

Phase 4:
Etsy, after final digital-product listing assets and policy checks.

This is a launch sequence, not a prediction of sales performance.

## 22. STORE QA GATE

No platform goes live until:

- final product exists;
- physical Notion QA passes;
- checkout test passes;
- delivery test passes;
- listing matches product;
- license is present;
- support works;
- refund wording is checked;
- platform terms are current.

## 23. CURRENT BLOCKERS

B1 — live Notion workspace.
B2 — physical mobile test.
B3 — physical formula test.
B4 — physical Sample/Blank duplication.
B5 — final package generation.
B6 — actual store account/listing setup.
B7 — controlled checkout tests.

## 24. NEXT

PRODUCT-BUILD-12 — FINAL RELEASE / PUBLICATION GATE.

It will combine:
- physical workspace QA;
- final package;
- listing;
- checkout;
- delivery;
- release manifest;
- version 1.0.0;
- publication checklist.

## 25. Status

PRODUCT-BUILD-11 — 100% specification/research.
Physical store and checkout remain pending.
