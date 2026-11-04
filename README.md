# BizBeacon

BizBeacon is a proposed Perth-first company and hiring directory. It helps people explore local employers, see what they do and where they operate, review current job opportunities, and follow links to original sources and application pages.

The project is at concept and planning stage. The documents describe the intended product and a practical validation path; they do not imply that a live service, complete company dataset, or automated refresh system exists yet.

## Start here

- [Open the demo](index.html) — dependency-free browser prototype with interactive search, filters, saved companies, profile previews, and a $1 employer-offer concept.
- [Project brief](docs/perth-company-and-hiring-directory-project-brief.md) — purpose, principles, phases, and open decisions.
- [Product requirements](docs/product-requirements.md) — users, requirements, and success measures.
- [MVP scope and user flows](docs/mvp-scope-and-user-flows.md) — first release boundaries and key journeys.
- [Data model](docs/data-model.md) — proposed records, fields, and relationships.
- [Data sourcing and operations](docs/data-sourcing-and-operations.md) — source handling, verification, freshness, and corrections.
- [Technical architecture](docs/technical-architecture.md) — implementation-neutral system outline.
- [Roadmap and validation](docs/roadmap-and-validation.md) — staged delivery and decision gates.
- [Risk and governance](docs/risk-and-governance.md) — product, data, and operational risks.

## Current product boundary

The initial geography is Greater Perth, Western Australia. The directory should communicate its coverage honestly; “all companies in Perth” is not an MVP promise. Company size should generally be shown as a sourced range. Company valuation is optional and should appear only when a credible public figure is available with a date and source. Job listings should link to the original listing or employer application page and show when they were last checked.

## Demo

Open `index.html` in a modern browser. The prototype uses fictional example companies and sample roles to demonstrate the experience; none are verified employers or live vacancies. Search, filters, sorting, saved-company controls, profile previews, and the employer offer modal work in the browser. The $1 offer is a checkout preview only: it does not take payment or send/store an inquiry. The prototype uses plain HTML, CSS, and JavaScript and has no build step.

## Repository status

This repository currently contains planning documents. Implementation choices such as the application stack, hosting, data providers, refresh automation, and pilot industries remain open until validated.
