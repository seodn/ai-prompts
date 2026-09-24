# Complete Website Audit Workflow

Use this workflow to find factual, content, SEO, technical, conversion, design, accessibility, and functional errors across service businesses, ecommerce stores, SaaS products, publishers, marketplaces, and other websites.

## 1. Establish the source of truth

Before auditing the website, collect the information that defines what the website is supposed to say and do:

- Client brief
- Product and service catalogue
- Prices, tax treatment, and inclusions
- Locations and service areas
- Approved claims, certifications, and awards
- Business hours and contact details
- Payment, delivery, warranty, refund, and cancellation policies
- Brand guidelines
- Keyword map
- Known exclusions
- Previous client feedback

Create a claim register:

| Status | Meaning |
| --- | --- |
| Confirmed | Supported by client information or authoritative evidence |
| Needs verification | Plausible, but proof is missing |
| Incorrect | Conflicts with the source of truth |
| Missing | Confirmed information is absent from the website |

For every time-sensitive claim, also record:

- Owner
- Authoritative evidence source
- Date verified
- Review-by or expiry date

Use the review-by date to trigger revalidation of prices, availability, opening hours, service areas, funding, staff qualifications, accreditations, review counts, and other claims that can become outdated. A claim without current evidence should return to `Needs verification`; it should not remain confirmed indefinitely.

Do not assume that existing website content is correct.

## 2. Define the website objective

Record the website type, target audience, primary conversion, secondary conversions, and highest-value pages.

| Website type | Typical primary conversion |
| --- | --- |
| Local service business | Phone call, quote, or booking |
| Ecommerce | Completed purchase |
| SaaS | Trial, demo, or subscription |
| Marketplace | Search, enquiry, or transaction |
| Publisher or blog | Reading, subscription, or affiliate click |
| Nonprofit | Donation, volunteer signup, or enquiry |
| Portfolio | Contact or project enquiry |
| Healthcare | Appointment request |
| Education | Application, enquiry, or course purchase |

## 3. Confirm that the site renders

Open the website in a real browser before relying on a crawler.

Verify:

- The page loads without an error.
- Text, images, icons, fonts, and styles render.
- The header and footer appear.
- JavaScript-dependent content becomes visible.
- No popup, cookie notice, or loading screen blocks the site.
- No obvious browser or console error breaks functionality.
- The URL is the intended environment.
- Staging content is not accidentally indexable.

Record the browser, device size, date, and environment tested.

## 4. Build the page inventory

Collect URLs from:

- Main navigation and dropdowns
- Footer
- XML sitemap
- Internal links
- Categories, filters, and pagination
- Search results
- Robots file
- Canonical links
- Search Console and analytics
- CMS page list, when available

Group URLs by template:

- Homepage
- Service or product pages
- Category or collection pages
- Location pages
- Blog or article pages
- About and team pages
- Contact pages and forms
- Checkout and account pages
- Legal pages
- Search, filter, pagination, error, and empty-state pages

Inspect every page on a small website. On a large website, inspect every important page plus representative samples from every template.

Recommended large-site sample:

- All primary navigation pages
- All conversion pages
- Top 20 organic landing pages
- Top 20 revenue pages
- At least five pages from every template
- Recently published pages
- Pages with declining traffic
- Parameter, filter, and pagination variants
- One valid and one invalid URL
- One unavailable or out-of-stock item
- One empty search result

## 5. Test global components

### Header

- Logo links to the homepage.
- Navigation labels are clear.
- Dropdowns work with mouse, touch, and keyboard.
- Every item reaches the correct page.
- Active-page state is clear.
- Contact details and calls to action work.
- Address and map links are correct.
- Important pages are not unnecessarily buried.

### Footer

- Contact details are accurate and consistent.
- Social links reach the correct profiles.
- Service links are complete.
- Legal links work.
- Copyright year is correct.
- Footer content is consistent across templates.

### Global conversion elements

- Sticky buttons do not obscure content.
- Chat and phone controls work.
- Cookie controls work.
- Quote or cart counters start in the correct state.
- Users can remove or clear selections.
- Success, error, and loading states are visible.

