# Perth Company and Hiring Directory

## Project brief

**Working name:** BizBeacon Perth  
**Status:** Concept brief  
**Initial market:** Greater Perth, Western Australia  
**Future direction:** Expand to other Australian regions if the Perth service proves useful and sustainable.

## Summary

BizBeacon will help people discover companies operating in Perth and understand what those companies do, how large they are, and whether they are hiring. Each company profile will bring together useful public information and links to original sources, including a direct link to apply for an open role when available.

The service should be a maintained, searchable directory rather than a one-time list. Its value depends on clear sourcing, visible update dates, and careful treatment of information that may be incomplete or change quickly.

## Problem and opportunity

Company information and job openings are spread across employer career pages, job boards, company websites, and other sources. People looking for work or researching the local economy may have to repeat the same searches and still lack a useful picture of an employer.

BizBeacon can make that discovery easier by connecting company profiles, current hiring information, and simple market-level views in one Perth-focused experience.

## Target users

- Job seekers exploring Perth employers and current openings.
- Students, graduates, and career changers learning about local industries.
- People comparing employers by industry, location, or approximate size.
- Researchers and local ecosystem participants looking for a structured view of companies and hiring activity.

## Product goals

1. Make it easy to find companies in Perth by name, industry, location, and size.
2. Show current or recently verified job openings with a reliable route to the employer's application page.
3. Help users understand the source, freshness, and confidence of company and hiring information.
4. Build a data and product foundation that can later support additional regions.

## Initial scope

### Company directory

Each company record should support:

- Company name and, where useful, trading name.
- Industry or company type.
- Perth-area location and headquarters location when known.
- Short description and company website.
- Approximate employee range, with source and verification date.
- Public company value information only when a credible, attributable figure is available.
- Profile last-checked date and links to relevant sources.

### Hiring information

Each job record should support:

- Job title, employer, and work location or remote status.
- Employment type and salary range when published.
- Original job listing source and direct apply link.
- First-seen and last-verified dates.
- Status such as open, closed, or unverified.

### Discovery and insight views

The first experience should prioritize search, filters, and company profiles. Useful initial filters include industry, Perth subregion, employee range, and currently hiring. A lightweight hiring overview can summarize active listings by company or industry once the underlying data is sufficiently reliable.

## Out of scope for the first release

- A claim that the directory contains every company in Perth.
- Unsupported or inferred valuations for private companies.
- Complex recruiting, applicant tracking, or employer CRM features.
- Automated hiring trend claims without enough historical data and validation.
- Expansion beyond Perth before the local data and update process are working well.

## Data quality and update principles

- Prefer company-owned pages and reputable public sources; record the source for each changing or material fact.
- Show when a listing or profile was last checked.
- Treat employee counts as ranges or estimates unless the source supports a precise figure.
- Treat company value as optional. For private companies without a trustworthy public valuation, display “Not publicly available.” For listed companies, label the figure, source, and date clearly; market value changes over time.
- Mark stale or uncertain job listings for rechecking, and remove or close them when verified no longer active.
- Avoid implying a relationship with an employer unless that relationship exists.
- Review source terms and applicable privacy, copyright, and data-use requirements before collecting or republishing information at scale.

## Product principles

- **Useful before comprehensive:** Start with a high-quality, well-defined slice of Perth employers.
- **Evidence visible:** Users can see where important information came from and when it was checked.
- **Link to the source:** Applications should go to the employer or original listing wherever possible.
- **Honest about uncertainty:** Use ranges, dates, and “unknown” states instead of false precision.
- **Local first, extensible by design:** Model region and location as data so future geographic expansion does not require a redesign.

## Success measures

For an initial pilot, track:

- Number of useful company profiles with verified sources.
- Share of active job listings with a working direct application link.
- Freshness of job records and company size information.
- Search-to-profile and profile-to-apply click-through rates.
- Repeat use, saved companies, or alert sign-ups if those features are introduced.
- User reports of stale, incorrect, or missing information.

Set numeric targets after a baseline and pilot cohort are defined.

## Suggested phased delivery

### Phase 1: Validate the concept

- Select a manageable set of employers across a few Perth industries.
- Confirm what users most need to compare and which data can be sourced consistently.
- Test a simple directory and profile experience with working source and apply links.

### Phase 2: Build the Perth MVP

- Add search and core filters.
- Add company profiles, size ranges, and active job listings.
- Add freshness indicators and a repeatable verification workflow.
- Measure whether people find relevant companies and reach application pages.

### Phase 3: Improve coverage and insight

- Expand Perth employer coverage based on user demand and data quality.
- Add saved searches, alerts, or hiring summaries if the pilot supports them.
- Improve refresh automation while retaining source checks and visible dates.

### Phase 4: Consider expansion

- Evaluate regional coverage, source availability, operating cost, and user demand.
- Add another region only when the Perth update process is dependable.

## Key risks and responses

| Risk | Response |
|---|---|
| Job posts become stale | Record verification dates, recheck regularly, and label uncertain records. |
| Employee counts or valuations are misleading | Use ranges and dated sources; make valuation optional and never invent a figure. |
| Source coverage is incomplete | State the directory's coverage honestly and prioritize quality over a “complete list” claim. |
| Data collection is costly or restricted | Review source terms and costs early; start with sources that support sustainable use. |
| Users do not find enough value | Pilot with target users and measure search, profile, and apply-link behavior before broad expansion. |

## Open decisions

- Which first user group should the pilot serve most directly: job seekers, students, or local business researchers?
- Which Perth industries should be included in the first employer set?
- What refresh cadence is realistic for job posts and company details?
- Which public and employer-provided sources can be used sustainably?
- Should employers be able to claim or suggest edits to their profiles in a later phase?
- What is the preferred technical approach for directory search, data refresh, and source tracking?

## Reference concepts

The supplied screenshots are treated as visual and feature inspiration, not requirements. They suggest a searchable company table with filters, employee ranges, company profiles, hiring dashboards, job-post analytics, and open-role lists. BizBeacon should adapt these ideas to a Perth job-discovery use case, with strong source and freshness indicators.

## Proposed next step

Agree on the pilot audience and initial Perth industry slice, then produce a short MVP requirements document covering the first screens, data fields, sourcing workflow, and acceptance criteria.
