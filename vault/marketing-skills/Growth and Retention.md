# Growth and Retention Skills

Three skills cover growth channels and keeping customers.

---

## Free Tool Strategy `/free-tool-strategy`

Plan and build free tools for lead generation, SEO, and brand awareness (engineering as marketing).

### What it asks
- Core product and target audience
- Goals: lead generation, SEO traffic, brand awareness, product education
- Technical capacity to build
- Ongoing maintenance bandwidth

### Core principles
1. The tool must solve a real problem. Utility that exists only to collect emails fails.
2. The tool should naturally lead to your product.
3. The tool should be shareable. Something people send to colleagues.
4. Build for the long term. The best marketing tools compound value over years.

### High-ROI tool types
- ROI calculators ("How much are you losing to X?")
- Graders and audit tools ("Score your X")
- Generators ("Create your X in seconds")
- Comparison tools ("Compare A vs. B")
- Industry data tools ("What does the average X look like?")

### Successful examples
- HubSpot Website Grader: built millions of backlinks
- Moz's Domain Authority checker: drives millions of SEO visits
- Ahrefs' free backlink checker: top-of-funnel for their paid tool

### Related
- For downloadable lead magnets: `/lead-magnets`
- For SEO value: `/programmatic-seo`

---

## Referral Program `/referral-program`

Design programs that turn customers into growth channels.

### Program types
- Customer referral program (B2C): customer refers friend, both get reward
- Affiliate program (B2B): partner earns commission for referrals
- Ambassador program: advocates create content and drive awareness

### What it asks
- Program type and B2B vs B2C
- Average customer LTV
- Current CAC from other channels
- Existing referral or affiliate program
- Current referral rate (% of customers who refer)
- What incentives have been tried

### Incentive design
- Two-sided rewards outperform one-sided (reward both referrer and referee)
- Cash rewards are most motivating but reduce margin
- Account credits work well for SaaS (low cost, high perceived value)
- Free months, upgrades, and feature access work for software

### Key metrics to track
- Referral rate: % of customers who refer at least one person
- K-factor: how many new users each referral generates
- Referral conversion rate: % of referred leads who become customers
- Referral CAC vs. other channels

### Related
- For launch virality: `/launch-strategy`

---

## Churn Prevention `/churn-prevention`

Reduce voluntary churn (cancellations) and involuntary churn (failed payments).

### What it asks
- Current monthly churn rate (voluntary vs involuntary if known)
- Number of active subscribers
- Average MRR per customer
- Current cancel flow (instant cancel or friction-based?)
- Billing provider (Stripe, Chargebee, Paddle, Recurly)
- Billing intervals (monthly, annual, or both)
- Existing retention tooling (Churnkey, ProsperStack, Raaft)

### Voluntary churn interventions

**Cancel flow design:**
- Show what they will lose (features, data, history)
- Offer a pause option (1 to 3 months) before they cancel
- Offer a downgrade to a free or cheaper plan
- Show a save offer (discount, extended trial)
- Ask why they are canceling (exit survey drives future improvements)

**Save offer triggers:**
- 1-month discount: "Stay for 20% off your next 2 months"
- Free extension: "We'd like to give you 2 extra weeks"
- Plan downgrade: "Try our Starter plan at half the price"
- Human outreach: for high-value customers, trigger a personal email

### Involuntary churn (dunning)

**Dunning sequence:**
- Day 0: Payment fails. Retry within 24 hours.
- Day 3: Email — "Your payment didn't go through. Update your card."
- Day 7: Retry payment again.
- Day 10: Final warning. Account access will pause in 3 days.
- Day 14: Account paused. Card update reactivates immediately.

**Best practices:**
- Use Stripe's Smart Retries or equivalent
- Send SMS in addition to email for days 3 and 10
- Make card update a one-click flow (no login friction)

### Related
- For post-cancel win-back emails: `/email-sequence`
- For in-app paywalls: `/paywall-upgrade-cro`
