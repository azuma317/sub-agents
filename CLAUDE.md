# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the Contains Studio AI Agents collection - a comprehensive library of specialized AI agent definitions designed to accelerate rapid development cycles. The repository contains agent markdown files organized by department (engineering, design, marketing, product, etc.), each defining a specialized agent with specific capabilities and expertise.

## Project Structure

```
sub-agents/
├── engineering/         # Development-focused agents
├── design/             # UI/UX and visual design agents
├── marketing/          # Growth and marketing agents
├── product/            # Product management agents
├── project-management/ # Coordination and tracking agents
├── studio-operations/  # Operations and maintenance agents
├── testing/            # Quality assurance agents
└── bonus/              # Special purpose agents
```

## Agent File Format

Each agent is defined in a markdown file with YAML frontmatter:

```yaml
---
name: agent-name # Kebab-case identifier
description: [usage info] # When to use + examples with context
color: [color] # Visual identification
tools: Tool1, Tool2 # Available tools for the agent
---
[System prompt content - 500+ words defining agent behavior]
```

## Common Development Tasks

### Adding a New Agent

1. Create a new `.md` file in the appropriate department folder
2. Include YAML frontmatter with name, description (with 3-4 examples), color, and tools
3. Write a comprehensive system prompt (500+ words) covering:
   - Agent identity and expertise
   - Primary responsibilities (5-8 specific duties)
   - Technical skills and domain knowledge
   - Integration with 6-day sprint workflow
   - Best practices and constraints

### Testing Agents

Verify that agents:

- Activate correctly for their intended use cases
- Can access all specified tools properly
- Produce helpful and actionable outputs
- Handle edge cases appropriately
- Work well in multi-agent workflows

### Modifying Existing Agents

When updating agents:

1. Preserve the YAML frontmatter structure
2. Ensure examples accurately reflect real usage patterns
3. Maintain consistency with the 6-day sprint philosophy
4. Test changes with real project scenarios

## Key Concepts

### 6-Day Sprint Philosophy

All agents are designed to support rapid development cycles where ideas go from concept to shipped product in 6 days. Agents prioritize speed, iteration, and user feedback over perfection.

### Proactive Agents

Some agents trigger automatically:

- **studio-coach**: Complex multi-agent coordination
- **test-writer-fixer**: After code modifications
- **whimsy-injector**: After UI/UX changes
- **experiment-tracker**: When feature flags are added

### Agent Collaboration

Agents are designed to work together on complex tasks. Multiple agents can be invoked for different aspects of a project.

## Installation for End Users

Users should copy agent files to their Claude Code agents directory:

```bash
cp -r * ~/.claude/agents/
```

Then restart Claude Code to load the new agents.
