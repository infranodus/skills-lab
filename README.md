# InfraNodus Lab

> **Placeholders, TBD:** the GitHub repository name `infranodus/infranodus-lab` and the marketplace name `infranodus-lab` are not final, and this repository is not published yet. Every command below that names them will change if the names change.

Experimental thinking, perspective and planning skills from [InfraNodus](https://infranodus.com). They moved here from [infranodus/skills](https://github.com/infranodus/skills), which now focuses on the core InfraNodus skill (knowledge graph + gap finder for your notes, vault or agent memory) and the research-to-publish workflow around it.

Several of these skills use the [InfraNodus MCP server](https://infranodus.com/mcp) for graph analysis; they still work without it, with fewer features.

## Skills

- **Actionize** (`actionize`, folder `skill-actionize`) - Turn insights, findings, or research into an actionable plan with deadlines and scheduled reminders. Collaboratively designs the plan with the user, saves it to the project, and sets up cron-based Telegram reminders for upcoming and overdue tasks. Includes a planning diagnostics mode that analyzes patterns like chronic deferral, vague tasks, and missing dependencies. Uses [InfraNodus MCP server](https://infranodus.com/mcp) to compare the original research against the plan and surface gaps. Use it after completing research or brainstorming when you have insights but no concrete next steps.

- **Critical Perspective** (`critical-perspective`, folder `skill-critical-perspective`) - Engage in critical thinking by questioning assumptions, exploring alternative perspectives, and uncovering latent topics in conversations.

- **Embodied Navigation** (`embodied-navigation`, folder `skill-embodied-navigation`) - Transfer principles from embodied movement practices (meditation, martial arts, contemporary dance, bodymind) to navigate complex situations. Maps any situation as a knowledge graph using [InfraNodus MCP server](https://infranodus.com/mcp) and reads its topology the way you'd read a body — identifying fixation points, tension patterns, neglected zones, and pivot joints. Provides four integrated toolkits: equanimous scanning (dissolving fixation loops through distributed attention), adaptive fluidity (absorbing and redirecting force instead of opposing it), tension redistribution (shifting stuck points by working on adjacent structure), and confluence (entering existing flows to redirect them from within). Use it when someone is stuck, in conflict, overwhelmed, negotiating, or when analytical thinking alone creates rigidity.

- **Perspective Reversal** (`perspective-reversal`, folder `skill-perspective-reversal`) - Flip any conflict, negotiation, or adversarial situation to the opponent's perspective to extract superior tactical advice. By reasoning from the adversary's point of view — mapping their full toolkit of moves, pressure points, and procedural weapons — and then translating each tactic into a concrete counter-move for the user. Covers landlord disputes, workplace conflicts, bureaucratic obstruction, scam attempts, debt collectors, and any scenario where someone feels stuck or outmaneuvered. Optionally uses [InfraNodus MCP server](https://infranodus.com/mcp) for discourse bias checks, search intent analysis of the adversary's playbook, and content gap detection to find blind spots.

- **Rhetorical Analyst** (`rhetorical-analyst`, folder `skill-rhetorical-analyst`) - Analyze arguments, debate tactics, and rhetorical moves across three dimensions: persuasion, rhetoric, and logic. Identifies the moves being made, scores their effectiveness, exposes hidden assumptions, tracks logical gaps, and checks for asymmetric standards — including the analyst's own. Use it to break down debates, stress-test your own arguments, or understand why something feels persuasive but wrong.

- **Shopping Assistant** (`shopping-assistant`, folder `skill-shopping`) - A systematic, multi-phase shopping research workflow that acts as your personal shopping advisor. Gathers requirements, researches product categories via web search, builds comparison matrices, analyzes reviews for recurring praise and complaints, and converges on 3-4 best options with clear reasoning. Designed to save hours of research and avoid both impulse buys and analysis paralysis.

- **Vipassana for LLMs** (`vipassana-llm`, folder `skill-vipassana-meditation`) - Apply Vipassana meditation principles to LLM processing — equanimous scanning, non-reactive observation, impermanence awareness (anicca), and breaking conditioned reaction chains (sankharas). Addresses the failure modes LLMs share with untrained minds: fixating on salient tokens, generating conditioned responses, craving coherence, and collapsing into narrative before observing raw phenomena. Use it when you want bare attention rather than premature conclusions, when conversations show reactive thinking, or when you need to dissolve fixation loops and see a situation as it really is.

## Installation

### Claude web / desktop (no terminal)

1. Download the skill's `.zip` from this repository's Releases page (zips are built by `.github/workflows/release.yml` when a `v*` tag is pushed; there are none until the first release here).
2. In Claude, open **Settings → Capabilities**, turn on **Code execution and file creation**, then click **Upload Skill** in the Skills section and pick the zip.

### Claude Code

Already using the `infranodus-skills` marketplace? Nothing changes: the same ids (for example `/plugin install actionize@infranodus-skills`) now fetch the skill from this repository.

Or add this marketplace directly:

```
/plugin marketplace add infranodus/infranodus-lab
/plugin install actionize@infranodus-lab
/plugin install infranodus-lab-all@infranodus-lab    # all Lab skills + InfraNodus MCP server
```

Install a skill from **one** marketplace only; installing the same skill from both loads it twice.

### `npx skills`

```bash
npx skills add infranodus/infranodus-lab --skill actionize -g
```

### Manual copy

Copy a skill folder into `~/.claude/skills/` (or a project's `.claude/skills/`) and name the destination after the skill's `name:` field, e.g. `cp -r skill-shopping ~/.claude/skills/shopping-assistant` and `cp -r skill-vipassana-meditation ~/.claude/skills/vipassana-llm`.

## History

The skills were copied (not history-preserving) from `infranodus/skills` at commit `8e59daf` (v1.7.3). Their earlier history lives in that repository.

## License

Code (scripts, plugin manifests) is licensed under [Apache-2.0](LICENSE); the skill content (`SKILL.md` files and other Markdown) under [CC BY 4.0](LICENSE). When you share or adapt the skills, credit them as "InfraNodus Skills by InfraNodus (https://infranodus.com)". See [LICENSE](LICENSE) and [NOTICE](NOTICE).
