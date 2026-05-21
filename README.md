# claude-skills

A collection of personal skills for [Claude Code](https://claude.ai/code) — drop-in prompt files that extend Claude with specialized frameworks for coaching, business, and copywriting.

## Collections

### strategic-intervention/
Tony Robbins–style breakthrough tools for internal and psychological work.

| Skill | Description |
|-------|-------------|
| `values-hierarchy` | Uncovers and ranks core values to resolve internal conflicts |
| `needs-decoder` | Diagnoses which of the Six Human Needs drives a behavior |
| `state-story-strategy` | Diagnoses whether you're stuck at State, Story, or Strategy level |
| `triad-state-shift` | Quick state shift via Physiology, Focus, and Language |
| `transformational-vocabulary` | Swaps disempowering language for empowering alternatives |
| `pattern-interrupt` | Breaks rumination loops and negative spirals |
| `leverage-questions` | Generates pain/pleasure questions to create urgency for change |
| `identity-forge` | Crafts a new self-concept and "I AM" identity statements |
| `nac-pattern-breaker` | Full Neuro-Associative Conditioning workflow for breaking habits |
| `dickens-protocol` | Visualization-based belief-shattering using the Christmas Carol framework |
| `modeling-excellence` | Reverse-engineers excellence from peak performers |
| `priming-ritual` | Builds a personalized morning priming routine |
| `rpm-goal-architect` | Transforms vague goals into Result → Purpose → Massive Action Plan |
| `seven-forces-audit` | Diagnoses which of the 7 Forces of Business Mastery is the bottleneck |

### solo-business/
Frameworks from Hormozi, Welsh, Koe, Bush/Cole, and Flynn for solo online business operators.

| Skill | Description |
|-------|-------------|
| `niche-clarity-engine` | Airport Test + History Test + Anti-Vision niche diagnostic |
| `solo-biz-validator` | P.L.A.N. framework + pre-sale test to validate business ideas |
| `solo-biz-phase-diagnostic` | Diagnoses which of the six solopreneur phases you're in |
| `grand-slam-offer-architect` | Hormozi's Grand Slam Offer — Value Equation, bonuses, guarantees |
| `product-ladder-designer` | Designs a full product ladder from free to high-ticket |
| `content-flywheel-builder` | Content Matrix + Rule of One + 5-12-3 repurposing system |
| `category-creation-workshop` | Identifies or invents a category you can own |

### copywriting/
A router stack — `platform-aware-copy-router` is the entry point.

| Skill | Description |
|-------|-------------|
| `platform-aware-copy-router` | Meta-router: routes to social or long-form based on platform |
| `copy-framework-router` | Selects the optimal framework and drafts long-form copy |
| `social-media-posts` | Platform-optimized posts for LinkedIn and X |

## Installation

Clone and unzip into `~/.claude/skills/` (global) or `.claude/skills/` (project-level):

```bash
git clone https://github.com/thebenwalther/claude-skills.git
cp -r claude-skills/strategic-intervention/* ~/.claude/skills/
cp -r claude-skills/solo-business/* ~/.claude/skills/
cp -r claude-skills/copywriting/* ~/.claude/skills/
```

Skills are picked up automatically on the next Claude Code session.

## Skill format

Each skill is a folder containing a `SKILL.md` with YAML frontmatter:

```
skill-name/
  SKILL.md          # frontmatter (name, description, triggers) + prompt content
  references/       # optional supporting reference files
    *.md
```
