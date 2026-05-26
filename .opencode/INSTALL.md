# Installing Product Superpowers for OpenCode

## Prerequisites

- [OpenCode.ai](https://opencode.ai) installed

## Installation

Add product-superpowers to the `plugin` array in your `opencode.json` (global or project-level):

```json
{
  "plugin": ["product-superpowers@git+https://github.com/your-org/product-superpowers.git"]
}
```

Restart OpenCode. The plugin installs through OpenCode's plugin manager and registers all skills.

Verify by asking: "Tell me about your product superpowers"

## Usage

Use OpenCode's native `skill` tool:

```
use skill tool to list skills
use skill tool to load product-superpowers/product-discovery
```

## Updating

OpenCode installs Product Superpowers through a git-backed package spec. Some OpenCode and Bun versions pin that resolved git dependency in a lockfile or cache, so a restart may not pick up the newest commit. If updates do not appear, clear OpenCode's package cache or reinstall the plugin.

To pin a specific version:

```json
{
  "plugin": ["product-superpowers@git+https://github.com/your-org/product-superpowers.git#v1.0.0"]
}
```

## Tool Mapping

When skills reference Claude Code tools:
- `TodoWrite` → `todowrite`
- `Task` with subagents → `@mention` syntax
- `Skill` tool → OpenCode's native `skill` tool
- File operations → your native tools

## Getting Help

Report issues at the repository.
Full documentation: see README.md
