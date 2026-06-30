# 07 · Technical SEO Audit & WordPress → .NET Migration

> The migration is the single best opportunity to fix everything at the root — and the single biggest risk if mishandled.

## Executive Summary

The technical findings cluster into a few root causes that a clean .NET rebuild resolves by design. The discipline is to treat SEO as a **migration acceptance criterion**, not a post-launch cleanup, and to protect existing equity through rigorous redirect and metadata governance.

## Business Problem

Platform migrations are where local businesses silently lose rankings: changed URLs without redirects, lost or duplicated metadata, broken indexation rules, and dropped tracking. Done wrong, the move erases the small footprint Swift has; done right, it leapfrogs years of incremental fixes.

## Research Findings

**Current issues (Screaming Frog + crawl):** HTTP/HTTPS & mixed content; duplicate titles / meta / H1s (Gutenverse templating); 42 `noindex` URLs; weak internal linking; thin content (1 page); image optimization; WordPress attachment-page bloat.

**Root causes:** (1) plugin-generated templating duplicates metadata; (2) WordPress auto-creates attachment URLs; (3) no deliberate IA or internal-linking model.

## Strategic Recommendation

Ship the new .NET site against an explicit SEO spec:
- **Unique, templated metadata** — every page type renders a unique `<title>`, meta description, and single H1 from structured fields.
- **URL taxonomy** — clean, keyword-aligned paths (`/services/water-damage-restoration/`, `/service-areas/ames-ia/`).
- **301 redirect map** — every legacy URL → its best new equivalent; no orphan 404s.
- **Indexation policy** — canonical tags, XML sitemap, robots rules; **suppress attachment/junk URLs** entirely.
- **Schema** — LocalBusiness/Organization, Service, FAQ, Breadcrumb.
- **Performance** — HTTPS-only, optimized image pipeline, Core Web Vitals budget.

## Implementation Plan

1. Freeze a full legacy URL inventory (already crawled).
2. Build the 301 map alongside the new sitemap (Section 09).
3. Implement template-level metadata + schema in .NET.
4. **Staging crawl** to validate titles/H1s/canonicals/redirects before launch.
5. Launch → submit new sitemap, monitor GSC coverage + crawl errors, watch redirects resolve.

## Expected Business Impact

Eliminates the duplicate-metadata and crawl-bloat classes permanently, preserves equity through the move, and establishes a technically clean base that makes every subsequent content and local effort effective.

## KPIs

Post-migration traffic-retention %, redirect coverage (target 100% of legacy URLs), `noindex`/duplicate counts on content pages (→0), indexed real pages, Core Web Vitals pass rate, crawl errors in GSC.

## Next Steps

Architecture in [08](../08-Website-Architecture/README.md); the page tree in [09](../09-SEO-Sitemap/README.md).

---
[← Back to overview](../README.md)
