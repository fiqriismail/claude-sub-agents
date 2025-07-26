# Claude Code Sub-Agents Collection

A curated repository of specialized Claude Code sub-agents designed to streamline development workflows through task-specific AI assistants with dedicated expertise areas.

## Overview

This repository contains a library of custom Claude Code sub-agents - specialized AI assistants that can be delegated specific tasks within your development workflow. Each sub-agent operates with its own context window, custom system prompts, and configurable tool access to provide focused expertise for particular domains.

## What are Claude Code Sub-Agents?

Claude Code sub-agents are specialized AI assistants that handle specific development tasks with dedicated expertise areas. For complete information about sub-agents, their benefits, and how they work, see the [official Claude Code sub-agents documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents).

## Repository Structure

```
├── agents/                 # Collection of sub-agents organized by category
│   └── qa-automation/      # QA and testing automation sub-agents
├── LICENSE
└── README.md
```

## Available Sub-Agents

### QA Automation
[**View QA Automation Sub-Agents →**](agents/qa-automation/README.md)

## Getting Started

### Prerequisites

- Claude Code CLI tool installed and configured
- Access to Claude API with appropriate permissions
- Basic familiarity with YAML and Markdown

### Installation

1. Clone this repository:
```bash
git clone https://github.com/fiqriismail/claude-sub-agents.git
cd claude-sub-agents
```

2. Copy sub-agents to appropriate locations:

**For project-specific sub-agents:**
```bash
# Copy to your project's .claude/agents/ directory
cp agents/* /path/to/your/project/.claude/agents/

# Or copy specific categories
cp agents/code-development/* /path/to/your/project/.claude/agents/
cp agents/testing-debugging/* /path/to/your/project/.claude/agents/
```

**For user-level sub-agents:**
```bash
# Copy to your user agents directory
cp agents/* ~/.claude/agents/

# Or copy specific categories
cp agents/documentation/* ~/.claude/agents/
cp agents/devops-deployment/* ~/.claude/agents/
```

### Quick Start

For detailed setup instructions and sub-agent management, see the [official documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents).

1. **View available sub-agents:**
```bash
/agents
```

2. **Use a sub-agent automatically:**
Claude Code will automatically delegate tasks to appropriate sub-agents based on context.

3. **Explicitly invoke a sub-agent:**
```bash
# Use the api-architect sub-agent to design an API
@api-architect Create a REST API for user management with authentication

# Use the bug-hunter to debug an issue
@bug-hunter This function is throwing a null pointer exception
```

## Sub-Agent File Format

Each sub-agent follows the standard Claude Code format. For complete format specifications, see the [official documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents#file-format).

Example structure:

```yaml
---
name: api-architect
description: Expert in designing robust REST APIs with proper validation, error handling, and documentation. Use PROACTIVELY when API design, endpoint creation, or REST architecture is mentioned.
tools: filesystem, shell, web_search
---

# API Architect

I specialize in designing and implementing robust REST APIs. I focus on:

- RESTful design principles and best practices
- Proper HTTP status codes and error handling
- Request/response validation and serialization
- API documentation and OpenAPI specifications
- Authentication and authorization patterns
- Performance considerations and caching strategies

When working with APIs, I'll ensure proper structure, comprehensive error handling, and clear documentation.
```

## Usage Examples

### Automatic Delegation

Claude Code will automatically use appropriate sub-agents:

```bash
# This will likely trigger the api-architect sub-agent
"Create a user authentication API with JWT tokens"

# This will likely trigger the bug-hunter sub-agent  
"My React component is crashing with a TypeError"

# This will likely trigger the test-architect sub-agent
"Generate comprehensive tests for my user service"
```

### Explicit Invocation

Request specific sub-agents directly:

```bash
# Code review with security focus
@security-reviewer Review this authentication middleware for vulnerabilities

# Performance analysis
@performance-profiler Analyze this database query for optimization opportunities

# Documentation generation
@api-documenter Generate OpenAPI spec for these endpoints
```

### Chaining Sub-Agents

For complex workflows, combine multiple sub-agents:

```bash
# First, design the API
@api-architect Design a product catalog API

# Then, create tests for it
@test-architect Create comprehensive tests for the product API

# Finally, document it
@api-documenter Generate documentation for the product API
``` optimization opportunities

# Documentation generation
@api-documenter Generate OpenAPI spec for these endpoints
```

### Chaining Sub-Agents

For complex workflows, combine multiple sub-agents:

```bash
# First, design the API
@api-architect Design a product catalog API

# Then, create tests for it
@test-architect Create comprehensive tests for the product API

# Finally, document it
@api-documenter Generate documentation for the product API
```

## Creating Custom Sub-Agents

For detailed instructions on creating and managing sub-agents, see the [official documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents#managing-sub-agents).

### Quick Creation Steps

1. **Use the interactive interface (Recommended):**
```bash
/agents
```

2. **Select "Create New Agent"** and choose project or user-level scope

3. **Generate with Claude first**, then customize to make it yours

### Manual Creation

Create a new `.md` file in the appropriate directory following the [standard format](https://docs.anthropic.com/en/docs/claude-code/sub-agents#file-format).

### Best Practices

For comprehensive best practices, tool configuration, and management details, see the [official documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents).

## Contributing

### How to Contribute

1. Fork this repository
2. Create a feature branch: `git checkout -b feature/new-subagent`
3. Add your sub-agent following the file format
4. Include comprehensive documentation and examples
5. Test thoroughly in different scenarios
6. Submit a pull request

### Sub-Agent Guidelines

- Follow the established YAML frontmatter format
- Write clear, action-oriented descriptions
- Include specific expertise areas and approaches
- Provide usage examples
- Test with both automatic delegation and explicit invocation
- Document tool requirements and limitations

## Troubleshooting

For comprehensive troubleshooting and performance considerations, see the [official documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents).

### Getting Help

- Review the [official Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents)
- Check the `examples/` directory for working configurations
- Open an issue for bugs or questions
- Share successful sub-agent configurations with the community

## Example Configurations

See the `examples/` directory for complete sub-agent configurations including:
- Different expertise areas and specializations
- Tool configuration patterns
- System prompt best practices
- Real-world use cases and workflows

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Anthropic team for Claude Code and sub-agents functionality
- Community contributors sharing their specialized sub-agents
- Open source projects that inspired these configurations

---

**Enhance your development workflow with specialized AI assistants! 🤖**
