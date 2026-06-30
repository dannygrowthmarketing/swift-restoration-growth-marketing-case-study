# 08 · Website Architecture

> A hub-and-spoke information architecture built to scale across services × counties.

## Executive Summary

The new IA is organized around two scalable hubs — Services and Service Areas — plus a Resources layer for topical authority, all interlinked so authority flows to the pages that convert.

## Business Problem

A flat brochure cannot express the service × location matrix that local SEO requires, and offers search engines no topical structure to understand or rank.

## Research Findings

Restoration demand is inherently two-dimensional (what + where). Competitors that win locally (SERVPRO of Ames) express this with dedicated service and location pages. Swift has neither.

## Strategic Recommendation

Adopt a hub-and-spoke model:
- **Services hub** → individual service pillars → sub-services (e.g., Water → basement flooding, burst pipe, sewage).
- **Service Areas hub** → county pages → city pages (Boone, Ames, Ogden, Madrid, Nevada, Des Moines, Ankeny, Waukee, Fort Dodge…).
- **Resources hub** → educational clusters (insurance, emergency guides, mold, storm, seasonal).
- **Conversion + trust pages:** Reviews, Case Studies (re-labelled Projects), About, Contact, Request Quote.
- **Internal linking:** service pillar ↔ sub-service ↔ relevant city pages ↔ insurance hub; persistent emergency CTA.

## Implementation Plan

Define page **types** in .NET (Service, Sub-Service, County, City, Article, FAQ) so new pages inherit correct templates, metadata, schema, and linking automatically — making location rollout a content task, not a dev task.

## Expected Business Impact

A structure that scales to dozens of city pages without technical debt, distributes authority to money pages, and gives search engines a clear topical map.

## KPIs

Internal links to priority pages, crawl depth to key pages (≤3 clicks), coverage of the service × location matrix, assisted conversions via internal paths.

## Next Steps

The concrete page list is in [09 · SEO Sitemap](../09-SEO-Sitemap/README.md).

---
[← Back to overview](../README.md)
