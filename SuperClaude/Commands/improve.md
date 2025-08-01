---
allowed-tools: [Read, Grep, Glob, Edit, MultiEdit, TodoWrite]
description: "Apply systematic improvements to code quality, performance, and maintainability"
---

# /sc:improve - Code Improvement

## Purpose
Apply systematic improvements to code quality, performance, maintainability, and best practices.

## Usage
```
/sc:improve [target] [--type quality|performance|maintainability|style] [--safe] [--tot] [--sc] [--mad]
```

## Arguments
- `target` - Files, directories, or project to improve
- `--type` - Improvement type (quality, performance, maintainability, style)
- `--safe` - Apply only safe, low-risk improvements
- `--preview` - Show improvements without applying them

### Advanced Reasoning Flags
- `--tot` - Use Tree-of-Thoughts to explore multiple improvement approaches
- `--sc` - Use Self-Consistency to validate improvement effectiveness
- `--mad` - Use Multi-Agent Debate to resolve quality trade-offs

## Execution
1. Analyze code for improvement opportunities
2. Apply advanced reasoning method selection based on improvement complexity
3. Identify specific improvement patterns and techniques using systematic exploration
4. Create improvement plan with risk assessment and multi-perspective validation
5. Apply improvements with appropriate validation
6. Verify improvements and report changes with reasoning transparency

## Advanced Reasoning Integration
- **ToT Mode**: Explores multiple improvement approaches, evaluates different optimization strategies
- **SC Mode**: Validates improvement effectiveness through multiple independent assessment paths
- **MAD Mode**: Debates quality trade-offs between refactorer, performance, architecture, and QA perspectives
- **Combined Integration**: Uses ToT for exploration, MAD for trade-off resolution, SC for validation

## Claude Code Integration
- Uses Read for comprehensive code analysis
- Leverages MultiEdit for batch improvements
- Applies TodoWrite for improvement tracking
- Maintains safety and validation mechanisms