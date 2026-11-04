# Technical architecture outline

**Status:** Conceptual; no technology selected

## Design goals

- Support a searchable, mobile-friendly Perth directory.
- Keep source provenance and verification history with the data.
- Make it possible to add regions without redesigning core records.
- Allow content to be corrected or removed through a controlled workflow.
- Start with a small, maintainable system and scale only when usage and data volume require it.

## Logical components

```text
Public web experience
        |
Application/API layer  <---->  Editorial interface or controlled admin workflow
        |
Relational data store
        |
Refresh and link-check jobs (optional, staged)
        |
External company and job sources
```

### Public experience

Directory search, filters, company profiles, job previews, source links, checked dates, and correction reporting. Public pages should not expose internal notes or unpublished records.

### Application/API layer

Validates and serves published records, supports search and filters, records appropriate usage events, and applies access controls to editorial functions.

### Data store

A relational model is a reasonable starting point because companies, locations, jobs, sources, and verification events have clear relationships. Search can begin with database capabilities; a separate search service is only needed if measured relevance or scale justifies it.

### Editorial workflow

Initially this may be a restricted admin interface or a documented manual workflow. It should support draft/review/published/archived status, field-level source references, correction, and verification history.

### Refresh jobs

Optional scheduled processes can check job URLs and notify editors of likely changes. They should not publish uncertain status changes without review until accuracy is demonstrated.

## Environments and access

- Separate local development, preview/staging, and production data.
- Restrict editorial actions to authorized users; use role-appropriate access.
- Keep secrets out of source control and use environment-specific secret storage.
- Back up production data and document restore procedures before launch.
- Use logs that support debugging without storing unnecessary personal data.

## Security and privacy requirements

- Collect the minimum user data needed for chosen features.
- Avoid user accounts in the first release unless validation shows they are necessary.
- Protect admin routes and validate inputs and external URLs.
- Use secure transport and standard protections appropriate to the chosen framework and host.
- Define retention for logs, correction reports, and backups.
- Review third-party analytics and hosting data practices before selecting providers.

## Observability

Track application errors, broken outbound links, refresh failures, data freshness, and correction response time. Keep product analytics limited to events needed to answer the MVP hypotheses.

## Stack selection criteria

Choose implementation technologies after confirming team skills and deployment constraints. Compare options on:

- Development and maintenance effort.
- Search and filtering needs.
- Editorial workflow support.
- Hosting and operating cost at pilot scale.
- Security updates and ecosystem maturity.
- Portability and data export.
- Accessibility support and performance.

No framework, hosting provider, or data vendor is mandated by this document.
