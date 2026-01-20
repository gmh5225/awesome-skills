# `awesome-skills`[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[![GitHub license](https://img.shields.io/github/license/gmh5225/awesome-skills)](https://github.com/gmh5225/awesome-skills/blob/main/LICENSE)

A curated list of Agent Skills, resources, and tools for AI coding agents like Claude Code, Codex, Gemini CLI, GitHub Copilot, and more.

> Show respect to all the projects below, perfect works of art :saluting_face:

## How to contribute?
- https://github.com/HyunCafe/contribute-practice
- https://docs.github.com/en/get-started/quickstart/contributing-to-projects


## What Are Agent Skills?

**Agent Skills** are instruction files that teach AI assistants how to perform specific tasks. They are specialized folders containing instructions, scripts, and resources that AI agents dynamically discover and load when relevant to tasks.

Skills employ a **progressive disclosure architecture** for efficiency:
1. **Metadata loading** (~100 tokens): AI scans available Skills to identify relevant matches
2. **Full instructions** (<5k tokens): Load when AI determines the Skill applies
3. **Bundled resources**: Files and executable code load only as needed

### Skill Structure

```
skill-name/
├── SKILL.md          # Required: Instructions and metadata
├── scripts/          # Optional: Helper scripts
├── templates/        # Optional: Document templates
└── resources/        # Optional: Reference files
```

### Basic SKILL.md Template

```markdown
---
name: my-skill-name
description: A clear description of what this skill does.
---

# My Skill Name

Detailed description of the skill's purpose.

## When to Use This Skill

- Use case 1
- Use case 2

## Instructions

[Detailed instructions for the agent on how to execute this skill]

## Examples

[Real-world examples]
```


## Compatible Agents & Platforms

### Programming Tools

