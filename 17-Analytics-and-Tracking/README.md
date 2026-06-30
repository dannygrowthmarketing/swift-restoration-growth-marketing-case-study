# 17 · Analytics & Tracking

> You can't improve what you don't measure — and the migration must not break tracking.

## Executive Summary

A measurement stack ties effort to business outcomes (calls and leads), establishes the baselines this engagement currently lacks, and is implemented as part of the migration so continuity is preserved.

## Business Problem

Today there is no analytics, call tracking, or rank/GBP reporting. Without it, ROI is unprovable and optimization is guesswork — and a migration done without analytics planning can sever tracking entirely.

## Research Findings

No GA4/GSC/call-tracking observed for Swift; the only connected ad data in the toolchain belongs to an unrelated client. Measured baselines available today: Domain Rating (3.2), GBP reviews (5.0★/15), crawl structure (~7 real pages).

## Strategic Recommendation

- **GA4** with conversions defined as **calls + form leads** (not pageviews).
- **Call tracking** (e.g. CallRail / DNI) to attribute phone calls to source — foundational for proving ROI.
- **GSC** for impressions/queries/coverage (the 'existing keywords' data not otherwise accessible).
- **Rank + geo-grid tracking** for local-pack share by town.
- **GBP performance** export monthly; **LSA** lead reporting.
- **Migration continuity:** re-implement GA4/GTM, call tracking, and schema on .NET; verify in staging.

## Implementation Plan

Stand up GA4 + call tracking + GSC in Month 1; capture baselines; build the KPI dashboard (Section 19). Validate all tags survive migration before launch.

## Expected Business Impact

Every channel becomes measurable in cost-per-qualified-lead terms; optimization becomes evidence-based; the migration ships without losing data.

## KPIs

Tracking coverage (calls + forms = 100% attributed), baseline capture completeness, post-migration tag-survival rate.

## Next Steps

Baselines and targets in [19 · Results & KPIs](../19-Results-and-KPIs/README.md); near-term plan in [18](../18-Month-1-Roadmap/README.md).

---
[← Back to overview](../README.md)
