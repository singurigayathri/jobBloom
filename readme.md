# ♛ JobBloom: run your career like a CEO

Upload any resume and get:
- **Live job ads** (LinkedIn or Indeed via Apify), ranked by AI against your resume
- **Target companies** suggested by AI, with job-board links
- **What to change** for each job: gaps, missing keywords, rewritten bullets
- An **application kit** for each job:
  - a **tailored resume** (only your real experience, rewritten for the ad), downloadable as Word or PDF
  - a **cold email**, a **cover letter (Anschreiben)** and a **motivation letter**, each in **English and German**
- **HR contacts**: emails and contact persons that the job ads actually publish (never guessed), plus recruiter search links
- **Your empire**: each application adds a tower to your skyline (XP, titles from Intern → Mogul, achievements)

You apply manually. Nothing is sent automatically.

**Live site:** https://singurigayathri.github.io/jobBloom/

## Setup (all free)
Open **⚙︎ Settings** on the site. Keys are stored only in your browser, never in this repo, and you can edit or remove them anytime.

1. **AI:** free Gemini key from https://aistudio.google.com/apikey (starts with `AQ.` or `AIza`). Anthropic keys also work (paid).
2. **Live jobs (optional):** free Apify account at https://apify.com. Copy the token from Settings → API & Integrations. The free plan includes $5/month of usage.
   - Default source: `simple.actor/linkedin-jobs` (~$0.30 per 1,000 jobs)
   - Alternative: `misceres/indeed-scraper` (set the country code, e.g. `AT`)
   - Or any other Apify actor via **Custom actor**, using an input JSON with `{{query}}`, `{{location}}`, `{{count}}`, `{{country}}`, `{{posted}}`

## Privacy
- No server, no database. Everything runs in your browser.
- Your resume goes only to the AI provider you choose. On Gemini's free tier, Google may use inputs to improve its products.
- Keys are kept for the session only, unless you tick "Remember keys on this device".

## Notes
- Scraping job sites can break when they change, so switch the source in Settings if one stops working. Check that the job board's terms are OK for your use.
- Single file: `index.html`. Edit it and push, and GitHub Pages redeploys on its own.
