# QA Automation Sub-Agents

A collection of specialized Claude Code sub-agents focused on quality assurance and test automation for modern web applications.

## Available Sub-Agents

- **`angular-qa-agent`**: Specialized in testing Angular applications with best practices for component testing, service testing, and E2E automation
- **`react-qa-agent`**: Expert in React testing including unit tests with React Testing Library, component testing, and integration testing strategies
- **`playwright-env-setup-agent`**: Handles Playwright test environment setup, configuration, and best practices for cross-browser testing automation

## Usage

These sub-agents can be used automatically by Claude Code when QA or testing tasks are detected, or explicitly invoked:

```bash
# Automatic delegation
"Create comprehensive tests for my React component"
"Set up Playwright for cross-browser testing"
"Review my Angular service tests"

# Explicit invocation
@react-qa-agent Create unit tests for this user authentication component
@angular-qa-agent Review my component testing strategy
@playwright-env-setup-agent Configure Playwright for CI/CD pipeline
```

## Installation

Copy the desired sub-agents to your project or user agents directory:

```bash
# Project-specific
cp agents/qa-automation/* /path/to/your/project/.claude/agents/

# User-level
cp agents/qa-automation/* ~/.claude/agents/
```