## 6. Audit page content

For each page, check:

- Is its purpose immediately clear?
- Does the opening accurately describe the offer?
- Is the content specific to this business?
- Does it answer the visitor's likely questions?
- Is important information missing?
- Is anything irrelevant, repetitive, or contradictory?
- Are prices and inclusions consistent?
- Are claims supported?
- Are exclusions explained where necessary?
- Are placeholder phrases, test numbers, or unfinished notes visible?
- Is the spelling and grammar appropriate for the target country?
- Is capitalisation consistent?
- Does the page use customer language?
- Does it avoid unsupported superlatives such as "best," "cheapest," or "guaranteed"?

Search sitewide for risky terms such as:

- Lorem ipsum
- Coming soon
- Test
- 123
- TBC
- To be confirmed
- Placeholder
- Update this
- Old company names
- Old domains
- Incorrect locations
- Unsupported "approved," "certified," "best," or "guaranteed" claims

## 7. Verify factual claims

Compare the live website with the claim register. Pay particular attention to:

- Prices and tax treatment
- Product or service availability
- Inclusions and exclusions
- Delivery and turnaround times
- Warranties and guarantees
- Certifications and memberships
- Review counts and ratings
- Customer numbers and years in business
- Staff qualifications
- Opening hours and locations
- Payment methods
- Brands stocked
- Areas served
- Regulatory authority
- Refund and cancellation rules

Use this decision rule:

- Confirmed and correctly worded: keep.
- Confirmed but missing: add.
- Contradictory: correct immediately.
- Ambiguous: ask the client.
- Unsupported: remove or qualify.
- Time-sensitive: verify immediately before publication.

Never convert an ambiguous statement such as "$150 GST" into either "$150 plus GST" or "$150 including GST" without clarification.

## 8. Check headings and page structure

- Use one descriptive H1.
- Use H2s for principal sections.
- Use H3s within H2 sections.
- Avoid jumping from H1 directly to H3.
- Do not use headings only for visual styling.
- Do not make eyebrow labels such as "OUR SERVICES" the principal H2.
- Avoid duplicate headings hidden in responsive layouts.
- Use sentence case consistently.
- Ensure headings remain useful without surrounding text.
- Automatically flag empty headings, empty links, icon-only controls without accessible names, and rendered-but-hidden duplicate structures.
- Check the rendered DOM as well as the source HTML so client-side components and responsive variants are included.

## 9. Audit SEO metadata

For every indexable page, record:

- URL
- HTTP status
- Title
- Meta description
- H1
- Robots directive
- Canonical URL
- Open Graph title, description, image, and URL
- Twitter metadata
- Structured data
- Internal-link count
- Word count

Verify that titles and descriptions are unique, useful, and free from placeholder copy. Canonicals must use the final production domain, and only pages intended for search should be indexable.

## 10. Audit crawlability and indexability

Inspect:

- `robots.txt`
- XML sitemap and response type
- Sitemap URLs
- Canonical tags
- Robots meta tags
- HTTP status codes
- Redirects and redirect chains
- Soft 404s
- Broken links
- Duplicate URLs
- Trailing-slash consistency
- HTTP-to-HTTPS redirection
- `www` versus non-`www`
- Parameter URLs
- Filters and pagination
- JavaScript rendering
- Initial HTML

Compare the raw HTML response with the browser-rendered page. If meaningful content appears only after JavaScript runs, recommend server rendering or pre-rendering.

A sitemap URL must return XML, not homepage HTML with a false 200 response.

## 11. Audit architecture and internal links

- Important pages should be within three clicks of the homepage.
- Parent pages should link to child pages.
- Child pages should link to their relevant parent.
- Related pages should link contextually.
- Anchor text should describe the destination.
- Important links should be real links, not JavaScript-only buttons.
- Indexable pages should not be orphaned.
- Breadcrumbs should reflect the hierarchy.
- Location pages should not be thin doorway pages.
- Multiple pages should not compete for the same keyword.

Create a search-intent cannibalisation map for every indexable page. Record its primary query or topic, search intent, location, audience, funnel stage, and any competing URLs. Where two pages target the same intent, differentiate them substantially, consolidate them, or select one canonical destination rather than allowing both to compete.

