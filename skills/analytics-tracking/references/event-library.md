# Event Library Reference

Comprehensive list of events to track by business type and context.

## Marketing Site Events

### Navigation & Engagement

| Event Name | Description | Properties |
|------------|-------------|------------|
| page\_view | Page loaded (enhanced) | page\_title, page\_location, content\_group |
| scroll\_depth | User scrolled to threshold | depth (25, 50, 75, 100) |
| outbound\_link\_clicked | Click to external site | link\_url, link\_text |
| internal\_link\_clicked | Click within site | link\_url, link\_text, location |
| video\_played | Video started | video\_id, video\_title, duration |
| video\_completed | Video finished | video\_id, video\_title, duration |

### CTA & Form Interactions

| Event Name | Description | Properties |
|------------|-------------|------------|
| cta\_clicked | Call to action clicked | button\_text, cta\_location, page |
| form\_started | User began form | form\_name, form\_location |
| form\_field\_completed | Field filled | form\_name, field\_name |
| form\_submitted | Form successfully sent | form\_name, form\_location |
| form\_error | Form validation failed | form\_name, error\_type |
| resource\_downloaded | Asset downloaded | resource\_name, resource\_type |

### Conversion Events

| Event Name | Description | Properties |
|------------|-------------|------------|
| signup\_started | Initiated signup | source, page |
| signup\_completed | Finished signup | method, plan, source |
| demo\_requested | Demo form submitted | company\_size, industry |
| contact\_submitted | Contact form sent | inquiry\_type |
| newsletter\_subscribed | Email list signup | source, list\_name |
| trial\_started | Free trial began | plan, source |

***

## Product/App Events

### Onboarding

| Event Name | Description | Properties |
|------------|-------------|------------|
| signup\_completed | Account created | method, referral\_source |
| onboarding\_started | Began onboarding | - |
| onboarding\_step\_completed | Step finished | step\_number, step\_name |
| onboarding\_completed | All steps done | steps\_completed, time\_to\_complete |
| onboarding\_skipped | User skipped onboarding | step\_skipped\_at |
| first\_key\_action\_completed | Aha moment reached | action\_type |

### Core Usage

| Event Name | Description | Properties |
|------------|-------------|------------|
| session\_started | App session began | session\_number |
| feature\_used | Feature interaction | feature\_name, feature\_category |
| action\_completed | Core action done | action\_type, count |
| content\_created | User created content | content\_type |
| content\_edited | User modified content | content\_type |
| content\_deleted | User removed content | content\_type |
| search\_performed | In-app search | query, results\_count |
| settings\_changed | Settings modified | setting\_name, new\_value |
| invite\_sent | User invited others | invite\_type, count |

### Errors & Support

| Event Name | Description | Properties |
|------------|-------------|------------|
| error\_occurred | Error experienced | error\_type, error\_message, page |
| help\_opened | Help accessed | help\_type, page |
| support\_contacted | Support request made | contact\_method, issue\_type |
| feedback\_submitted | User feedback given | feedback\_type, rating |

***

## Monetization Events

### Pricing & Checkout

| Event Name | Description | Properties |
|------------|-------------|------------|
| pricing\_viewed | Pricing page seen | source |
| plan\_selected | Plan chosen | plan\_name, billing\_cycle |
| checkout\_started | Began checkout | plan, value |
| payment\_info\_entered | Payment submitted | payment\_method |
| purchase\_completed | Purchase successful | plan, value, currency, transaction\_id |
| purchase\_failed | Purchase failed | error\_reason, plan |

### Subscription Management

| Event Name | Description | Properties |
|------------|-------------|------------|
| trial\_started | Trial began | plan, trial\_length |
| trial\_ended | Trial expired | plan, converted (bool) |
| subscription\_upgraded | Plan upgraded | from\_plan, to\_plan, value |
| subscription\_downgraded | Plan downgraded | from\_plan, to\_plan |
| subscription\_cancelled | Cancelled | plan, reason, tenure |
| subscription\_renewed | Renewed | plan, value |
| billing\_updated | Payment method changed | - |

