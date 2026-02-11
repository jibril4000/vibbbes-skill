```
██╗   ██╗██╗██████╗ ██████╗ ██████╗ ███████╗███████╗
██║   ██║██║██╔══██╗██╔══██╗██╔══██╗██╔════╝██╔════╝
██║   ██║██║██████╔╝██████╔╝██████╔╝█████╗  ███████╗
╚██╗ ██╔╝██║██╔══██╗██╔══██╗██╔══██╗██╔══╝  ╚════██║
 ╚████╔╝ ██║██████╔╝██████╔╝██████╔╝███████╗███████║
  ╚═══╝  ╚═╝╚═════╝ ╚═════╝ ╚═════╝ ╚══════╝╚══════╝
```

### [designwithvibbbes.com](https://www.designwithvibbbes.com) — Generate Design Systems Instantly with AI

Generate production-ready design systems instantly from the command line or any AI coding tool.

Describe what you want, paste a URL, or drop a screenshot — Vibbbes generates a complete design system with 85+ components, tokens, and patterns.

---

# Vibbbes Skill for Claude Code

Teach your AI coding agent to generate production-ready design systems with 85+ components — from text prompts, website URLs, or screenshots.

This skill works alongside the [Vibbbes MCP server](https://www.npmjs.com/package/vibbbes) to give your AI agent the knowledge of **when** and **how** to use Vibbbes tools effectively.

## What This Does

Without the skill, your AI agent has the Vibbbes MCP *tools* but doesn't know the best practices for using them. With the skill installed, your agent will:

- Automatically use Vibbbes when you ask for design work (instead of writing CSS by hand)
- Choose the right tool for the job (text prompt vs URL extraction vs image analysis)
- Pick the correct output format based on your tech stack (Tailwind, CSS variables, JSON, HTML)
- Write specific, detailed prompts that produce better results
- Check for existing design system files before generating new ones
- Save outputs to the right locations in your project

## Prerequisites

You need the Vibbbes MCP server installed first. If you haven't set it up:

```bash
npx vibbbes login
npx vibbbes setup
```

This gives your AI agent the Vibbbes tools. The skill below teaches it how to use them well.

## Install the Skill

```
/plugin install github:jibril4000/vibbbes-skill
```

That's it. The skill is now active in all your Claude Code sessions.

## What Gets Installed

```
vibbbes-skill/
├── .claude-plugin/
│   └── plugin.json          # Plugin metadata
├── skills/
│   └── vibbbes/
│       └── SKILL.md         # Agent instructions
├── LICENSE
└── README.md
```

## Usage

Once installed, just ask naturally. The skill auto-triggers when you mention design systems, design tokens, themes, or component libraries.

**Generate from a description:**
> "Create a design system for a modern dark SaaS dashboard with purple accents"

**Extract from a website:**
> "Generate a design system from stripe.com"

**Match a screenshot:**
> "Generate a design system from ./mockup.png"

**You can also invoke it directly:**
```
/vibbbes create a minimal design system for a health app
```

## Manual Installation (Alternative)

If you prefer not to use the plugin system, copy the agent instructions from [`skills/vibbbes/SKILL.md`](skills/vibbbes/SKILL.md) into your project's `CLAUDE.md` file.

## MCP Tools Reference

The skill teaches your agent to use these three Vibbbes MCP tools:

| Tool | Input | Cost | Description |
|------|-------|------|-------------|
| `generate_design_system` | Text prompt | 1 credit | Generate from a description |
| `generate_design_system_from_url` | Website URL | 2 credits | Extract a site's design language |
| `generate_design_system_from_image` | Image path | 1 credit | Match a screenshot or mockup |

### Output Formats

| Format | Best For |
|--------|----------|
| `json` | Structured tokens, custom integrations |
| `html` | Visual preview with 85+ components |
| `css_variables` | Vanilla CSS, framework-agnostic projects |
| `tailwind` | Tailwind CSS projects |

## Links

- [Vibbbes](https://www.designwithvibbbes.com) — Generate design systems with AI
- [Documentation](https://www.designwithvibbbes.com/docs) — Full CLI & MCP docs
- [npm package](https://www.npmjs.com/package/vibbbes) — Vibbbes CLI & MCP server
- [Pricing](https://www.designwithvibbbes.com/pricing) — Free tier + paid plans

## License

MIT
