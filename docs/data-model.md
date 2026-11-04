# Proposed data model

**Status:** Conceptual; implementation-neutral

The model separates companies, locations, jobs, sources, and verification events. This supports multiple sources per fact, changing job status, and possible future regional expansion.

## Entities

### Company

| Field | Meaning |
|---|---|
| `id` | Stable internal identifier. |
| `name` | Display name. |
| `alternate_names` | Known trading names or aliases, when useful. |
| `description` | Short factual summary. |
| `industry` | Primary industry classification used for filtering. |
| `company_type` | Optional organization type, such as public, private, government, or not-for-profit when known. |
| `website_url` | Official company site. |
| `employee_range` | Approximate range, not a false-precision count. |
| `employee_range_as_of` | Date or period the range describes, if available. |
| `valuation` | Optional public valuation record; see below. |
| `record_status` | Draft, published, under review, or archived. |
| `created_at`, `updated_at` | Record timestamps. |

### Location

| Field | Meaning |
|---|---|
| `id` | Stable identifier. |
| `company_id` | Related company. |
| `label` | Office/site name if available. |
| `address_or_locality` | Publicly appropriate location detail. |
| `region` | Geographic region, initially Greater Perth. |
| `is_headquarters` | Whether the source identifies this as headquarters. |
| `source_id` | Source supporting the location. |

### Job

| Field | Meaning |
|---|---|
| `id` | Stable identifier. |
| `company_id` | Hiring company. |
| `title` | Published job title. |
| `description_url` | Original job post URL. |
| `apply_url` | Direct application URL if distinct and available. |
| `location_text` | Published location or remote description. |
| `employment_type` | Full-time, part-time, contract, casual, internship, or unknown. |
| `salary_min`, `salary_max`, `salary_currency`, `salary_period` | Optional published salary details; retain original context. |
| `first_seen_at` | First observed by BizBeacon. |
| `posted_at` | Posting date if supplied by the source. |
| `last_verified_at` | Most recent successful check. |
| `status` | Active, stale, closed, or removed. |

### Source

| Field | Meaning |
|---|---|
| `id` | Stable identifier. |
| `publisher` | Employer, official registry, job board, or other publisher. |
| `url` | Source page. |
| `source_type` | Company site, job listing, public filing, directory, or other. |
| `accessed_at` | When source was checked. |
| `usage_notes` | Applicable source constraints or review notes. |

### Fact evidence / verification event

Record the entity and field checked, source used, observed value or status, review timestamp, reviewer/process, and outcome. Keep enough history to understand why a value changed. Avoid retaining unnecessary personal information about reviewers.

## Valuation representation

Valuation should be optional and typed rather than a generic number:

- Value and currency.
- Valuation type, such as market capitalization or reported funding-round valuation.
- As-of date or report date.
- Source and publication date.
- Editorial note distinguishing reported valuation from current market value.

Do not combine unlike valuation types into a single comparison without clear explanation. If no credible public figure is available, store no value and render “Not publicly available” or omit the section.

## Relationships

- One company can have multiple locations, jobs, and sources.
- A source can support more than one fact, and a fact can have more than one source.
- Each job belongs to one company and may reference separate description and application URLs.
- Verification events attach to a record or individual fact.

## Data rules

- Use stable identifiers; company names and URLs can change.
- Normalize URLs and avoid duplicate jobs where the same employer post appears in several places.
- Preserve the original published wording for salary and work location where normalization could distort meaning.
- Distinguish “unknown,” “not applicable,” and “not publicly available.”
- Store dates with an explicit timezone strategy; display dates in the user's locale.
- Record only data needed for directory functionality and operations.
