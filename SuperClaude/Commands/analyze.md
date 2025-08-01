---
allowed-tools: [Read, Grep, Glob, Bash, TodoWrite]
description: "Analyze code quality, security, performance, and architecture"
---

# /sc:analyze - Code Analysis

## Purpose
Execute comprehensive code analysis across quality, security, performance, and architecture domains.

## Usage
```
/sc:analyze [target] [--focus quality|security|performance|architecture] [--depth quick|deep] [--tot] [--sc] [--mad]
```

## Arguments
- `target` - Files, directories, or project to analyze
- `--focus` - Analysis focus area (quality, security, performance, architecture)
- `--depth` - Analysis depth (quick, deep)
- `--format` - Output format (text, json, report)

### Advanced Reasoning Flags
- `--tot` - Use Tree-of-Thoughts for systematic analysis exploration
- `--sc` - Use Self-Consistency for critical analysis validation
- `--mad` - Use Multi-Agent Debate for multi-perspective analysis

## Execution
1. Discover and categorize files for analysis
2. Select reasoning method based on complexity and requirements
3. Apply appropriate analysis tools and techniques
4. Generate findings with severity ratings using advanced reasoning
5. Create actionable recommendations with priorities
6. Present comprehensive analysis report with reasoning transparency

## Advanced Reasoning Integration
- **ToT Mode**: Explores multiple analysis approaches systematically, evaluates different perspectives
- **SC Mode**: Validates critical findings through multiple independent analysis paths
- **MAD Mode**: Debates findings from quality, security, performance, and architecture perspectives
- **Combined**: Uses ToT for exploration, MAD for perspective integration, SC for validation

## Claude Code Integration
- Uses Glob for systematic file discovery
- Leverages Grep for pattern-based analysis
- Applies Read for deep code inspection
- Maintains structured analysis reporting