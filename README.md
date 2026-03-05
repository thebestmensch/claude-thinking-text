<p align="center">
  <h1 align="center">Spincraft</h1>
  <p align="center">
    AI-generated spinner verbs for Claude Code, tailored to your personality.
    <br />
    <br />
    <a href="#installation">Install</a>
    &middot;
    <a href="#usage">Usage</a>
    &middot;
    <a href="https://github.com/thebestmensch/spincraft/issues">Report Bug</a>
  </p>
</p>

## About

Claude Code shows rotating phrases while it thinks — "Reasoning...", "Analyzing...", etc. Since v2.1.23, you can [customize these](https://code.claude.com/docs/en/settings) in `~/.claude/settings.json`.

Most people pick from a hardcoded list. **Spincraft** generates them for you. It asks a few questions about your vibe, interests, and preferences, then creates a set of spinner verbs that actually feel like yours.

No API keys. No dependencies. Claude Code is the AI.

## Installation

### Git clone (recommended)

```bash
git clone https://github.com/thebestmensch/spincraft.git
claude --plugin-dir ./spincraft
```

### Manual (no git, no marketplace)

If you can't install plugins or clone repos (e.g. locked-down corporate environment), you can copy the skill file directly:

```bash
mkdir -p ~/.claude/skills/spincraft-generate
```

Then create `~/.claude/skills/spincraft-generate/SKILL.md` with the contents of [`skills/generate/SKILL.md`](skills/generate/SKILL.md) from this repo.

This registers it as a personal skill at `/spincraft-generate` instead of `/spincraft:generate` — same functionality, no plugin install required.

## Usage

```
/spincraft:generate
```

Or pass a theme to skip the first question:

```
/spincraft:generate pirate
/spincraft:generate cooking
/spincraft:generate 90s hip-hop
```

### What happens

1. Claude asks you a few questions about your vibe and interests
2. Generates 20–30 custom spinner verbs
3. Lets you iterate until you're happy
4. Writes them to `~/.claude/settings.json`
5. Restart Claude Code to see your new verbs

### Modes

You'll be asked to choose a mode before writing:

| Mode | Behavior |
|------|----------|
| `replace` | Only your custom verbs are shown |
| `append` | Your verbs are mixed in with Claude's defaults |

## Example

> **Vibe:** chill · **Interests:** space, astronomy · **Avoid:** nothing specific

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

- [Claude Code](https://code.claude.com) v2.1.23 or later

## Contributing

Contributions are welcome. Open an issue or submit a pull request.

## License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for details.
