# Product requirements

**Status:** Draft for validation  
**Product:** BizBeacon Perth

## Product statement

BizBeacon helps people discover employers operating in Perth and understand their industry, location, approximate size, and current hiring opportunities. It presents useful public information with sources and checked dates, then directs users to the original employer or job listing.

## User needs

- As a job seeker, I want to find Perth employers hiring for relevant roles so I can reach the original application page.
- As a student or career changer, I want to browse companies by industry and approximate size so I can learn about possible career paths.
- As a person comparing employers, I want to inspect location, company type, and available company information with clear sources.
- As a directory editor, I want to add, correct, verify, and retire records so the public directory stays useful.

## Goals

1. Make employer discovery in Perth faster and more navigable.
2. Provide useful links to active job opportunities.
3. Make source, freshness, and uncertainty visible.
4. Establish a repeatable data process before broadening coverage.

## Non-goals for MVP

- Guaranteeing a complete list of Perth businesses.
- Accepting applications or replacing employer recruitment systems.
- Ranking employers by quality, safety, or desirability.
- Predicting company value or publishing unsourced private-company valuations.
- Making hiring-market forecasts before sufficient validated history exists.
- Expanding to other cities before the Perth operation is viable.

## Functional requirements

### Discovery

- Users can search companies by name.
- Users can filter the directory by industry, geographic area, employee range, and hiring status when data is available.
- Results show company name, industry, Perth-area location, employee range when known, and hiring indicator.
- Empty and partial-data states explain what is unavailable and provide a useful next step.

### Company profile

- A profile can show name, description, industry, location, website, employee range, and open jobs.
- Material facts show a source and a last-checked date or a clear unavailable state.
- Private-company value is not estimated. A public market value, if included, carries its definition, currency, source, and as-of date.

### Job discovery

- A job card shows title, employer, location or remote status, employment type when known, and posted/checked dates when available.
- The apply action goes to the original job listing or employer's application page.
- Jobs with uncertain status are not presented as confirmed active listings.
- Broken or closed links can be reported and routed to review.

### Content operations

- Editors can create and update company and job records and retain source references.
- Editors can mark records verified, stale, closed, or removed.
- Corrections can be traced to a source and a review event.

## Quality requirements

- Core directory pages should work on mobile and desktop.
- Users should be able to distinguish verified facts from estimates or missing data.
- Search and filters should remain understandable when the dataset is small.
- External links should be clearly labeled and opened safely.
- The system should support correction and removal workflows.
- Accessibility should be considered from the first interface, including keyboard use, readable contrast, and meaningful link labels.

## MVP measurement

Instrument a small set of privacy-conscious events: search submitted, filter applied, profile opened, job link clicked, and correction reported. Assess:

- Whether users can find relevant employers in moderated tasks.
- Result-to-profile and profile-to-apply click rates.
- Percentage of displayed jobs with a working application route.
- Age of last verification for active listings.
- User reports per record and time to resolve corrections.
- Repeat visits or saved searches if that feature is later included.

Numeric targets should be set after the pilot baseline is known. Do not use traffic volume alone as evidence of product usefulness.

## Assumptions to validate

- Users want an employer-first directory in addition to job-board search.
- Public information can be maintained with acceptable effort and source permissions.
- Employee ranges help users compare companies even when precise counts are unavailable.
- A focused local dataset is useful before broad coverage is achieved.
