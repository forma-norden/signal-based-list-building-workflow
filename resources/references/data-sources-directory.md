# Data Sources Directory

Approved data sources for list building and enrichment workflows.

## B2B Contact Databases (The "Big Three")

| Provider | Data Strength | Weakness | Cost | Use Case |
|----------|---------------|----------|------|----------|
| Apollo.io | Coverage volume, US data | Bounce rates can be high | $ | Primary list building |
| ZoomInfo | Enterprise data, accuracy | Opaque pricing, lock-in | $$$ | Enterprise ABM, direct dials |
| Cognism | European data (GDPR compl.) | Smaller US footprint | $$ | EMEA/APAC targeting |

## Niche Contact Providers

| Provider | Focus Area | When to use |
|----------|------------|-------------|
| PhantomBuster | LinkedIn extraction | Scraping Sales Nav lists and event attendees |
| Ocean.io | Lookalike company search | Uncovering TAM based on your best customers |
| StoreLeads | E-commerce stores | Targeting Shopify, Magento, WooCommerce merchants |
| Prospeo | LinkedIn email finding | Best API for scraping individual LinkedIn profiles |

## Email Verification (Non-Negotiable)

| Provider | Accuracy | Feature |
|----------|----------|---------|
| BounceBan | High | Best at verifying Catch-All domains safely |
| Findymail | High | Specializes in B2B accuracy |
| MillionVerifier | Good | High volume, cost-effective |
| NeverBounce | Good | Standard industry fallback |

## Company / Firmographic Enrichment

| Provider | Best For | Note |
|----------|----------|------|
| Clearbit | Real-time API enrichment | Excellent for inbound form shortening |
| Clay | Workflow orchestration | Aggregates 50+ providers into one table |
| FullContact | Identity resolution | Good for mapping personal to professional data |

## How to Choose

1. **For pure volume in US:** Apollo -> Verify with Findymail -> Proceed
2. **For highest quality specific contacts:** LinkedIn Sales Nav -> Clay -> Prospeo/Findymail waterfall
3. **For EMEA compliance:** Cognism
4. **For eCommerce:** StoreLeads -> Apollo for contacts -> Verify
