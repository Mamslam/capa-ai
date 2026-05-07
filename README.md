# CAPA AI

AI-drafted CAPA (Corrective and Preventive Action) reports for EU pharmaceutical SMEs.

**What it does:** Takes a deviation description + root cause category → generates a draft CAPA report as a .docx download following EU-GMP Part I Chapter 8 format.

**Who it's for:** QA Managers at 50–200 employee EU pharma companies writing 5–20 CAPAs/month.

**Status:** Pre-build — validating with pharma QA managers before coding.

---

## The Problem

EU pharma QA managers spend 2–4 hours writing each CAPA report manually in Word.
At 10 CAPAs/month, that's 20–40 hours of QA staff time on a formulaic, templated document.
No AI-native tool exists for this segment. Legacy QMS (Veeva, MasterControl) is enterprise-only.

## Output Format

Each generated CAPA includes:
1. Deviation / nonconformance description
2. Immediate action taken
3. Root cause analysis (5 Whys or Ishikawa)
4. Corrective action (what, who, by when)
5. Preventive action (systemic change)
6. Effectiveness check criteria + verification date
7. Responsible person + QA reviewer
8. Target closure date

All output is labeled **DRAFT — requires QA review and sign-off.**
No content is stored server-side (stateless by design, GDPR-safe).

## Stack

```
Frontend   → Next.js → Vercel
Backend    → Express + Node.js → Railway
AI         → Claude API (anthropic)
Export     → .docx generation (docx npm package)
Auth       → none on MVP (freemium: 10 free, then €49/month)
```

## Pricing

- Free: 10 CAPAs (no account required)
- Pro: €99/month per company — unlimited CAPAs, unlimited QA team members

## Design Doc

Full design: `docs/design.md`

---

*MLT Web Services · Essen, Deutschland*
*Built with Claude Code + gstack*
