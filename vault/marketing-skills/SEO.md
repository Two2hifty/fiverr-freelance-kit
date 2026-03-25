# SEO Skills

Five skills cover search engine optimization.

---

## SEO Audit `/seo-audit`

Diagnose and fix organic search issues.

### Audit priority order
1. Crawlability and indexation (can Google find and index the site?)
2. Technical foundations (speed, Core Web Vitals, mobile)
3. On-page optimization (titles, meta descriptions, headings, content)
4. Content quality (does it deserve to rank?)
5. Authority and links (does it have credibility?)

### What it asks
- Site type (SaaS, e-commerce, blog)
- Known issues or concerns
- Current organic traffic level
- Scope: full site or specific pages
- Access to Search Console or analytics

### Important limitation
`web_fetch` and `curl` cannot detect schema markup. Many CMS plugins inject JSON-LD via JavaScript, which does not appear in static HTML. To check schema, use:
- Google Rich Results Test
- Browser DevTools: `document.querySelectorAll('script[type="application/ld+json"]')`
- Screaming Frog (if client provides export)

### Related
- For structured data: `/schema-markup`
- For AI search: `/ai-seo`
- For scaling content: `/programmatic-seo`

---

## AI SEO `/ai-seo`

Optimize content to be cited by AI search engines: Google AI Overviews, ChatGPT, Perplexity, Claude, Gemini, Copilot.

### What it asks
- Do you appear in AI-generated answers today?
- What queries matter most to your business?
- What content types do you produce?
- What's your domain authority?

### Core optimization principles
- Write direct, factual answers to specific questions
- Use clear headings that match search queries
- Structure content with FAQ format where relevant
- Include structured data (see `/schema-markup`)
- Build topical authority by covering a subject comprehensively
- Get cited on authoritative external sites

### Related
- For traditional SEO: `/seo-audit`
- For structured data: `/schema-markup`

---

## Programmatic SEO `/programmatic-seo`

Build SEO-optimized pages at scale using templates and data.

### Common use cases
- Location pages: "[Service] in [City]"
- Comparison pages: "[Product A] vs [Product B]"
- Integration pages: "[Your tool] + [Partner tool]"
- Directory pages: "[Category] companies in [Location]"
- Alternative pages: "Best [Competitor] alternatives"

### What it asks
- What search patterns exist for your audience?
- How many potential pages?
- What data do you have to populate templates?
- What's the conversion goal for these pages?

### Critical requirement
Pages must provide genuine value. Thin content earns Google penalties. Each page needs a unique, useful data point or perspective — not just swapped keywords.

### Related
- For individual SEO: `/seo-audit`
- For content planning: `/content-strategy`
- For alternative pages specifically: `/competitor-alternatives`

---

## Site Architecture `/site-architecture`

Plan website page hierarchy, navigation, URL structure, and internal linking.

### What it asks
- Site type (SaaS marketing site, e-commerce, blog)
- Primary audiences
- Top 3 goals for the site
- New site or restructuring?
- If restructuring: what is broken?

### Deliverables
- Page hierarchy map
- URL structure recommendations
- Navigation structure
- Internal linking strategy
- Redirect plan (for restructures)

### Note
This covers visual sitemaps and information architecture. XML sitemaps and technical crawl issues are covered by `/seo-audit`.

### Related
- For technical SEO: `/seo-audit`
- For structured data: `/schema-markup`
- For scaling pages: `/programmatic-seo`

---

## Schema Markup `/schema-markup`

Implement JSON-LD structured data for rich results in Google search.

### Common schema types
- FAQ schema: shows expandable Q&A in results
- Product schema: star ratings, price, availability
- Review schema: aggregate ratings
- Breadcrumb schema: shows page path in results
- Organization schema: knowledge panel data
- Article schema: publication date, author
- HowTo schema: step-by-step rich results

### What it asks
- Page type and primary content
- Current schema (if any)
- Errors in Google Search Console
- Which rich results you're targeting

### Core principle
Schema must accurately represent page content. Do not add schema for content that does not exist on the page.

### Related
- For broader SEO: `/seo-audit`
- For AI search: `/ai-seo`
