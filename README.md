# Bill's OpenClaw Skills

Custom [OpenClaw](https://github.com/openclaw/openclaw) skills for marketing, SEO, CRO, and growth.

## Structure

```
skills/          # OpenClaw skill directories (SKILL.md + references)
tools/           # Integration guides for marketing platforms
├── REGISTRY.md  # Tool index with capabilities matrix
└── integrations/  # Per-platform setup & usage guides
```

## Skills

| Skill | Description |
|-------|-------------|
| [ab-test-setup](skills/ab-test-setup) | Plan, design, and implement A/B tests and experiments |
| [analytics-tracking](skills/analytics-tracking) | Set up, improve, or audit analytics tracking and measurement |
| [competitor-alternatives](skills/competitor-alternatives) | Create competitor comparison and alternative pages for SEO |
| [content-strategy](skills/content-strategy) | Plan content strategy, topics, and editorial calendars |
| [copy-editing](skills/copy-editing) | Edit, review, and improve existing marketing copy |
| [copywriting](skills/copywriting) | Write or rewrite marketing copy for any page |
| [email-sequence](skills/email-sequence) | Create or optimize email sequences and drip campaigns |
| [form-cro](skills/form-cro) | Optimize lead capture, contact, and checkout forms |
| [free-tool-strategy](skills/free-tool-strategy) | Plan and build free tools for lead gen and SEO |
| [launch-strategy](skills/launch-strategy) | Plan product launches, PH launches, and announcements |
| [marketing-ideas](skills/marketing-ideas) | Generate marketing ideas and growth strategies |
| [marketing-psychology](skills/marketing-psychology) | Apply behavioral science and psychology to marketing |
| [onboarding-cro](skills/onboarding-cro) | Optimize post-signup onboarding and activation |
| [page-cro](skills/page-cro) | Optimize conversions on marketing and landing pages |
| [paid-ads](skills/paid-ads) | Run paid ad campaigns on Google, Meta, LinkedIn, X |
| [paywall-upgrade-cro](skills/paywall-upgrade-cro) | Optimize in-app paywalls, upgrade screens, and upsells |
| [popup-cro](skills/popup-cro) | Create and optimize popups, modals, and banners |
| [pricing-strategy](skills/pricing-strategy) | Pricing decisions, packaging, and monetization |
| [product-marketing-context](skills/product-marketing-context) | Create product marketing context documents |
| [programmatic-seo](skills/programmatic-seo) | Create SEO pages at scale with templates and data |
| [referral-program](skills/referral-program) | Build and optimize referral and affiliate programs |
| [schema-markup](skills/schema-markup) | Add and optimize schema markup and structured data |
| [seo-audit](skills/seo-audit) | Audit and diagnose SEO issues |
| [signup-flow-cro](skills/signup-flow-cro) | Optimize signup, registration, and trial activation |
| [social-content](skills/social-content) | Create and optimize social media content |

## Tools & Integrations

See [`tools/REGISTRY.md`](tools/REGISTRY.md) for a full index of 29 marketing platform integrations (GA4, Stripe, HubSpot, Shopify, etc.) with API/MCP/CLI/SDK availability.

## Installation

```bash
# Copy a skill into your OpenClaw workspace
cp -r skills/launch-strategy/ ~/.openclaw/workspace/skills/

# Or symlink the whole skills directory
ln -s /path/to/bills-openclaw-skills/skills/* ~/.openclaw/workspace/skills/
```

## Credits

Marketing skills originally created by [Corey Haines](https://github.com/coreyhaines31) in [marketingskills](https://github.com/coreyhaines31/marketingskills). Converted to OpenClaw format with minor adaptations. All credit for the marketing knowledge, frameworks, and strategies goes to him. 🙏

## License

MIT