***

## E-commerce Events

### Browsing

| Event Name | Description | Properties |
|------------|-------------|------------|
| product\_viewed | Product page viewed | product\_id, product\_name, category, price |
| product\_list\_viewed | Category/list viewed | list\_name, products\[] |
| product\_searched | Search performed | query, results\_count |
| product\_filtered | Filters applied | filter\_type, filter\_value |
| product\_sorted | Sort applied | sort\_by, sort\_order |

### Cart

| Event Name | Description | Properties |
|------------|-------------|------------|
| product\_added\_to\_cart | Item added | product\_id, product\_name, price, quantity |
| product\_removed\_from\_cart | Item removed | product\_id, product\_name, price, quantity |
| cart\_viewed | Cart page viewed | cart\_value, items\_count |

### Checkout

| Event Name | Description | Properties |
|------------|-------------|------------|
| checkout\_started | Checkout began | cart\_value, items\_count |
| checkout\_step\_completed | Step finished | step\_number, step\_name |
| shipping\_info\_entered | Address entered | shipping\_method |
| payment\_info\_entered | Payment entered | payment\_method |
| coupon\_applied | Coupon used | coupon\_code, discount\_value |
| purchase\_completed | Order placed | transaction\_id, value, currency, items\[] |

### Post-Purchase

| Event Name | Description | Properties |
|------------|-------------|------------|
| order\_confirmed | Confirmation viewed | transaction\_id |
| refund\_requested | Refund initiated | transaction\_id, reason |
| refund\_completed | Refund processed | transaction\_id, value |
| review\_submitted | Product reviewed | product\_id, rating |

***

## B2B / SaaS Specific Events

### Team & Collaboration

| Event Name | Description | Properties |
|------------|-------------|------------|
| team\_created | New team/org made | team\_size, plan |
| team\_member\_invited | Invite sent | role, invite\_method |
| team\_member\_joined | Member accepted | role |
| team\_member\_removed | Member removed | role |
| role\_changed | Permissions updated | user\_id, old\_role, new\_role |

### Integration Events

| Event Name | Description | Properties |
|------------|-------------|------------|
| integration\_viewed | Integration page seen | integration\_name |
| integration\_started | Setup began | integration\_name |
| integration\_connected | Successfully connected | integration\_name |
| integration\_disconnected | Removed integration | integration\_name, reason |

### Account Events

| Event Name | Description | Properties |
|------------|-------------|------------|
| account\_created | New account | source, plan |
| account\_upgraded | Plan upgrade | from\_plan, to\_plan |
| account\_churned | Account closed | reason, tenure, mrr\_lost |
| account\_reactivated | Returned customer | previous\_tenure, new\_plan |

***

## Event Properties (Parameters)

### Standard Properties to Include

**User Context:**

```
user_id: "12345"
user_type: "free" | "trial" | "paid"
account_id: "acct_123"
plan_type: "starter" | "pro" | "enterprise"
```

**Session Context:**

```
session_id: "sess_abc"
session_number: 5
page: "/pricing"
referrer: "https://google.com"
```

**Campaign Context:**

```
source: "google"
medium: "cpc"
campaign: "spring_sale"
content: "hero_cta"
```

**Product Context (E-commerce):**

```
product_id: "SKU123"
product_name: "Product Name"
category: "Category"
price: 99.99
quantity: 1
currency: "USD"
```

**Timing:**

```
timestamp: "2024-01-15T10:30:00Z"
time_on_page: 45
session_duration: 300
```

***

## Funnel Event Sequences

### Signup Funnel

1. signup\_started
2. signup\_step\_completed (email)
3. signup\_step\_completed (password)
4. signup\_completed
5. onboarding\_started

### Purchase Funnel

1. pricing\_viewed
2. plan\_selected
3. checkout\_started
4. payment\_info\_entered
5. purchase\_completed

### E-commerce Funnel

1. product\_viewed
2. product\_added\_to\_cart
3. cart\_viewed
4. checkout\_started
5. shipping\_info\_entered
6. payment\_info\_entered
7. purchase\_completed