For local businesses, reconcile the name, address, phone number, opening hours, location name, service area, and map destination across visible page copy, the header and footer, structured data, contact pages, location pages, Google Business Profiles, and other authoritative listings. Record every discrepancy instead of choosing one version without client confirmation.

## 12. Test every call to action

Create a CTA inventory containing:

- CTA text
- Page and section
- Intended result
- Actual result
- Destination
- Tracking event
- Status

Test repeated instances of every CTA type. Verify that the CTA visibly responds, reaches the correct destination, preserves or preselects relevant information, can be reversed where appropriate, works on mobile and desktop, and fires the correct analytics event once.

Use consistent language. A button labelled "Book" should not merely add an item to a list, and a button labelled "Get a quote" should open or reach a quote process.

## 13. Test every form

Use authorised test data and a test destination. Do not submit real personal information during an audit.

Check:

- Visible, connected labels
- Correct required fields and input types
- Stable field names
- Browser autocomplete
- Useful validation messages
- Preserved data after an error
- Correct product or service preselection
- Privacy wording
- Spam protection
- Secure POST submission
- No personal details in the URL
- Clear loading, success, and failure states
- Delivery to the intended recipient
- Duplicate-submission control
- Conversion tracking on successful submission only

Test empty, invalid, valid, long, special-character, failure, duplicate-click, and keyboard-only scenarios.

## 14. Perform visual and responsive QA

Test at representative widths:

- 320px
- 360px
- 375px
- 390px
- 768px
- 1024px
- 1280px
- 1440px

At every width, inspect horizontal overflow, cropped text, wrapping headings, overlapping controls, floating widgets, grids, image cropping, whitespace, card heights, alignment, padding, modal scrolling, sticky headers, menus, tables, forms, carousels, and footer stacking.

Also test landscape orientation and 200% zoom. Capture screenshots of every visual defect.

## 15. Check accessibility basics

- Keyboard access to every interactive element
- Visible focus indicator
- Logical tab order
- Skip-to-content link
- Correct link and button roles
- Accessible menus and accordions
- Modal focus trap, Escape handling, and focus return
- Meaningful image alt text
- Empty alt text for decorative images
- Connected form labels
- Announced errors and status changes
- Sufficient colour contrast
- Information not conveyed by colour alone
- Touch targets of approximately 44 by 44 pixels
- Declared page language
- Logical heading hierarchy

Automated accessibility checks support, but do not replace, manual keyboard testing.

## 16. Inspect images and media

- Relevance and authenticity
- Real versus generic stock imagery
- Unnecessary repetition
- Accurate alt text
- Dimensions and file size
- Modern formats
- Responsive variants
- Lazy loading
- Explicit width and height
- Hero image prioritisation
- Captions and attribution
- Video controls and poster images
- Broken media
- Ecommerce gallery and zoom behaviour

## 17. Review trust and compliance

Check for verifiable certifications, current reviews, source links, named team members, qualifications, address, phone, email, consistent business identity, legal policies, regulatory disclosures, secure checkout, accurate payment methods, and appropriately qualified guarantees.

Remove or qualify anything that cannot be proven.

## 18. Run website-type-specific checks

### Ecommerce

Test category navigation, search, filters, sorting, variants, stock, pricing, tax, currency, product images, cart updates, discount codes, shipping calculations, guest checkout, payment failure, confirmation, returns, out-of-stock handling, Product schema, Offer schema, and faceted URL indexation.

### Service business

Test service accuracy, service areas, quote and booking flows, phone links, maps, hours, qualifications, prices, inclusions, exclusions, LocalBusiness schema, Google Business Profile consistency, reviews, and location-page duplication.

For every local landing page, require location-specific evidence such as a real address or verified service area, local phone and hours where applicable, staff or provider details, original photographs, services and availability, reviews or testimonials, directions, and genuinely useful local information. Flag pages that merely swap place names in a shared template, make unsupported local claims, or exist primarily to capture nearby keywords as potential doorway pages.

### SaaS

