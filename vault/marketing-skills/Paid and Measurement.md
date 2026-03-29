# Paid and Measurement Skills

Four skills cover paid advertising, ad creative, analytics, and experimentation.

---

## Paid Ads `/paid-ads`

Plan, launch, and optimize paid campaigns on Google, Meta, LinkedIn, Twitter/X, and TikTok.

### Platform selection guide
| Platform | Best for | Use when |
|---|---|---|
| Google Ads | High-intent search traffic | People actively search for your solution |
| Meta | Demand generation, visual products | Creating demand, strong creative assets |
| LinkedIn | B2B, decision-makers | Job title or company targeting matters, higher price points |
| Twitter/X | Tech audiences, thought leadership | Audience is active on X |
| TikTok | Younger demographics, viral creative | Audience skews 18 to 34, video capacity exists |

### What it asks
- Primary objective (awareness, traffic, leads, sales)
- Target CPA or ROAS
- Monthly budget
- Product or offer being promoted
- Landing page URL
- Ideal customer profile
- Existing customer data for lookalikes

### Ad copy frameworks
- **Problem-Agitate-Solve (PAS)**: Name the problem. Make it feel urgent. Present your product as the solution.
- **Before-After-Bridge (BAB)**: Show life before your product. Show life after. Bridge the gap with your product.
- **Social Proof Lead**: Start with a customer result, then explain how it happened.

### Campaign structure best practice
- One campaign per objective
- One ad set per audience segment
- Multiple ad variations per ad set (3 to 5 minimum for testing)

### Retargeting strategy
- **Warm audience** (visited site, viewed product): direct offer with urgency
- **Hot audience** (started trial, abandoned cart): remove the friction that stopped them
- **Past customers**: upsell or win-back with a specific reason to return

### Budget guidance for beginners
- $150 to $300/month minimum per platform to generate meaningful data
- Run a platform for 30 to 60 days before evaluating performance
- Allocate 70% to your best-performing audience, 30% to testing

### Related
- For ad copy generation: `/ad-creative`
- For landing page optimization: `/page-cro`

---

## Ad Creative `/ad-creative`

Generate ad copy at scale: headlines, descriptions, primary text, and full variations.

### What it asks
- Platform and ad format (search RSA, display, social feed, stories, video)
- Existing ads to iterate on, or starting from scratch
- Product and core value proposition
- Target audience and intent level
- Performance data (if iterating on existing ads)

### Google RSA headline structure
- Up to 15 headlines, 30 characters each
- Up to 4 descriptions, 90 characters each
- Include: keyword, benefit, social proof, urgency, CTA

### Meta/social ad copy structure
- Primary text (above image): hook + problem + solution + CTA
- Headline (below image): value proposition, 40 characters or fewer
- Description: supporting detail or social proof

### Iteration process
1. Start with 5 to 10 variations per message angle
2. Run for 2 weeks minimum
3. Pause lowest performers
4. Create new variations based on winners
5. Test one variable at a time (headline vs. headline, not headline vs. image)

### Related
- For campaign strategy: `/paid-ads`
- For landing page copy: `/copywriting`

---

## Analytics Tracking `/analytics-tracking`

Set up, audit, and improve marketing and product analytics.

### Core principles
1. Track for decisions, not data. Every event should inform a decision.
2. Avoid vanity metrics. Focus on actions tied to business outcomes.
3. Quality over quantity. Too many events create noise.

### What it asks
- What decisions will this data inform?
- What are the key conversion events?
- What tools are currently in use?
- Tech stack and privacy or compliance requirements

### Standard events to track (minimum)
- Page views with UTM parameters
- Signup started
- Signup completed
- Activation event (product-specific "aha moment")
- First conversion
- Purchase or subscription start
- Cancellation

### UTM parameter standard
- utm_source: where traffic comes from (google, newsletter, twitter)
- utm_medium: channel type (cpc, email, social, organic)
- utm_campaign: campaign name (launch_jan2025, black_friday)
- utm_content: specific creative or link (button_hero, link_nav)

### Related
- For A/B test measurement: `/ab-test-setup`

---

## A/B Test Setup `/ab-test-setup`

Design valid A/B tests and experiments.

### Core principles
1. Start with a hypothesis. Not "let's see what happens." A specific prediction based on data or reasoning.
2. Test one variable at a time.
3. Run until statistical significance. Do not call tests early.
4. Minimum detectable effect. Know what improvement you're looking for.

### What it asks
- What are you trying to improve?
- What change are you considering?
- Baseline conversion rate
- Current traffic volume
- Technical constraints and tools available

### Sample size calculation
Before running a test, calculate required sample size:
- Baseline rate: current conversion rate
- Minimum detectable effect: smallest improvement worth acting on (typically 10 to 20%)
- Statistical significance: 95% confidence (standard)
- Use tools: Evan Miller's sample size calculator

### Metrics to define before running
- **Primary metric**: the one number that determines winner (conversion rate, revenue per visitor)
- **Secondary metrics**: supporting signals to check (bounce rate, time on page)
- **Guardrail metrics**: things that must not get worse (signup rate, NPS, load time)

### Test duration
- Run for at least 2 full business cycle weeks
- Never call a test based on day-of-week bias
- Stop when sample size is met and significance is reached

### Hypothesis format
"Changing [X] to [Y] will increase [primary metric] because [reason based on data or behavior]."

### Related
- For tracking implementation: `/analytics-tracking`
- For page-level optimization: `/page-cro`
