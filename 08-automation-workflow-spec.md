# Automation Workflow Spec – Prompt Audit Micro-Offer

**Goal**: Fully automated (or near-automated) delivery of the “Prompt Audit + Setup” micro-offer.

## Recommended Stack
- Intake: Tally.so or Typeform
- Payment: Stripe Payment Link (test: https://buy.stripe.com/test_8x26oIdqO4WeaYDdBs0kE01)
- Brain: Make.com (or n8n)
- AI: Claude / GPT API
- Delivery: GitHub repo access + Notion page + email
- Tracking: Money Automator Tracker Notion database

## Exact Flow (Make.com / n8n)

1. **Trigger**: New form submission (Tally/Typeform webhook)
   - Fields: Name, Email, Current AI tools, Main use case, Sample prompt (optional), Budget tier

2. **Payment Check** (optional parallel): Stripe webhook or manual confirmation for first sales; later automate with Stripe events.

3. **AI Processing**:
   - Send client context + sample prompt to Claude/GPT with the Core Framework + Evaluation Template.
   - Generate:
     - Optimized system prompt
     - 3–5 improved prompt examples
     - Quick-start checklist tailored to their tools
     - Scorecard of current vs improved approach

4. **Asset Creation**:
   - Create a private GitHub repo or folder for the client (or add to a delivery repo).
   - Create a Notion page with the deliverables.
   - Generate a short PDF/Markdown report.

5. **Delivery**:
   - Email the client with links (GitHub invite + Notion page + download).
   - Update Money Automator Tracker: Type = Sale, Status = Done, Amount = 47/97, Link = payment or delivery URL.

6. **Follow-up** (optional automation):
   - Day 3: Check-in email.
   - Day 7: Upsell to full Starter Pack or 1:1 audit.

## Setup Time Target
< 4 hours for the first complete scenario. After that, each new client should require < 15 minutes of human QC.
