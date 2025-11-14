# Claude Tools Registry

This is a test registry for the Claude Nia Tool Management CLI (cntm).

## Structure

The registry contains a `registry.json` file that lists available tools for Claude Code:

- **Agents**: Autonomous helpers for complex tasks
- **Commands**: Custom slash commands
- **Skills**: Reusable knowledge and patterns

## Registry Format

```json
{
  "version": "1.0.0",
  "updated_at": "2024-11-14T12:00:00Z",
  "tools": {
    "agent": [...],
    "command": [...],
    "skill": [...]
  }
}
```

## Usage

This registry is used by the `cntm` CLI tool:

```bash
# Search for tools
cntm search "code review"

# List all tools
cntm list --remote

# Get tool info
cntm info code-reviewer
```

## Configuration

Point your cntm configuration to this registry:

```yaml
registry:
  url: https://github.com/nghiadoan-work/claude-tools-registry
  branch: main
```

## Tools Included

### Agents
- **code-reviewer**: Automated code review agent
- **git-helper**: Git workflow automation
- **test-generator**: Automatic test generation

### Commands
- **test-coverage**: Coverage reports and analysis
- **deploy-preview**: PR preview environments

### Skills
- **github-api**: GitHub API patterns
- **docker-best-practices**: Docker optimization techniques
