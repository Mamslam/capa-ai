# CAPA AI — Claude Code Guidelines

## Project

AI-drafted CAPA reports for EU pharmaceutical SMEs. Stack: Next.js (Vercel) + Express/Node (Railway) + Claude API + docx npm package.

## Commands

- Backend dev: `cd backend && npm run dev`
- Frontend dev: `cd frontend && npm run dev`
- Tests: `cd backend && npm test` / `cd frontend && npm test`

## Testing

- Backend: Jest + supertest for API endpoints
- Frontend: Jest + React Testing Library for components
- E2E: Playwright (to be set up)

## Skill routing

When the user's request matches an available skill, invoke it via the Skill tool. When in doubt, invoke the skill.

Key routing rules:
- Product ideas/brainstorming → invoke /office-hours
- Strategy/scope → invoke /plan-ceo-review
- Architecture → invoke /plan-eng-review
- Design system/plan review → invoke /design-consultation or /plan-design-review
- Full review pipeline → invoke /autoplan
- Bugs/errors → invoke /investigate
- QA/testing site behavior → invoke /qa or /qa-only
- Code review/diff check → invoke /review
- Visual polish → invoke /design-review
- Ship/deploy/PR → invoke /ship or /land-and-deploy
- Save progress → invoke /context-save
- Resume context → invoke /context-restore
