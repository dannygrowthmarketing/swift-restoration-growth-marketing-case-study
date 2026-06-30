# 03 · Current-State Audit

> The site is a brochure, not a lead engine — and that's the strategic unlock.

## Executive Summary

A live crawl plus a Screaming Frog issue export reveal a site with almost no SEO-relevant structure. This is good news strategically: there is nothing to undo, and the migration lets us build correctly the first time.

## Business Problem

Without keyword-targeted pages, schema, internal linking, or local pages, the site cannot rank for the commercial and emergency queries that drive restoration revenue. It currently earns visibility almost only for brand/navigational queries.

## Research Findings

**On-page (measured from live crawl):**
- Homepage title **and** meta description are the placeholder *"This site is used to help customers look into our company."*
- Homepage H1 is pure emotion ("We care about YOU and YOUR belongings…") — no service or location keyword.
- **No service pages** — service cards link to `#`.
- **No location pages** — the 8 counties appear as unlinked homepage text.
- "Projects" = three unlabeled photo galleries ("Project One/Two/Three") — local proof wasted.

**Technical (Screaming Frog):**
- **42 `noindex` URLs (24.85%)** — most urgent unaddressed finding.
- Duplicate **titles, meta descriptions, and H1s** clustered at ~48–51 URLs each — a single root cause: the **Gutenverse** plugin/templating, not hundreds of page-level errors.
- ~93 crawled URLs **dominated by WordPress image-attachment pages** (crawl bloat).
- One thin-content page flagged (a content-library push is **not** justified by the data).
- Image optimization, weak internal linking, HTTP/HTTPS and mixed-content items to resolve at migration.

## Strategic Recommendation

Do not patch the WordPress site. **Carry these findings into the .NET migration spec** (Section 07) so the new platform ships with unique template-level metadata, clean indexation rules, suppressed attachment URLs, and a real internal-linking model.

## Implementation Plan

Translate each finding into a migration acceptance criterion: unique `<title>`/H1 per template, canonical + indexation policy, 301 map, attachment-page suppression, image pipeline, HTTPS-only. Validated by a pre-launch staging crawl.

## Expected Business Impact

Eliminates the entire duplicate-metadata class at the root, removes crawl bloat, and gives every future page a clean technical baseline — the precondition for ranking anything.

## KPIs

Indexed real pages (target ↑ from ~7), `noindex`/duplicate counts (→ 0 on content pages), crawl-to-content ratio, Core Web Vitals at launch.

## Next Steps

See [04 · SWOT](../04-SWOT-Analysis/README.md) and [07 · Technical SEO & Migration](../07-Technical-SEO-Audit/README.md).

---
[← Back to overview](../README.md)