| Tool | Project Path | Global Path | Documentation |
|------|--------------|-------------|---------------|
| **Amp** | `.agents/skills/` | `~/.config/agents/skills/` | [Amp Skills](https://ampcode.com/manual#agent-skills) |
| **Antigravity** | `.agent/skills/` | `~/.gemini/antigravity/skills/` | [Antigravity Skills](https://antigravity.google/docs/skills) |
| **Clawdbot** | `./skills/` | `~/.clawdbot/skills/` | [Clawdbot Skills](https://docs.clawd.bot/tools/skills) |
| **Claude Code** | `.claude/skills/` | `~/.claude/skills/` | [Claude Code Skills](https://code.claude.com/docs/en/skills) |
| **Codex** | `.codex/skills/` | `~/.codex/skills/` | [Codex Skills](https://developers.openai.com/codex/skills) |
| **Cursor** | `.cursor/skills/` | `~/.cursor/skills/` | [Cursor Skills](https://cursor.com/docs/context/skills) |
| **Droid/Factory** | `.factory/skills/` | `~/.factory/skills/` | [Factory Droid Skills](https://docs.factory.ai/cli/configuration/skills) |
| **Gemini CLI** | `.gemini/skills/` | `~/.gemini/skills/` | [Gemini CLI Skills](https://geminicli.com/docs/cli/skills/) |
| **GitHub Copilot** | `.github/skills/` | `~/.copilot/skills/` | [Copilot Skills](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills) |
| **Goose** | `.goose/skills/` | `~/.config/goose/skills/` | [Goose Skills](https://block.github.io/goose/docs/guides/context-engineering/using-skills/) |
| **Kilo Code** | `.kilocode/skills/` | `~/.kilocode/skills/` | [Kilo Skills](https://kilo.ai/docs/agent-behavior/skills) |
| **OpenCode** | `.opencode/skills/` | `~/.config/opencode/skills/` | [OpenCode Skills](https://opencode.ai/docs/skills) |
| **Roo Code** | `.roo/skills/` | `~/.roo/skills/` | [Roo Code Skills](https://docs.roocode.com/features/skills) |
| **Windsurf** | `.windsurf/skills/` | `~/.codeium/windsurf/skills/` | [Windsurf Cascade Skills](https://docs.windsurf.com/windsurf/cascade/skills) |

### Conversational Tools

- [Coze](https://www.coze.cn/open/docs/cozespace/what_is_skill) - Skills Usage Guide
- [Cherry Studio](https://mp.weixin.qq.com/s/nqBMW9QaTcagohzy2gXaZA) - Agent Skills Best Practices
- [Alma](https://alma.now/docs/zh/features/skills.html) - Skills Usage Guide


## Official Skills

### Official Anthropic Skills

| Skill | Description | Source |
|-------|-------------|--------|
| docx | Create, edit, analyze Word documents with tracked changes | [anthropics/skills](https://github.com/anthropics/skills) |
| xlsx | Spreadsheet manipulation: formulas, charts, data transformations | [anthropics/skills](https://github.com/anthropics/skills) |
| pptx | Read, generate, and adjust slides, layouts, templates | [anthropics/skills](https://github.com/anthropics/skills) |
| pdf | Extract text, tables, metadata from PDFs | [anthropics/skills](https://github.com/anthropics/skills) |
| algorithmic-art | Create generative art using p5.js with seeded randomness | [anthropics/skills](https://github.com/anthropics/skills) |
| canvas-design | Design visual art in PNG and PDF formats | [anthropics/skills](https://github.com/anthropics/skills) |
| frontend-design | Avoid "AI slop" aesthetics and make bold design decisions | [anthropics/skills](https://github.com/anthropics/skills) |
| slack-gif-creator | Create animated GIFs optimized for Slack size constraints | [anthropics/skills](https://github.com/anthropics/skills) |
| theme-factory | Style artifacts with professional themes | [anthropics/skills](https://github.com/anthropics/skills) |
| web-artifacts-builder | Build complex HTML artifacts with React and Tailwind | [anthropics/skills](https://github.com/anthropics/skills) |
| mcp-builder | Create MCP servers to integrate external APIs | [anthropics/skills](https://github.com/anthropics/skills) |
| webapp-testing | Test local web applications using Playwright | [anthropics/skills](https://github.com/anthropics/skills) |
| brand-guidelines | Apply brand colors and typography to artifacts | [anthropics/skills](https://github.com/anthropics/skills) |
| internal-comms | Write status reports, newsletters, and FAQs | [anthropics/skills](https://github.com/anthropics/skills) |
| skill-creator | Guide for creating skills that extend capabilities | [anthropics/skills](https://github.com/anthropics/skills) |

### Official OpenAI Codex Skills

| Skill Scope | Location | Suggested Use |
|-------------|----------|---------------|
| REPO | `$CWD/.codex/skills` | Skills relevant to a working folder |
| REPO | `$CWD/../.codex/skills` | Skills for shared areas in parent folders |
| REPO | `$REPO_ROOT/.codex/skills` | Root skills for everyone using the repository |
| USER | `$CODEX_HOME/skills` (default: `~/.codex/skills`) | Personal skills that apply to any repository |
| ADMIN | `/etc/codex/skills` | SDK scripts, automation, and default admin skills |
| SYSTEM | Bundled with Codex | Built-in skills like skill-creator and plan |

### Official HuggingFace Skills

| Skill | Description | Source |
|-------|-------------|--------|
| hf_dataset_creator | Prompts, templates, and scripts for creating structured training datasets | [huggingface/skills](https://github.com/huggingface/skills) |
| hf_model_evaluation | Instructions plus utilities for orchestrating evaluation jobs | [huggingface/skills](https://github.com/huggingface/skills) |
| hf-llm-trainer | Comprehensive training skill with guidance, helper scripts | [huggingface/skills](https://github.com/huggingface/skills) |
| hf-paper-publisher | Tools for publishing and managing research papers on Hugging Face Hub | [huggingface/skills](https://github.com/huggingface/skills) |


## Skills by Teams

### Vercel Engineering Team

- [vercel-labs/react-best-practices](https://github.com/vercel-labs/agent-skills/tree/main/skills/react-best-practices) - React best practices and patterns
- [vercel-labs/vercel-deploy-claimable](https://github.com/vercel-labs/agent-skills/tree/main/skills/claude.ai/vercel-deploy-claimable) - Deploy projects to Vercel
- [vercel-labs/web-design-guidelines](https://github.com/vercel-labs/agent-skills/tree/main/skills/web-design-guidelines) - Web design guidelines and standards

### Trail of Bits Security Team

- [trailofbits/audit-context-building](https://github.com/trailofbits/skills/tree/main/plugins/audit-context-building) - Deep architectural context via ultra-granular code analysis
- [trailofbits/building-secure-contracts](https://github.com/trailofbits/skills/tree/main/plugins/building-secure-contracts) - Smart contract security toolkit with vulnerability scanners
- [trailofbits/burpsuite-project-parser](https://github.com/trailofbits/skills/tree/main/plugins/burpsuite-project-parser) - Search and extract data from Burp Suite project files
- [trailofbits/constant-time-analysis](https://github.com/trailofbits/skills/tree/main/plugins/constant-time-analysis) - Detect compiler-induced timing side-channels in crypto code
- [trailofbits/differential-review](https://github.com/trailofbits/skills/tree/main/plugins/differential-review) - Security-focused diff review with git history analysis
- [trailofbits/entry-point-analyzer](https://github.com/trailofbits/skills/tree/main/plugins/entry-point-analyzer) - Identify state-changing entry points in smart contracts
- [trailofbits/fix-review](https://github.com/trailofbits/skills/tree/main/plugins/fix-review) - Verify fix commits address audit findings without new bugs
- [trailofbits/property-based-testing](https://github.com/trailofbits/skills/tree/main/plugins/property-based-testing) - Property-based testing for multiple languages
- [trailofbits/semgrep-rule-creator](https://github.com/trailofbits/skills/tree/main/plugins/semgrep-rule-creator) - Create and refine Semgrep rules for vulnerability detection
- [trailofbits/static-analysis](https://github.com/trailofbits/skills/tree/main/plugins/static-analysis) - Static analysis toolkit with CodeQL, Semgrep, and SARIF
- [trailofbits/variant-analysis](https://github.com/trailofbits/skills/tree/main/plugins/variant-analysis) - Find similar vulnerabilities via pattern-based analysis

### Sentry Team

- [getsentry/agents-md](https://github.com/getsentry/skills/tree/main/plugins/sentry-skills/skills/agents-md) - Generate and manage AGENTS.md files
- [getsentry/code-review](https://github.com/getsentry/skills/tree/main/plugins/sentry-skills/skills/code-review) - Perform code reviews
- [getsentry/commit](https://github.com/getsentry/skills/tree/main/plugins/sentry-skills/skills/commit) - Create commits with best practices
- [getsentry/create-pr](https://github.com/getsentry/skills/tree/main/plugins/sentry-skills/skills/create-pr) - Create pull requests
- [getsentry/find-bugs](https://github.com/getsentry/skills/tree/main/plugins/sentry-skills/skills/find-bugs) - Find and identify bugs in code

### Expo Team

- [expo/expo-app-design](https://github.com/expo/skills/tree/main/plugins/expo-app-design) - Design and build Expo applications
- [expo/expo-deployment](https://github.com/expo/skills/tree/main/plugins/expo-deployment) - Deploy Expo apps to production
- [expo/upgrading-expo](https://github.com/expo/skills/tree/main/plugins/upgrading-expo) - Upgrade Expo SDK versions


## Community Skills

### Skill Collections

| Repository | Description |
|------------|-------------|
| [anthropics/skills](https://github.com/anthropics/skills) | Official Anthropic collection (document editing, data analysis) |
| [openai/skills](https://github.com/openai/skills) | Official OpenAI Codex skills catalog |
| [huggingface/skills](https://github.com/huggingface/skills) | HuggingFace skills (compatible with Claude, Codex, Gemini) |
| [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | **179+ skills** for Claude Code, Gemini CLI, Cursor, Copilot & more |
| [obra/superpowers](https://github.com/obra/superpowers) | Core skills library with 20+ battle-tested skills including TDD, debugging |
| [skillcreatorai/Ai-Agent-Skills](https://github.com/skillcreatorai/Ai-Agent-Skills) | SkillCreator.ai collection with CLI installer |
| [karanb192/awesome-claude-skills](https://github.com/karanb192/awesome-claude-skills) | 50+ verified skills for Claude Code and Claude.ai |
| [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) | Quality Skills collection for various programming tasks |
| [ComposioHQ/awesome-codex-skills](https://github.com/ComposioHQ/awesome-codex-skills) | Practical Codex skills for automation workflows |
| [VoltAgent/awesome-claude-skills](https://github.com/VoltAgent/awesome-claude-skills) | Awesome collection with official and community-built resources |
| [mhattingpete/claude-skills-marketplace](https://github.com/mhattingpete/claude-skills-marketplace) | Git, code review, and testing skills |
| [Code-and-Sorts/awesome-copilot-agents](https://github.com/Code-and-Sorts/awesome-copilot-agents) | Instructions, prompts, skills and custom agents for GitHub Copilot |

### Document Processing

| Skill | Description |
|-------|-------------|
| [Markdown to EPUB](https://github.com/smerchek/claude-epub-skill) | Converts markdown documents into professional EPUB ebook files |
| [revealjs-skill](https://github.com/ryanbbrown/revealjs-skill/tree/main) | Generate polished presentations using Reveal.js HTML framework |
| [epub-translator](https://github.com/Nebu1eto/skills/tree/main/epub-translator) | Translate EPUB ebooks between languages with parallel processing and quality validation |
| [pdf-translator](https://github.com/Nebu1eto/skills/tree/main/pdf-translator) | Translate PDF documents with layout preservation, supports academic papers and Markdown/PDF output |

### Development & Code Tools

| Skill | Description |
|-------|-------------|
| [aws-skills](https://github.com/zxkane/aws-skills) | AWS development with CDK best practices |
| [D3.js Visualization](https://github.com/chrisvoncsefalvay/claude-d3js-skill) | D3 charts and interactive data visualizations |
| [Playwright Automation](https://github.com/lackeyjb/playwright-skill) | Browser automation for testing web apps |
| [iOS Simulator](https://github.com/conorluddy/ios-simulator-skill) | Interact with iOS Simulator for testing |
| [Swift Concurrency Migration](https://github.com/kylehughes/the-unofficial-swift-concurrency-migration-skill) | Swift Concurrency Migration guide |
| [Obsidian Plugin](https://github.com/gapmiss/obsidian-plugin-skill) | Obsidian.md plugin development |
| [FFUF Web Fuzzing](https://github.com/jthack/ffuf_claude_skill) | Web fuzzer integration for vulnerability analysis |
| [move-code-quality-skill](https://github.com/1NickPappas/move-code-quality-skill) | Move language code quality checklist |
| [pypict-claude-skill](https://github.com/omkamal/pypict-claude-skill) | Pairwise Independent Combinatorial Testing |
| [claude-starter](https://github.com/raintree-technology/claude-starter) | Production-ready Claude Code configuration template |
| [cloudflare-skill](https://github.com/dmmulroy/cloudflare-skill/tree/main/skill/cloudflare) | Cloudflare platform reference docs |
| [solana-dev-skill](https://github.com/GuiBibeau/solana-dev-skill) | Solana blockchain development skill |
| [Skill Seekers](https://github.com/yusufkaraaslan/Skill_Seekers) | Convert documentation websites into Skills |

### Data & Analysis

| Skill | Description |
|-------|-------------|
| [CSV Summarizer](https://github.com/coffeefuelbump/csv-data-summarizer-claude-skill) | Analyze CSV files and generate insights with visualizations |
| [postgres](https://github.com/sanjay3290/ai-skills/tree/main/skills/postgres) | Safe read-only SQL queries against PostgreSQL |
| [deep-research](https://github.com/sanjay3290/ai-skills/tree/main/skills/deep-research) | Autonomous multi-step research using Gemini |
| [root-cause-tracing](https://github.com/obra/superpowers/tree/main/skills/root-cause-tracing) | Trace back to find original error triggers |

### Integration & Automation

| Skill | Description |
|-------|-------------|
| [Dev Browser](https://github.com/SawyerHood/dev-browser) | Web browser capability for agents |
| [Sheets CLI](https://github.com/gmickel/sheets-cli) | Google Sheets CLI automation |
| [Spotify Skill](https://github.com/fabioc-aloha/spotify-skill) | Spotify API integration |
| [linear-claude-skill](https://github.com/wrsmith108/linear-claude-skill) | Manage Linear issues, projects, and teams |
| [n8n-skills](https://github.com/czlonkowski/n8n-skills) | n8n workflow automation skills |
| [NotebookLM Integration](https://github.com/PleasePrompto/notebooklm-skill) | Chat with NotebookLM for source-grounded answers |

### Collaboration & Project Management

| Skill | Description |
|-------|-------------|
| [git-pushing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/git-pushing) | Automate git operations and repository interactions |
| [review-implementing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/review-implementing) | Evaluate code implementation plans |
| [test-fixing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/test-fixing) | Detect failing tests and propose fixes |
| [test-driven-development](https://github.com/obra/superpowers/tree/main/skills/test-driven-development) | TDD implementation workflow |
| [using-git-worktrees](https://github.com/obra/superpowers/blob/main/skills/using-git-worktrees/) | Git worktrees with smart directory selection |
| [finishing-a-development-branch](https://github.com/obra/superpowers/tree/main/skills/finishing-a-development-branch) | Complete development work workflow |

### Security & Systems

| Skill | Description |
|-------|-------------|
| [computer-forensics](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/computer-forensics-skills/skills/computer-forensics) | Digital forensics analysis and investigation |
| [Threat Hunting](https://github.com/jthack/threat-hunting-with-sigma-rules-skill) | Hunt for threats using Sigma detection rules |
| [defense-in-depth](https://github.com/obra/superpowers/blob/main/skills/defense-in-depth) | Multi-layered testing and security best practices |
| [varlock-claude-skill](https://github.com/wrsmith108/varlock-claude-skill) | Secure environment variable management |

### Scientific & Research

| Skill | Description |
|-------|-------------|
| [claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) | 125+ scientific skills for bioinformatics, cheminformatics |
| [materials-simulation-skills](https://github.com/HeshamFS/materials-simulation-skills) | Computational materials science skills |
| [family-history-research](https://github.com/emaynard/claude-family-history-research-skill) | Family history and genealogy research |

### Health & Life Sciences

| Skill | Description |
|-------|-------------|
| [Claude-Ally-Health](https://github.com/huifer/Claude-Ally-Health) | Health assistant for medical report analysis and wellness suggestions |

### Cybersecurity & Penetration Testing

| Skill | Description |
|-------|-------------|
| [ethical-hacking-methodology](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/ethical-hacking-methodology) | Penetration testing lifecycle and security scanning |
| [metasploit-framework](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/metasploit-framework) | Metasploit for vulnerability exploitation |
| [burp-suite-testing](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/burp-suite-testing) | Web application testing with Burp Suite |
| [sql-injection-testing](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/sql-injection-testing) | SQL injection vulnerability detection |
| [xss-html-injection](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/xss-html-injection) | Cross-site scripting and HTML injection testing |
| [active-directory-attacks](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/active-directory-attacks) | Windows domain penetration testing |
| [aws-penetration-testing](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/aws-penetration-testing) | AWS cloud security assessment |
| [linux-privilege-escalation](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/linux-privilege-escalation) | Linux privesc vectors and exploitation |
| [windows-privilege-escalation](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/windows-privilege-escalation) | Windows privilege escalation techniques |
| [top-web-vulnerabilities](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/top-web-vulnerabilities) | OWASP-aligned vulnerability taxonomy |
| [red-team-tools](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/red-team-tools) | Red team methodology and bug bounty hunting |

### Marketing & Growth

| Skill | Description |
|-------|-------------|
| [copywriting](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/copywriting) | Marketing copy for landing pages and pricing pages |
| [seo-audit](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/seo-audit) | Technical and on-page SEO auditing |
| [page-cro](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/page-cro) | Conversion rate optimization for marketing pages |
| [email-sequence](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/email-sequence) | Email drip campaigns and lifecycle programs |
| [paid-ads](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/paid-ads) | Google Ads, Meta, LinkedIn campaign optimization |
| [pricing-strategy](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/pricing-strategy) | SaaS pricing and monetization strategy |
| [launch-strategy](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/launch-strategy) | Product launches and go-to-market strategies |
| [programmatic-seo](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/programmatic-seo) | SEO-driven pages at scale |
| [marketing-ideas](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/marketing-ideas) | 140 proven SaaS marketing strategies |

### AI Agents & LLM Development

| Skill | Description |
|-------|-------------|
| [langgraph](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/langgraph) | Stateful, multi-actor AI applications |
| [crewai](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/crewai) | Role-based multi-agent framework |
| [langfuse](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/langfuse) | LLM observability and tracing |
| [rag-engineer](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/rag-engineer) | RAG systems with embeddings and vector databases |
| [prompt-engineer](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/prompt-engineer) | Prompt design for LLM applications |
| [voice-agents](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/voice-agents) | Voice-based AI assistants |
| [browser-automation](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/browser-automation) | Browser automation with Playwright and Puppeteer |
| [agent-memory-systems](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/agent-memory-systems) | Memory architecture for AI agents |
| [autonomous-agents](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/autonomous-agents) | AI systems with ReAct and reflection patterns |
| [loki-mode](https://github.com/asklokesh/claudeskill-loki-mode) | Multi-agent autonomous startup system |

### Integrations & APIs

| Skill | Description |
|-------|-------------|
| [stripe-integration](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/stripe-integration) | Stripe checkout, subscriptions, webhooks |
| [firebase](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/firebase) | Firebase Auth, Firestore, Cloud Functions |
| [supabase](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/nextjs-supabase-auth) | Supabase Auth with Next.js App Router |
| [clerk-auth](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/clerk-auth) | Clerk auth implementation and webhooks |
| [twilio-communications](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/twilio-communications) | SMS, voice, video with Twilio |
| [discord-bot-architect](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/discord-bot-architect) | Production Discord bots with Discord.js |
| [slack-bot-builder](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/slack-bot-builder) | Slack bots with Bolt framework |
| [graphql](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/graphql) | GraphQL schema design and Apollo integration |
| [aws-serverless](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/aws-serverless) | Lambda, API Gateway, DynamoDB |
| [vercel-deployment](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/vercel-deployment) | Vercel deployment and edge functions |

### Web Performance & SEO

| Skill | Description |
|-------|-------------|
| [web-accessibility-contrast](https://github.com/nicepkg/awesomeAgentskills/tree/main/web-performance-seo) | Fix PageSpeed accessibility issues |
| [google-official-seo-guide](https://github.com/nicepkg/awesomeAgentskills/tree/main/google-official-seo-guide) | Google SEO documentation reference |
| [internationalizing-websites](https://github.com/nicepkg/awesomeAgentskills/tree/main/internationalizing-websites) | Multi-language support with next-intl |
| [deploying-to-production](https://github.com/nicepkg/awesomeAgentskills/tree/main/deploying-to-production) | GitHub + Vercel deployment automation |

### Framework Documentation

| Skill | Description |
|-------|-------------|
| [shipany-docs](https://github.com/nicepkg/awesomeAgentskills/tree/main/shipany) | Shipany AI-powered SaaS boilerplate (228 pages) |
| [react-best-practices](https://github.com/vercel-labs/agent-skills/tree/main/skills/react-best-practices) | React patterns from Vercel |
| [react-native-best-practices](https://github.com/callstackincubator/agent-skills/blob/main/skills/react-native-best-practices/SKILL.md) | React Native optimization from Callstack |

### Maker & Product Tools

| Skill | Description |
|-------|-------------|
| [micro-saas-launcher](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/micro-saas-launcher) | Launch small SaaS products fast |
| [browser-extension-builder](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/browser-extension-builder) | Chrome/Firefox extensions with Manifest v3 |
| [telegram-bot-builder](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/telegram-bot-builder) | Telegram bots and Mini Apps |
| [viral-generator-builder](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/viral-generator-builder) | Building shareable viral generators |
| [3d-web-experience](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/3d-web-experience) | Three.js, React Three Fiber, WebGL |
| [interactive-portfolio](https://github.com/sickn33/antigravity-awesome-skills/tree/main/skills/interactive-portfolio) | Developer/designer portfolios |

### Notion Skills

| Skill | Description |
|-------|-------------|
| [notion-knowledge-capture](https://github.com/ComposioHQ/awesome-llm-skills/tree/main/notion-knowledge-capture) | Convert chats to structured Notion pages |
| [notion-meeting-intelligence](https://github.com/ComposioHQ/awesome-llm-skills/tree/main/notion-meeting-intelligence) | Meeting prep with Notion context |
| [notion-research-documentation](https://github.com/ComposioHQ/awesome-llm-skills/tree/main/notion-research-documentation) | Synthesize Notion sources into reports |
| [notion-spec-to-implementation](https://github.com/ComposioHQ/awesome-llm-skills/tree/main/notion-spec-to-implementation) | Turn Notion specs into task plans |

### Context Engineering

| Skill | Description |
|-------|-------------|
| [context-fundamentals](https://github.com/muratcankoylan/Agent-Skills-for-Context-Engineering/tree/main/skills/context-fundamentals) | Understand context in agent systems |
| [context-degradation](https://github.com/muratcankoylan/Agent-Skills-for-Context-Engineering/tree/main/skills/context-degradation) | Recognize patterns of context failure |
| [context-compression](https://github.com/muratcankoylan/Agent-Skills-for-Context-Engineering/tree/main/skills/context-compression) | Design compression strategies for long sessions |
| [multi-agent-patterns](https://github.com/muratcankoylan/Agent-Skills-for-Context-Engineering/tree/main/skills/multi-agent-patterns) | Multi-agent architectures |
| [memory-systems](https://github.com/muratcankoylan/Agent-Skills-for-Context-Engineering/tree/main/skills/memory-systems) | Design memory architectures |


## Skills Marketplaces

- [skillsmp.com](https://skillsmp.com/) - Most comprehensive and frequently updated Skills marketplace
- [SkillStore](https://skillstore.io/) - Security-audited Skills marketplace
- [agentskills.me](https://agentskills.me/) - Marketplace offering developer revenue sharing
- [skills.rest](https://skills.rest/) - Marketplace with Skill rating system


## Supporting Tools

- [Skill_Seekers](https://github.com/yusufkaraaslan/Skill_Seekers) - Automated conversion of documentation sites to Skills
- [openskills](https://github.com/numman-ali/openskills) - Global Skills loading tool for multiple platforms
- [skild.sh](https://skild.sh/) - CLI tool for installing, managing, and syncing Skills
- [agent-skills-guard](https://github.com/brucevanfdm/agent-skills-guard) - Skills visualization management + security scanning
- [skillmaster](https://github.com/davidyangcool/agent-skill) - Manage, install, and use Agent Skills via terminal
- [vercel-labs/add-skill](https://github.com/vercel-labs/add-skill) - `npx skills` CLI tool for quick installation


## Content Humanization

- [humanizer](https://github.com/blader/humanizer) - Remove AI writing signs from text
- [Humanizer-zh](https://github.com/op7418/Humanizer-zh) - Humanizer Chinese version


## GitHub Copilot Instructions & Prompts

### Language & Stack Instructions

| Language | Description |
|----------|-------------|
| [C](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/c) | System libraries, CLI tools, embedded applications |
| [C#](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/csharp) | .NET applications with modern C# patterns |
| [C++](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/cplusplus) | Modern C++ with STL, RAII, performance optimization |
| [Go](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/go) | Microservices, CLI tools, concurrent applications |
| [Java](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/java) | Enterprise Java with Spring framework |
| [JavaScript](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/javascript) | Modern ES6+, Node.js, browser development |
| [Kotlin](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/kotlin) | Android and multi-platform projects |
| [Python](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/python) | Web applications, data science, automation |
| [Rust](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/rust) | Systems programming with memory safety |
| [Swift](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/swift) | iOS and macOS development with SwiftUI |
| [TypeScript](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/languages/typescript) | Web and Node.js applications |

### Framework Instructions

| Framework | Description |
|-----------|-------------|
| [Cobra CLI](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/frameworks/cobra-cli-go) | Charmbracelet Bubbles CLI with Golang Cobra |
| [Node.js Azure Functions](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/frameworks/nodejs-typescript) | Azure Function Apps with TypeScript |
| [Express API](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/frameworks/nodejs-typescript) | REST API with Express.js and TypeScript |
| [Terraform](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/tools/infra-as-code/terraform) | Infrastructure as Code with Atmos |
| [Drupal 11](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/instructions/tools/cms/drupal) | Drupal module and theme development |

### Custom Copilot Agents

| Agent | Description |
|-------|-------------|
| [Architect](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/agents/ai-development-mode/architect.agent.md) | Design and plan software systems |
| [Clean Code](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/agents/ai-development-mode/clean-code.agent.md) | Write clean, maintainable code |
| [Debugger](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/agents/ai-development-mode/debugger.agent.md) | Debug application code |
| [PRD Creation](https://github.com/Code-and-Sorts/awesome-copilot-agents/tree/main/agents/ai-development-mode/prd-creation.agent.md) | Build Product Requirements Documents |


## Tutorials & Resources

### Official Documentation

- [Claude Skills Overview](https://www.anthropic.com/news/skills) - Official announcement and features
- [Using Skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude) - How to use skills
- [Creating Custom Skills](https://support.claude.com/en/articles/12512198-creating-custom-skills) - Skill development guide
- [Create a Skill Through Conversation](https://support.claude.com/en/articles/12599426-how-to-create-a-skill-with-claude-through-conversation) - Interactive skill creation
- [Skills API Documentation](https://docs.claude.com/en/api/skills-guide) - API integration guide
- [Agent Skills Blog Post](https://anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) - Engineering deep dive
- [Skills Explained](https://claude.com/blog/skills-explained) - Comprehensive guide on progressive disclosure
- [Claude for Financial Services Skills](https://support.claude.com/en/articles/12663107-claude-for-financial-services-skills) - Industry-specific skills
- [GitHub Copilot Agent Skills](https://docs.github.com/copilot/concepts/agents/about-agent-skills) - GitHub documentation
- [VS Code Agent Skills](https://code.visualstudio.com/docs/copilot/customization/agent-skills) - VS Code integration
- [MCP Official Documentation](https://modelcontextprotocol.io/) - Model Context Protocol

### Video Tutorials

- [Claude Skills Just 10x'd My AI Agents by Greg Isenberg](https://www.youtube.com/watch?v=G-5bInklwRQ)
- [Claude Skills: Build Your Own AI Experts](https://www.youtube.com/watch?v=46zQX7PSHfU)
- [Agent Skills: Specialized capabilities you can customize](https://www.youtube.com/watch?v=IoqpBKrNaZI)
- [Claude Skills—From TOY to TOOL](https://www.youtube.com/watch?v=WKFFFumnzYI)
- [Stop Using MCP... Use NEW Claude Skills Instead](https://www.youtube.com/watch?v=M8yaR-wNGj0)
- [Claude Skills explained: How to create reusable AI workflows](https://www.youtube.com/watch?v=MZZCW179nKM)
- [Agent Skills from Usage to Principles](https://www.youtube.com/watch?v=yDc0_8emz7M) (Chinese)
- [Stop Building Agents, The Future is Skills](https://www.youtube.com/watch?v=xeoWgfkxADI) (Chinese)

### Articles & Blog Posts

- [Skills Explained](https://claude.com/blog/skills-explained) - Official blog post on Skills
- [Simon Willison: Claude Skills are awesome](https://simonwillison.net/2025/Oct/16/claude-skills/) - Technical analysis
- [Extending Claude with Skills and MCP](https://claude.com/blog/extending-claude-capabilities-with-skills-mcp-servers)
- [Building Skills for Claude Code](https://claude.com/blog/building-skills-for-claude-code)
- [Don't Build Agents, Build Skills Instead](https://x.com/iamzhihui/status/2005883147305500681)
- [Improving Frontend Design Through Skills](https://claude.com/blog/improving-frontend-design-through-skills)
- [How to Create Skills: Key Steps, Limitations, and Examples](https://claude.com/blog/how-to-create-skills-key-steps-limitations-and-examples)
- [Nick Nisi: Claude Skills](https://nicknisi.com/posts/claude-skills/) - Getting started guide


## Data Science & AI Learning Roadmaps

- [Data Science Career Roadmap](https://pub.towardsai.net/simple-but-effective-free-roadmap-to-start-a-career-in-data-science-ai-in-2023-9d17c76a184b)
- [Data Analytics Roadmap](https://levelup.gitconnected.com/comprehensive-data-analytics-roadmap-for-2023-with-free-resources-adfefc0d0d7f)
- [Python for Data Science Roadmap](https://levelup.gitconnected.com/ultimate-free-python-for-data-science-roadmap-in-2023-728daa9581de)
- [MLOps Learning Roadmap](https://pub.towardsai.net/ultimate-mlops-learning-roadmap-with-free-learning-resources-in-2023-3ba7664cb1e9)
- [Computer Vision Study Roadmap](https://levelup.gitconnected.com/a-comprehensive-computer-vision-free-study-roadmap-for-2023-3e95a6d656e7)
- [Generative AI Learning Roadmap](https://open.substack.com/pub/youssefh/p/generative-ai-learning-roadmap-from)
- [Complete LLM Roadmap](https://open.substack.com/pub/youssefh/p/complete-llm-roadmap-from-beginner)
- [LLMs Mastery Study Plan](https://pub.towardsai.net/from-novice-to-expert-a-comprehensive-step-by-step-study-plan-for-mastering-llms-dc9feb60ecc4)
- [SQL Mastery for Data Scientists](https://levelup.gitconnected.com/sql-mastery-for-data-scientists-a-comprehensive-guide-from-novice-to-advanced-3b9305b03210)


## Skills vs Other Approaches

| Tool | Best For |
|------|----------|
| **Skills** | Reusable procedural knowledge across conversations |
| **Prompts** | One-time instructions and immediate context |
| **Projects** | Persistent background knowledge within workspaces |
| **Subagents** | Independent task execution with specific permissions |
| **MCP** | Connecting to external data sources and APIs |

**Key insight**: *If you find yourself typing the same prompt repeatedly across multiple conversations, it's time to create a Skill.*


## FAQ

**Q: How much do skills impact token usage?**  
A: Skills are highly efficient. Each skill uses only ~100 tokens during metadata scanning. When activated, the full skill content loads at <5k tokens.

**Q: What's the difference between Agent Skills and MCP?**  
A: They do different things and work great together:
- **Agent Skills** = teach the AI *how* to do something (workflows, best practices)
- **MCP** = help the AI *access* things (APIs, databases, external tools)

**Q: Do Agent Skills run code?**  
A: No. Skills are just text instructions. If you need to run actual code, you'd use MCP servers alongside skills.

**Q: How do I create my first Agent Skill?**  
A: Create a `SKILL.md` file with a name and description at the top, write clear instructions, put it in your `.github/skills/` or `.claude/skills/` folder, and test it out.


## Security Considerations

⚠️ **Important**: Skills can execute arbitrary code in the agent's environment. Only install skills from trusted sources.

- **Review SKILL.md and all scripts** before enabling a skill
- **Be cautious of skills** that request sensitive data access
- **Audit carefully** before deploying to production


## License

MIT License - see LICENSE file for details.
