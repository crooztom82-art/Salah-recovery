# OutreachPilot quality upgrades

This backup preserves the existing application features and adds safer, more accurate behavior:

- CSV export/import now preserves State / Province / Region separately from City.
- Discovery candidates are clearly treated as provisional search candidates until website analysis is run.
- Manual quick-add no longer assigns an invented 75/100 fit score or fabricated business facts; it starts as Insufficient Information.
- Discovery UI no longer claims search results are website-verified when they are only returned by a configured search provider.
- Generic fallback/outreach language avoids unsupported pricing, savings, transaction-fee, or free-plan claims.
- Existing CRM, pipeline, AI analysis, outreach, follow-ups, history, localStorage, CSV, global countries, and mobile UI remain in the project.

Validation note: the original dependency tree is intentionally not included in this source backup. A full TypeScript/Vite build should be run after dependencies are installed in the target environment.


## Live business discovery provider
- Added **Google Places API (New)** as a selectable real-business discovery provider in Settings.
- Find Prospects can query Places Text Search using country/region/city/niche/keywords and returns public business records with website/address/phone when supplied by the API.
- Results are deduplicated by website domain.
- Discovery does not invent Fit Scores; new Places candidates start as **Insufficient Information** until public website analysis/qualification runs.
- Production Google Places usage requires a Google Cloud project, Places API enabled, API key/OAuth, and billing according to Google Maps Platform requirements.
