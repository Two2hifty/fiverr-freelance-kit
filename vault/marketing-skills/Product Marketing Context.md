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

### Sections captured
- Product overview (one-liner, what it does, product category, type)
- Target audience and ICP
- Key problems solved
- Positioning and differentiators
- Pricing model
- Brand voice and tone
- Customer language (verbatim phrases from reviews, support tickets)

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
