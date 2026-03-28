# Blog Development — Human-Curated, AI-Enabled

This repo tracks the development of [blog.telogos.ai](https://blog.telogos.ai), a public blog on AI maturation in the enterprise. The blog itself is an example of the Human-Curated, AI-Enabled (HCAE) framework it discusses.

## Blog Identity

- **Author:** JD Longmire, Sr. Enterprise Architect
- **Framework:** Human-Curated, AI-Enabled
- **Voice:** Practitioner, not vendor. Honest assessments, real tradeoffs.
- **Brand:** None. No company branding, no product pitches.
- **Audience:** IT decision makers, enterprise architects, CIOs

## Platform

- **CMS:** Ghost (self-hosted)
- **URL:** https://blog.telogos.ai
- **Admin:** https://blog.telogos.ai/ghost/
- **Email:** Newsletter delivery via SMTP relay (Gmail API with OAuth)
- **Hosting:** Docker container, Cloudflare tunnel
- **Comments:** Ghost Members (email-based registration)
- **Newsletter:** Built-in Ghost newsletter on publish

## Development Process

### How We Work

This blog is developed using the HCAE framework:
- **Human** sets direction, editorial voice, strategic framing, and final approval
- **AI** handles research, drafting, technical implementation, and deployment
- Every post, feature, and configuration change follows this pattern

### Issue Tracking

All work is tracked in [GitHub Issues](https://github.com/jdlongmire/telogos-blog/issues) on this repo.

### Security Rules

**This is a public repository. Never include:**
- Passwords, API keys, tokens, or secrets
- Personal email addresses
- Service account credentials
- Internal IP addresses (Tailscale, Docker, localhost)
- Port numbers or internal architecture details
- Any information that could be used to access systems

**Instead:**
- Reference credentials as "see internal documentation" or "stored securely"
- Reference infrastructure as "self-hosted" without specifics
- Reference services by public URL only (e.g., blog.telogos.ai)
- If unsure whether something is sensitive, leave it out

### Content Workflow

1. **Idea** — captured as a GitHub issue with `content` label
2. **Draft** — AI produces initial draft based on human direction
3. **Review** — human reviews, edits, approves
4. **Publish** — published via Ghost editor or API
5. **Newsletter** — Ghost sends to subscribers on publish

### Technical Workflow

1. **Feature request** — captured as a GitHub issue
2. **Implementation** — AI implements, human reviews approach
3. **Testing** — verify functionality, audit for security
4. **Deploy** — apply to Ghost instance
5. **Document** — update this file if the process changes

## Content Guidelines

### Tone
- Direct, concise, no filler
- Technical but accessible — write for enterprise architects, not academics
- Honest about limitations and tradeoffs
- No hype, no buzzwords, no "revolutionary" or "game-changing"
- Show, don't tell — use real examples and real numbers

### Structure
- Lead with the insight, not the setup
- Use concrete examples over abstract principles
- Include data where possible (cost comparisons, timelines, metrics)
- End with implications, not summaries

### Attribution
Every post ends with:
> *This post was human-curated and AI-enabled. The architectural thinking, editorial voice, and strategic framing are mine. The research, drafting, and technical execution were AI-assisted.*

### Topics (Content Pillars)
- **AI in Ops** — how AI changes infrastructure management
- **Data Sovereignty** — why enterprises are bringing AI in-house
- **Open Source vs SaaS** — honest comparisons with real numbers
- **The Autonomous Enterprise** — agents, scheduled AI, proactive operations
- **Architecture Decisions** — real decisions, real tradeoffs, real outcomes

## For Collaborators

If you're an AI assistant working on this blog:

1. Read this file first
2. Check existing issues before creating new ones
3. **Audit every issue body and comment for sensitive information before posting**
4. Follow the content guidelines for any drafts
5. Use the HCAE attribution line on all posts
6. Keep the voice consistent — practitioner, not salesperson
