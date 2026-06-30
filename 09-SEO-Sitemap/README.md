# 09 · SEO Sitemap

> The concrete page tree to build on .NET — sequenced by priority.

## Executive Summary

This sitemap turns the architecture and keyword strategy into a buildable, prioritized page list and the basis for the 301 redirect map.

## Business Problem

Without a defined page tree, the migration risks rebuilding the same flat brochure and the location strategy has nothing to populate.

## Research Findings

The keyword priority (06) and competitor town-page benchmark (05) define which pages earn build priority: core services + Boone/Ames first.

## Strategic Recommendation

```
/                                   Home (emergency hero, trust, service+area links)
/services/                          Services hub
  /services/water-damage-restoration/        [P1]
    .../basement-flooding/  .../burst-pipe/  .../sewage-cleanup/
  /services/fire-damage-restoration/         [P2]  .../smoke-odor/
  /services/mold-remediation/                [P2]
  /services/storm-damage-restoration/        [P2, NEW]
  /services/commercial-restoration/          [P2]
  /services/emergency-restoration/           [P1]
/service-areas/                     Service Areas hub
  /service-areas/boone-county/      → /boone-ia/ /ogden-ia/ /madrid-ia/   [Critical]
  /service-areas/story-county/      → /ames-ia/ /nevada-ia/ /story-city-ia/ [Critical]
  /service-areas/polk-county/       → /des-moines-ia/ /ankeny-ia/         [Later]
  /service-areas/dallas-county/     → /waukee-ia/ /adel-ia/               [Medium]
  /service-areas/{webster,hamilton,greene,guthrie}-county/                [Low]
/resources/                         Insurance · emergency guides · mold · storm · seasonal
/reviews/  /projects/  /about/  /contact/  /request-quote/
```

## Implementation Plan

Build order: Home + Water + Emergency + Boone + Ames (Month 1) → remaining services + Story/Boone towns → county hubs + Dallas/Webster → metro + resources. Each legacy URL maps to its new equivalent for the 301 plan (Section 07).

## Expected Business Impact

A clear, prioritized build backlog that front-loads the highest-conversion pages and gives the migration a defined target state.

## KPIs

Pages shipped vs. plan, indexed new pages, rankings per shipped page, matrix coverage.

## Next Steps

Navigation that exposes this tree is in [10](../10-Navigation-Strategy/README.md).

---
[← Back to overview](../README.md)
