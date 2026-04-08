# Website Design Agent

A unified Claude Code skill for designing, building, auditing, and critiquing production-grade websites. Combines six specialized design disciplines into a single 5-phase workflow, backed by 58 real brand design system references.

## What's Inside

| Component | Source | What It Does |
|-----------|--------|-------------|
| **Creative Direction** | frontend-design | Anti-generic aesthetic philosophy, bold design thinking |
| **Expert References** | impeccable-design | 7 deep-dive docs (typography, color/OKLCH, motion, spatial, interaction, responsive, UX writing) |
| **Searchable Design DB** | ui-ux-pro-max | 50+ styles, 97 palettes, 57 font pairings, BM25 search engine |
| **Quantitative Critique** | design-critique | Nielsen's heuristics /40, cognitive load assessment, 5-persona testing |
| **Visual Audit** | refactoring-ui | 7-pillar audit (hierarchy, spacing, color, typography, shadows, borders, icons) |
| **Token Generation** | ui-design-system | Design token generator (colors, type scale, spacing, shadows) |
| **Brand References** | [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) | 58 real brand DESIGN.md files with pixel-level specs |

## 5-Phase Workflow

```
Phase 1: UNDERSTAND  — Commit to a bold aesthetic direction
Phase 2: RESEARCH    — Brand reference lookup + design system generation
Phase 3: BUILD       — Implementation with expert reference consultation
Phase 4: AUDIT       — 7-pillar visual audit + AI slop detection (mandatory gate)
Phase 5: CRITIQUE    — Nielsen's heuristics /40 + persona testing
```

## Installation

### Claude Code (recommended)

Copy the entire directory to your Claude Code skills folder:

```bash
# Clone this repo
git clone https://github.com/nhouseholder/website-design-agent.git

# Copy to Claude Code skills
cp -r website-design-agent ~/.claude/skills/website-design-agent
```

The skill auto-registers with Claude Code and appears as `website-design-agent` in the skill list.

### Manual Usage

You can also reference the SKILL.md directly in any AI coding assistant's system prompt or context window.

## Directory Structure

```
website-design-agent/
├── SKILL.md                    # Master skill definition (5-phase workflow)
├── reference/                  # Expert design references (from impeccable-design)
│   ├── typography.md           # Modular scales, fluid type, OpenType features
│   ├── color-and-contrast.md   # OKLCH, tinted neutrals, 60-30-10 rule
│   ├── motion-design.md        # 100/300/500ms rule, easing curves
│   ├── spatial-design.md       # 4pt grid, container queries, squint test
│   ├── interaction-design.md   # 8 states per element, focus-visible, popover API
│   ├── responsive-design.md    # Content-driven breakpoints, pointer queries
│   ├── ux-writing.md           # Microcopy formulas, error patterns
│   └── theme-library.md        # Pre-built theme combinations
├── critique/                   # Quantitative evaluation frameworks
│   ├── heuristics-scoring.md   # Nielsen's 10 heuristics scoring guide
│   ├── cognitive-load.md       # 8-item cognitive load checklist
│   └── personas.md             # 5 user archetypes for persona testing
├── design-refs/                # 58 real brand DESIGN.md files
│   ├── linear.app/DESIGN.md    # Exact colors, fonts, spacing, components
│   ├── stripe/DESIGN.md
│   ├── vercel/DESIGN.md
│   ├── figma/DESIGN.md
│   ├── apple/DESIGN.md
│   ├── spotify/DESIGN.md
│   └── ... (58 brands total)
├── scripts/                    # Python tools
│   ├── search.py               # BM25 design system search engine
│   ├── core.py                 # Search engine core
│   ├── design_system.py        # Design system generator
│   └── design_token_generator.py # Token generator (colors, type, spacing)
└── data/                       # Search database (CSV)
    ├── styles.csv              # 50+ UI styles
    ├── typography.csv          # 57 font pairings
    ├── colors.csv              # 97 color palettes
    ├── products.csv            # Product-type recommendations
    ├── landing.csv             # Landing page patterns
    ├── ux-guidelines.csv       # UX best practices
    └── stacks/                 # Stack-specific guidelines
        ├── html-tailwind.csv
        ├── react.csv
        ├── nextjs.csv
        └── ...
```

## Brand References (58)

| Category | Brands |
|----------|--------|
| **AI & ML** | Claude, Cohere, Mistral AI, Ollama, Together AI, xAI, OpenCode, Minimax, Replicate |
| **Dev Tools** | Cursor, Linear, Vercel, Supabase, Sentry, PostHog, Expo, Warp, Raycast, HashiCorp |
| **Design** | Figma, Framer, Webflow, Miro, Notion, Cal, Mintlify, Lovable, Sanity |
| **Infra** | MongoDB, ClickHouse, Resend |
| **Fintech** | Stripe, Coinbase, Wise, Revolut, Kraken |
| **Enterprise** | Apple, Spotify, Uber, Airbnb, Pinterest, SpaceX, NVIDIA, IBM, Superhuman, Zapier, Airtable, Intercom, ElevenLabs, RunwayML, Clay, Composio |
| **Auto** | Tesla, Ferrari, BMW, Lamborghini, Renault |

Each DESIGN.md contains exact color palettes, typography specs, spacing systems, component patterns, and animation details extracted from the real website.

## Tools

### Design System Search

```bash
# Generate full design system recommendations
python3 scripts/search.py "minimal dark saas" --design-system -p "My App"

# Search specific domains
python3 scripts/search.py "elegant luxury" --domain typography
python3 scripts/search.py "glassmorphism dark" --domain style
python3 scripts/search.py "saas fintech" --domain color

# Stack-specific guidelines
python3 scripts/search.py "layout responsive" --stack html-tailwind
```

### Design Token Generator

```bash
python3 scripts/design_token_generator.py "#6366f1" modern css
```

Generates: color palette, modular type scale, 8pt spacing grid, shadows, animations, breakpoints.

## AI Slop Detection

Built-in 10-point checklist catches common AI-generated design fingerprints:

1. Inter/Roboto/Open Sans defaults
2. Purple gradient heroes
3. Cards-in-cards nesting
4. Gray text on colored backgrounds
5. Glassmorphism everywhere
6. Fake hero metrics
7. Generic gradient buttons
8. Identical section rhythm
9. Stock testimonials
10. SVG blob backgrounds

**Score 3+ = slop. Redesign before delivering.**

## Credits

- Expert references adapted from [pbakaus/impeccable](https://github.com/pbakaus/impeccable) (Apache 2.0)
- Brand DESIGN.md files from [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) (MIT)
- Search engine and design database from [phanvuminhtrung/ui-ux-pro-max](https://github.com/phanvuminhtrung/ui-ux-pro-max)

## License

MIT