Test positioning, feature accuracy, pricing tiers, trial restrictions, signup, email verification, login, password reset, upgrades, billing frequency, cancellation, documentation, integrations, security claims, and software schema where relevant.

### Publisher or blog

Test author information, publication and update dates, sources, freshness, related content, categories, tags, pagination, subscriptions, affiliate disclosures, Article schema, and archive indexation.

### Marketplace or directory

Test search quality, filters, locations, listing ownership, duplicates, empty results, reviews, provider profiles, contact or transaction flows, spam listings, pagination, filter indexation, and listing schema.

## 19. Record issues consistently

Every issue should contain:

| Field | Required information |
| --- | --- |
| ID | Unique issue number |
| Severity | Critical, High, Medium, or Low |
| URL | Exact affected page |
| Section | Header, hero, form, product card, footer, and so on |
| Device | Desktop, mobile, or both |
| Category | Technical, content, SEO, conversion, design, accessibility, or factual |
| Current issue | What is wrong |
| Evidence | Screenshot, extracted value, or test result |
| Impact | Why it matters |
| Recommended change | Exact correction |
| Replacement copy | Include when relevant |
| Owner | Developer, designer, SEO, content, or client |
| Status | Open, in progress, blocked, fixed, or verified |
| Verification method | How the fix will be retested |

Avoid vague recommendations such as "improve SEO" or "fix design." Every issue must be independently actionable.

## 20. Apply severity rules

### Critical

- Prevents purchase, booking, or submission
- Blocks important pages from indexing
- Exposes customer information
- Publishes materially false legal, price, or service information
- Produces a security or payment failure
- Makes the principal journey unusable

### High

- Seriously damages conversion
- Misrepresents an important offer
- Creates major navigation or mobile problems
- Removes essential trust
- Causes substantial duplicate or indexation risk
- Affects a global template or many pages

### Medium

- Creates confusion or avoidable friction
- Weakens relevance
- Produces inconsistent design or terminology
- Creates an accessibility problem without completely blocking use
- Creates incomplete internal linking

### Low

- Cosmetic or minor grammar issue
- Limited local impact
- Does not prevent task completion

Severity reflects business impact, not implementation difficulty.

## 21. Prioritise implementation

Organise work into:

1. Launch blockers
2. High-impact fixes
3. Quick wins
4. Longer-term improvements

Prioritise global-template fixes before individual pages, revenue pages before low-traffic pages, factual corrections before stylistic edits, indexability before keyword optimisation, and functional repairs before experiments.

## 22. Verify every fix

A change is not complete merely because it was deployed.

Retest:

- The original affected URL
- The same component on other templates
- Desktop and mobile
- Keyboard behaviour
- Raw HTML when SEO is involved
- Form delivery
- Analytics events
- Production-domain output
- Canonicals and sitemap
- Redirects
- Structured data

Mark an issue as verified only after independently reproducing the corrected behaviour.

## Recommended execution order

1. Collect client context.
2. Define goals and conversions.
3. Confirm that the live site renders.
4. Inventory pages and templates.
5. Crawl the website.
6. Inspect raw technical signals.
7. Visually inspect the homepage.
8. Test the global header, footer, and navigation.
9. Inspect every important page or template sample.
10. Compare claims with the source of truth.
11. Test CTAs, forms, and conversion journeys.
12. Test responsive layouts.
13. Test accessibility basics.
14. Run website-type-specific checks.
15. Record evidence-backed issues.
16. Prioritise by impact.
17. Send factual questions to the client.
18. Retest deployed fixes.
19. Perform a final pre-launch crawl.
20. Monitor production after launch.

## Minimum deliverables

- Page inventory
- Claim and source-of-truth register
- Prioritised issue log
- Page-level SEO table
- Broken-link and redirect report
- CTA and form test report
- Responsive screenshots
- Accessibility summary
- Client clarification list
- Consolidated developer checklist
- Post-fix verification report

## Final quality rule

Every finding must answer:

1. Where is the problem?
2. What exactly is wrong?
3. What evidence proves it?
4. Why does it matter?
5. What precisely should replace or fix it?

If a finding cannot answer all five questions, it is not ready for the developer.
