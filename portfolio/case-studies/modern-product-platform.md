# Case study: Modern product platform

**Domain:** Web product, customer experience, and internal operations  
**Code visibility:** Private commercial repositories; this is a sanitized overview.

## Context

A product-oriented web platform requires both a visitor-facing interface and an internal interface to support day-to-day operational tasks. These are distinct user experiences, even when they work within the same business.

## Engineering scope

The source projects contain two distinct frontend applications:

- A **Next.js and TypeScript** customer-facing application
- A **React, TypeScript, and Vite** administrative dashboard

The inspected package manifests include React Query / TanStack Query for asynchronous data flows, Axios for HTTP communication, and Zod in the Next.js application for schema validation.

## Technical themes

- Organizing large user-facing workflows into reusable React components
- Separating customer and operational interfaces by application
- Working with asynchronous API state and typed frontend code
- Managing forms, loading states, and validation across product journeys
- Supporting maintainable frontend development in a commercial setting

## What an interviewer can explore

1. When two interfaces should share packages and when they should remain separate
2. Handling loading, errors, retries, and cache invalidation around API requests
3. Structuring validation at the UI boundary
4. Designing component boundaries for features that evolve over time

## Evidence and boundaries

This summary is informed by the inspected private frontend repositories. It **does not** publish their source, internal APIs, deployment settings, customer information, or commercial metrics. No claims about measured improvements or production uptime are made.

[← All case studies](../README.md)
