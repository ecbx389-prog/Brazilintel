# Brazil Intel

**Intelligence & Risk Advisory**

> **Brazil is complex. Your decisions should not be.**

Brazil Intel is a Brazil-focused intelligence and risk advisory boutique serving international organizations that need decision-grade understanding before investing, operating, entering a market, selecting partners or assuming exposure in Brazil.

The firm supports high-stakes decisions through lawful multi-source research, enhanced due diligence, corporate intelligence, market-entry intelligence, geopolitical risk analysis, security intelligence and strategic OSINT.

## Core promise

**Reduce uncertainty before capital, reputation or operations are exposed.**

Brazil Intel turns fragmented information into structured assessments designed to clarify what is verified, what is relevant, what is connected, what remains uncertain and which risks deserve scrutiny before a consequential decision is made.

## Brazil expertise

Brazil Intel is built around a multidisciplinary network of specialists who live in, work in and understand Brazil.

The network includes professionals with backgrounds in defense, public security, intelligence, cybersecurity, academia and corporate risk. Many have spent their careers operating, researching and analyzing Brazil's institutional, economic and security environments.

This background does **not** imply access to classified, restricted or privileged government information. Brazil Intel relies on lawful collection, structured analysis and independently verifiable or appropriately licensed sources.

## Capabilities

- Enhanced Due Diligence
- Corporate Intelligence
- Market Entry Intelligence
- Geopolitical Risk
- Security Intelligence
- Strategic OSINT

## Analytical method

1. Intelligence Requirement
2. Collection Plan
3. Verification
4. Analysis
5. Alternative Analysis
6. Decision Support

Material products distinguish, when appropriate, between **fact, assessment, hypothesis and confidence level**.

## Principles

- Lawful collection
- Source integrity
- Analytical rigor
- Alternative analysis
- Explicit uncertainty and confidence
- Confidentiality
- Independence
- Human-led, technology-enabled analysis

## Public payment positioning

Digital asset settlement may be available for approved engagements. Client identification, compliance screening, invoicing and applicable accounting requirements remain part of the engagement process.

## Website

The static website is implemented in `index.html` and is designed for direct deployment through GitHub Pages, Cloudflare Pages or another static hosting service. No build step is required — it is plain HTML/CSS with a small inline script for the intake form.

Supporting production files:

- `favicon.svg` — brand mark favicon
- `robots.txt` — allows crawling; a `Sitemap:` line will be added once a public URL exists
- `_headers` — baseline security headers for Cloudflare Pages / Workers static assets (`nosniff`, frame denial, referrer policy, restrictive permissions policy)
- `wrangler.jsonc` — Cloudflare Workers (static assets) configuration; needed because this project was connected through Cloudflare's "Import a repository" (Workers Builds) flow, which deploys with `wrangler deploy` rather than the classic Pages build pipeline. It serves the repository root as the static asset directory.
- `.assetsignore` — keeps non-site files (`README.md`, `wrangler.jsonc`, `.git`, `.github`) out of the deployed static assets

`sitemap.xml`, the `canonical` link and the Open Graph `og:url` tag are intentionally not yet present — they require a real, deployed URL and will be added after the first successful deployment rather than pointing at an invented domain.

## Intake form

The "Submit a Requirement" form has no backend yet. Submitting it clears the fields client-side and shows: "Secure intake is being activated. Please return shortly." No form data is sent to any service or stored anywhere. Do not wire this form to a third-party form service (e.g. Formspree) without explicit authorization.

## Deployment status

A Cloudflare Workers project named `brazilintel` was created via the dashboard's "Import a repository" flow, deploying from the `main` branch with `npx wrangler deploy`. `main` does not yet include this repo's production-readiness changes (they live on this PR's branch) and, before `wrangler.jsonc` was added, `wrangler deploy` had no assets/entry-point configuration to work from. Merge this PR to `main` to get both fixes live at once.
