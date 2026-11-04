# MVP scope and user flows

**Status:** Draft for validation

## MVP outcome

A user can search a curated set of Perth-area employers, understand the basic company profile, see currently verified job links, and reach the original application page. An editor can maintain the underlying records with sources and review dates.

## Included

- Public company directory with name search and a small set of useful filters.
- Company profile pages.
- Current job listings linked to original sources.
- Industry, Perth-area location, and employee range where supported by sources.
- Source attribution and last-checked dates for changing facts.
- Simple editorial workflow for adding, correcting, checking, and closing records.
- Basic usage and data-quality measurement.

## Deferred

- User accounts, saved lists, alerts, and personalization.
- Employer self-service profile management.
- Full regional job-post analytics, salary histograms, and hiring trend forecasts.
- Paid employer promotion or subscription features.
- Automated scraping or enrichment at scale before source permission and reliability are established.
- Expansion beyond Perth.

## Primary screens

1. **Directory:** search, filters, result count, company cards or table, and clear empty state.
2. **Company profile:** summary, industry, location, size range, sources, open roles, and last checked.
3. **Job detail or preview:** role, employer, location, known conditions, source, checked date, and apply link.
4. **Editorial workspace:** record status, source details, verification date, and correction history. This can initially be a restricted internal tool or a controlled process rather than a public-facing admin product.

## User flows

### Find a company by sector

1. User opens the directory.
2. User selects an industry and optionally location or employee range.
3. Results update and show enough information to compare employers.
4. User opens a company profile and follows its website or job link.

### Find an open role

1. User searches or filters for companies currently hiring.
2. User opens a relevant company profile.
3. User reviews available roles and their locations and checked dates.
4. User follows the labeled original listing/apply link.

### Check reliability

1. User sees a company size or job listing.
2. User can see the source and when BizBeacon last checked it.
3. If a fact is missing or uncertain, the interface says so rather than showing a fabricated value.
4. User can report a stale or incorrect item.

### Maintain a listing

1. Editor receives a new record or correction.
2. Editor checks the original source and records the source URL and review date.
3. Editor publishes, updates, marks stale, closes, or removes the record.
4. Review history records what changed and why.

## Acceptance criteria for a pilot

- A user can complete company search and open a profile on a mobile viewport.
- A user can identify the source and checked date for a job and company-size claim.
- Every job shown as active has a tested destination at the time of verification.
- Missing data is represented consistently and does not break search or layout.
- An editor can correct or close a record without losing its source history.
- The pilot dataset is explicitly described as selected coverage, not a complete Perth census.

These criteria are proposed and should be adjusted after user research and implementation planning.
