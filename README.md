# Spincraft

A Claude Code plugin that generates personalized spinner verbs using AI. Instead of picking from a hardcoded list, Claude asks you a few questions about your vibe, interests, and preferences — then generates a custom set of spinner verbs tailored to you.

## What are spinner verbs?

Spinner verbs are the rotating phrases Claude Code shows while it's thinking — "Reasoning...", "Analyzing...", etc. Since v2.1.23, you can customize these in `~/.claude/settings.json`. This plugin makes that fun and easy.

## Install

### From a marketplace

```bash
claude plugin install spincraft
```

### Manual install

Clone this repo and load it directly:

```bash
git clone https://github.com/thebestmensch/spincraft.git
claude --plugin-dir ./spincraft
```

## Usage

Once the plugin is loaded, run:

```
/spincraft:generate
```

Or pass a theme to get started faster:

```
/spincraft:generate pirate
/spincraft:generate cooking
/spincraft:generate 90s hip-hop
```

Claude will:

1. Ask you a few questions about your vibe and interests
2. Generate 20-30 custom spinner verbs
3. Let you iterate until you're happy
4. Write them to your `~/.claude/settings.json`

Restart Claude Code after generating to see your new verbs in action.

## Modes

When installing your verbs, you'll be asked to choose:

- **replace** — Only your custom verbs are shown (Claude's defaults are removed)
- **append** — Your verbs are mixed in with Claude's defaults

## Example output

After telling Claude you're into space and want a chill vibe, you might get:

```
Orbiting the problem
Consulting the stars
Drifting through possibilities
Aligning the satellites
Warming up the thrusters
Scanning the horizon
Charting a course
Entering the atmosphere
```

## Requirements

- Claude Code v2.1.23 or later
- That's it. No API keys, no dependencies. Claude Code is the AI.

## License

MIT
