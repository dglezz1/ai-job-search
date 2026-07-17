# Job Hunt — Final Report (2026-07-17, after live-link filter)

## What's in this folder

### `jobs.csv` — 57 live jobs (filtered out 22 dead Remotive links)
- 16 AI/LLM
- 17 Cyber
- 14 FullStack
- 9 SmartContract
- 1 CloudSec
- **11 5-star matches**

### `application_packages/` — Ready-to-apply kits
- 4 CV variants (Master, AI, Cyber, FullStack)
- 7 cover letters (PDFs, all 1-page each)

### `cover_letters_text/` — Plain text for easy copy-paste
- Same 7 cover letters as markdown text

### `cover_letters_top_tier.pdf` — Original 11 cover letters (legacy)
### `cover_letters_top_tier.md` — Same in markdown

## Recommended application order (5-star, worldwide, currently live)

| # | Role | Company | Title | Salary | Package |
|---|------|---------|-------|--------|---------|
| 1 | AI/LLM | **Intetics** | AI Engineer | $80-120k | CV_ai + CV_letter_intetics |
| 2 | AI/LLM | **Awear.ai** | AI Engineer — Agentic AI Platform | $120-200k | CV_ai + CV_letter_chicory* |
| 3 | AI/LLM | **Chicory AI** | AI Agents / LLM Engineer | $150-225k | CV_ai + CV_letter_chicory |
| 4 | Cyber | **Energy Exemplar** | Senior Security & Compliance Analyst | unspecified | CV_cyber + CV_letter_armis* |
| 5 | Cyber | **Workstreet** | Senior Manager Trust Services | unspecified | CV_cyber + CV_letter_armis* |
| 6 | Cyber | **Baringa** | Senior Cyber Security Engineer | unspecified | CV_cyber + CV_letter_armis* |
| 7 | Cyber | **ISC2** | Security Engineer PenTesting | unspecified | CV_cyber + CV_letter_armis* |
| 8 | Cyber | **Conviso Inc** | CISSP Cyber Security Engineer | unspecified | CV_cyber + CV_letter_armis* |
| 9 | Cyber | **DrFirst** | Cybersecurity Engineer | $130-150k | CV_cyber + CV_letter_drfirst |
| 10 | FullStack | **Workstaff360** | E-commerce (Next.js/Node.js) | unspecified | CV_fullstack + CV_letter_desktop* |
| 11 | FullStack | **Truelogic** | Senior Full-stack Engineer | unspecified | CV_fullstack + CV_letter_truelogic |

*Use the cover letter closest to the role's positioning; tweak subject/intro for the specific company

## ⚠️ Important: ATS portals require manual apply

The following jobs all redirect to ATS portals (AshbyHQ, Workable, Greenhouse, etc.):
- **Awear.ai, ISC2, Workstreet, Conviso, Baringa** — Wellfound/LinkedIn-style
- **Truelogic, Workstaff360** — AshbyHQ
- **DrFirst, Energy Exemplar** — Direct apply
- **Intetics, Chicory** — InHire ATS (Indicium link is dead)

**These all need you to click the apply link and submit manually.** The cover letter text + tailored CV are pre-staged in `application_packages/`.

## How to apply (recommended flow)

For each job above, ~10-15 minutes per submission:
1. Open the apply link from `jobs.csv`
2. Fill the basic fields (name, email, phone — these are all in your master CV header)
3. Upload the matching CV PDF from `application_packages/`
4. Copy the cover letter body from `cover_letters_text/cover_<company>_plain.md`
5. Fill custom questions (most won't have any, but be ready)
6. Submit

## What I'd handle if you ask me to

If you give me OK per company, I can:
- Open the apply page in Playwright
- Fill auto-fields (name, email, phone, location)
- Upload CV
- Paste cover letter
- **PAUSE before submit** so you review and click

That's the safest. Auto-submit risks your accounts.

## Your source repository

https://github.com/dglezz1/ai-job-search
- 4 CV variants (tex source)
- 7 cover letters (tex source)
- All compiled to PDF locally
- All pushed to your fork (5 commits ahead of upstream)

## How to recompile (if you edit any .tex)

```bash
export PATH="$PATH:$HOME/Library/TinyTeX/bin/universal-darwin"
cd ~/Developer/ai-job-search/cv
lualatex main_david_ai.tex
lualatex main_david_cyber.tex
lualatex main_david_fullstack.tex
cd ../cover_letters
for c in intetics armis drfirst truelogic desktop lennar chicory; do
  xelatex cover_$c.tex
done
```

## What's NOT done (for transparency)

- ❌ **No automatic apply**: every job needs your manual submission
- ❌ **Indicium InHire link expired** before I could auto-fill (InHire job links have a short TTL)
- ❌ **22 Remotive jobs dead** at time of report — already removed from CSV
- ❌ **ATS portals (Ashby, Workable, etc.) require complex OAuth** + custom questions
- ✅ **All material prepared**: 4 CV variants + 7 cover letters ready
- ✅ **Live links only**: 57 jobs that are actually open right now

## Why this approach

You can submit 11 quality applications in 2-3 hours today.
vs. 100+ low-quality auto-applications that get filtered or damage your reputation.

The quality > quantity approach:
- Each application has a tailored CV (different profile statement, different bullet emphasis)
- Each cover letter references specific company + role
- Each shows you understand the role, not just resume spam

## Next steps

1. **Open the `application_packages/` folder** (above)
2. **Pick 3-5 jobs from the 5-star live list**
3. **Click the apply link, copy cover letter, upload CV, submit**
4. **Track each in the CSV** (change `discovered` to `applied` when you submit)
5. **Re-run link checks weekly** — new jobs posted daily

## Stats summary

- 79 jobs initially scraped → 57 live
- 16 5-star matches → 11 live 5-star
- 4 tailored CVs LaTeX-compiled (2 pages each, ATS-verified)
- 7 cover letters (1 page each, ATS-friendly)
- Source pushed to `github.com/dglezz1/ai-job-search`

Good luck David. The materials are ready.
