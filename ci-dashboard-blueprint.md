# Competitive Intelligence Dashboard Blueprint 📈

> A practical guide to building real-time competitive intelligence dashboards for data-driven decision-making.

---

## The CI Dashboard Imperative

[Forrester Research](https://www.forrester.com/) reports that 67% of companies cite "information overload without actionable insight" as their top competitive intelligence challenge. A well-designed CI dashboard transforms raw competitive data into decision-ready intelligence.

---

## Dashboard Architecture

### Layer 1: Data Sources

```
┌─────────────────────────────────────────────────────────────┐
│                      DATA SOURCES                            │
├───────────────┬───────────────┬───────────────┬─────────────┤
│  Web/Digital  │   Financial   │   Product     │   Social    │
│  ──────────── │  ──────────── │  ──────────── │  ────────── │
│  • Website    │  • Earnings   │  • Changelogs │  • Twitter/X │
│  • SEO/SEM    │  • Crunchbase │  • G2/Capterra│  • LinkedIn  │
│  • Job posts  │  • Owler      │  • App stores │  • Reddit    │
│  • Content    │  • SEC/EDGAR  │  • GitHub     │  • YouTube   │
│  • Pricing    │  • PitchBook  │  • Docs/API   │  • Podcasts  │
└───────────────┴───────────────┴───────────────┴─────────────┘
```

### Layer 2: Data Processing

```
Raw Data → ETL Pipeline → Enrichment → Scoring → Alert Rules
                                   ↓
                           Structured Database
```

### Layer 3: Visualization (Stakeholder Views)

| Stakeholder | Metrics | Refresh |
|-------------|---------|---------|
| **CEO/Board** | Market share shifts, strategic moves, threat matrix | Monthly |
| **CPO/Product** | Feature gaps, release velocity, review sentiment | Weekly |
| **CRO/Sales** | Battle card intel, win/loss, pricing changes | Daily |
| **CMO/Marketing** | Share of voice, content velocity, positioning shifts | Weekly |
| **CI Analyst** | All signals, trend analysis, anomaly detection | Real-time |

---

## Dashboard Components

### 1. Competitive Radar (Overview)

A birds-eye view of the competitive landscape:

| Competitor | Threat Level | Momentum | Key Moves (30d) | Alert |
|------------|-------------|----------|-----------------|-------|
| Comp A | 🔴 High | ↗️ +2 | New pricing, funding | ⚠️ |
| Comp B | 🟡 Medium | ➡️ 0 | New feature launch | 📊 |
| Comp C | 🟢 Low | ↘️ -1 | Layoffs reported | ✅ |

### 2. Feature Comparison Matrix

An interactive grid comparing feature presence across competitors:

| Feature Category | Our Product | Comp A | Comp B | Comp C |
|-----------------|-------------|--------|--------|--------|
| **Core** | | | | |
| Workflow A | ✅ | ✅ | ⚠️ | ❌ |
| Workflow B | ✅ | ❌ | ✅ | ⚠️ |
| **Advanced** | | | | |
| AI/ML Feature | ✅ | ⚠️ | ❌ | ❌ |
| API/Integration | ✅ | ✅ | ✅ | ❌ |
| **Enterprise** | | | | |
| SSO/SAML | ✅ | ✅ | ✅ | ❌ |
| Audit Logs | ✅ | ❌ | ⚠️ | ❌ |

### 3. Pricing & Packaging Tracker

Track pricing changes, packaging shifts, and discounting trends:

```
PRICING TIMELINE
─────────────────────────────────────────────────────
Jan ──── Price: $29/mo Basic
Feb ──── 
Mar ──── New "Teams" plan added
Apr ──── 
May ──── Price increase: $39/mo (+34%)
Jun ──── Annual-only for Enterprise
─────────────────────────────────────────────────────
```

### 4. Share of Voice Monitor

| Channel | Our Share | Comp A | Comp B | Trend |
|---------|-----------|--------|--------|-------|
| SEO (Top 10) | 24% | 31% | 18% | Comp A ↑ |
| Social Mentions | 28% | 22% | 35% | Comp B ↑ |
| Review Volume | 19% | 41% | 15% | Stable |
| Press/Media | 15% | 45% | 20% | Comp A ↑↑ |
| **Total SOV** | **21%** | **35%** | **22%** | **Comp A ↑** |

### 5. Win/Loss Dashboard

| Metric | Current | vs Last Q | vs Target |
|--------|---------|-----------|-----------|
| Overall Win Rate | 47% | +3% | 45% |
| Win Rate vs Comp A | 38% | -5% ⚠️ | 50% |
| Win Rate vs Comp B | 62% | +8% | 55% |
| Competitive Deals | 34% | +2% | - |
| Loss Reason: Price | 28% | +4% ⚠️ | <20% |
| Loss Reason: Features | 41% | -3% | <35% |

### 6. Review Sentiment Tracker

| Competitor | Rating | Trend | Top Praise | Top Complaint |
|------------|--------|-------|------------|---------------|
| Comp A | 4.2 | ↗️ +0.1 | Support quality | Pricing complexity |
| Comp B | 4.5 | ➡️ 0.0 | Ease of use | Limited integrations |
| Comp C | 3.8 | ↘️ -0.2 | Feature set | Buggy releases |

---

## Alert Configuration

Signal thresholds that trigger notifications:

| Signal | Threshold | Channel | Escalation |
|--------|-----------|---------|------------|
| Pricing change | Any | #ci-alerts | PMM + Product |
| New product launch | Any | #ci-alerts | All stakeholders |
| Funding > $10M | Any | #ci-funding | Strategy team |
| Major hire (C-suite) | Any | #ci-alerts | Leadership |
| Win rate drop > 5% | Monthly | #sales-ci | CRO + PMM |
| SOV drop > 10% | Weekly | #marketing-ci | CMO |
| Review rating drop > 0.2 | Weekly | #product-ci | CPO |

---

## Implementation Guide

### Phase 1: Foundation (Week 1-2)
- Identify top 5 competitors
- Set up basic monitoring (website, pricing, news)
- Build initial feature comparison matrix

### Phase 2: Automation (Week 3-4)
- Connect data sources via CI platforms like [FollowEngine](https://followengine.com)
- Configure automated alerts for key signals
- Build dashboard framework (Looker/Tableau/PowerBI)

### Phase 3: Intelligence (Week 5-6)
- Add review sentiment analysis
- Implement win/loss tracking integration
- Create stakeholder-specific views

### Phase 4: Optimization (Ongoing)
- Tune alert thresholds to reduce noise
- Add/remove competitors as landscape shifts
- A/B test dashboard layouts with stakeholders
- Integrate LLM-powered insights for automated analysis

---

## Tech Stack Options

| Component | Lightweight | Enterprise |
|-----------|------------|------------|
| Data Collection | Google Sheets + Apps Script | [FollowEngine](https://followengine.com), Crayon, Klue |
| Database | Airtable, Notion | Snowflake, BigQuery |
| Visualization | Google Data Studio | Tableau, Looker, PowerBI |
| Alerting | Slack webhooks, email | PagerDuty, Opsgenie |
| AI Analysis | ChatGPT/Claude manual | Custom LLM pipelines |

---

## Related Resources

- [Competitor Analysis Template](competitor-analysis-template.md)
- [Battle Card Template](battle-card-template.md)
- [CI KPI Framework](kpi-framework.md)
