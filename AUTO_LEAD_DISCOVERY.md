# Automatic Lead Discovery

OutreachPilot now includes a **Built-in Live Web Search** discovery provider.

## How it works
1. Choose country, optional region/city, niche, desired lead count and keywords.
2. Find Prospects sends the criteria to the server.
3. The server uses Gemini with Google Search grounding to search the live public web.
4. Only businesses with a public website URL returned by search are kept.
5. Duplicate domains are removed.
6. New discoveries start as **Insufficient Information**; run **Analyze Prospect** before treating the fit score as verified.
7. Outreach remains manual — the app does not automatically contact businesses.

## Configuration
Select **Settings → Prospect Discovery → Built-in Live Web Search**. No separate search-provider API key is entered in the UI. The server uses its existing `GEMINI_API_KEY` configuration.

## Important
Google documents Google Search grounding as a real-time web-search capability with citations. Usage and billing/quotas depend on the Gemini API/project configuration; this feature does not promise unlimited free searching.
