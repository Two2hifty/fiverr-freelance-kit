# Product Marketing Context

Invoke: `/product-marketing-context`
Source: coreyhaines31/marketingskills
Version: 1.1.0

---

## What It Does

Creates and maintains `.agents/product-marketing-context.md` in your project. Every other marketing skill reads this file first before asking questions. Set it up once; all other skills inherit it.

---

## When to Use

- Starting a new project
- When another skill keeps asking the same foundational questions
- When you want to update your positioning, ICP, or messaging

---

## How It Works

### Step 1: Check for existing context
The skill checks `.agents/product-marketing-context.md`. If it exists, it summarizes what's captured and asks what to update.

### Step 2: Two setup options
1. **Auto-draft from codebase** (recommended): Reads your README, landing pages, marketing copy, and package.json. Drafts all sections. You review and correct.
2. **Start from scratch**: Walks through each section one at a time.

### All 12 sections captured
1. **Product Overview**: one-liner, what it does, product category, product type
2. **Target Audience**: demographics, firmographics, buying triggers
3. **Personas**: named profiles for each key buyer type
4. **Problems and Pain Points**: ranked by severity and frequency
5. **Competitive Landscape**: direct and indirect competitors, how you position against each
6. **Differentiation**: what makes you meaningfully different (not just "better")
7. **Objections and Anti-Personas**: who is NOT a good fit, common hesitations
8. **Switching Dynamics**: what makes people switch to you, what makes them leave
9. **Customer Language**: verbatim phrases from reviews, interviews, support tickets
10. **Brand Voice**: tone descriptors, dos and don'ts, sample sentences
11. **Proof Points**: metrics, case studies, testimonials, logos
12. **Goals**: what success looks like for this product in 6 to 12 months

---

## Key Principle

Use verbatim customer language. Exact phrases customers use are more valuable than polished descriptions because they reflect how customers actually think.

---

## Output

Creates `.agents/product-marketing-context.md` in your project root. All other skills reference this automatically.

---

## Related Skills
- All other marketing skills reference this first
- [[Content and Copy]]
- [[SEO]]
- [[CRO]]
