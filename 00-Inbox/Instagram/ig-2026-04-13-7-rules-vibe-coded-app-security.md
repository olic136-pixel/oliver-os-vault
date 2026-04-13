---
type: inbox
status: active
projects:
  - '[[Qanun-Platform]]'
  - '[[Qlarifai-CRM]]'
  - '[[TradeDar]]'
  - '[[Fuutura-Exchange]]'
  - '[[Human8-BIT]]'
  - '[[Human8-Nodex]]'
entities: []
jurisdictions: []
people: []
tags:
  - instagram
  - security
  - vibe-coding
  - app-development
  - authentication
  - best-practices
  - claude-code
created: '2026-04-13'
last_reviewed: '2026-04-13'
source: instagram
instagram_url: 'https://www.instagram.com/p/DXAhfExDolr/'
instagram_author: '@andrewcodesmith'
---
# 7 Rules of App Security for Vibe-Coded Apps

> Saved from Instagram — @andrewcodesmith, 2026-04-13

## Core Insight
A senior software engineer outlines the 7 most critical security rules that vibe-coded (AI-generated) apps consistently get wrong. The core thesis is that security doesn't require perfection — it requires nailing the 20% of practices that prevent 80% of the damage. This is especially timely as AI-assisted coding accelerates development speed but often skips security fundamentals. Highly relevant given Oliver's extensive use of Claude Code and AI-assisted development across multiple projects.

## Key Points
- **Authentication on the server only:** "You're logged in" must be decided by the backend, not the frontend. Use Supabase, Auth0, JWT — never let the client fake identity.
- **Authorisation on every action:** Being logged in doesn't mean you can do anything. Every sensitive API call must check "can this user touch this specific record?" — never trust UI-side guards only.
- **Treat all input as untrusted:** Form fields, URL params, API payloads, even AI-generated inputs — always validate, sanitise, and use parameterised queries or safe ORM patterns to block injection.
- **Secrets never in client/git:** Never put API keys, JWT secrets, DB passwords, or admin tokens in the frontend, mobile app, or repo config files. Use environment variables or secure secret storage (Vault, AWS Secrets, Supabase secrets).
- **Keep dependencies updated:** Vibe-built apps are often half third-party libraries that go unchecked. These are actively targeted (referenced the Axios hack). Keep packages updated and check for known vulnerabilities.
- **Default to safer settings:** Default to least-privilege roles, short-lived tokens, HTTPS, and strict CORS/CSRF protections instead of leaving everything wide open.
- **Log suspicious activity, not passwords:** Log important events, failed logins, and suspicious behaviour, but never log passwords, tokens, or sensitive user data.

## Relevance to Active Work
Critical checklist for all of Oliver's active software projects: [[Qanun-Platform]], [[Qlarifai-CRM]], [[TradeDar]], [[Fuutura-Exchange]], [[Human8-BIT]], and [[Human8-Nodex]]. These security rules should be incorporated into the development standards and code review processes across all projects. Particularly important given the vibe-coding approach being used with Claude Code.

## Action Items
- [ ] Audit all active projects against these 7 security rules
- [ ] Ensure server-side auth is implemented in Qanun-Platform and Qlarifai-CRM
- [ ] Check that no secrets are committed to any GitHub repos
- [ ] Set up dependency vulnerability scanning (e.g., npm audit, Dependabot) across projects
- [ ] Create a security checklist document for all new project scaffolding

## Source Content
**Author:** @andrewcodesmith
**Caption:** 7 rules of app security (from a senior software engineer). Security isn't about doing everything perfectly, it's about nailing the 20% that stops 80% of the damage.
**URL:** [View on Instagram](https://www.instagram.com/p/DXAhfExDolr/)

## Visual Notes
The video shows a man sitting at a desk with a typewriter, with retro pixel-art graphics overlaid showing computer icons, a skull emoji, and monitors. The title "7 sins of vibe coded apps" appears in cyan/purple pixel font. The setting has a wooden beam ceiling suggesting a loft-style workspace.
