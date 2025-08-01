---
allowed-tools: [Read, Grep, Glob, Write, Edit, TodoWrite]
description: "Design system architecture, APIs, and component interfaces"
---

# /sc:design - System and Component Design

## Purpose
Design system architecture, APIs, component interfaces, and technical specifications.

## Usage
```
/sc:design [target] [--type architecture|api|component|database] [--format diagram|spec|code] [--tot] [--mad] [--sc]
```

## Arguments
- `target` - System, component, or feature to design
- `--type` - Design type (architecture, api, component, database)
- `--format` - Output format (diagram, spec, code)
- `--iterative` - Enable iterative design refinement

### Advanced Reasoning Flags
- `--tot` - Use Tree-of-Thoughts to explore multiple design approaches systematically
- `--mad` - Use Multi-Agent Debate for stakeholder-driven design decisions
- `--sc` - Use Self-Consistency to validate design choices through multiple reasoning paths

## Execution
1. Analyze requirements and design constraints
2. Apply advanced reasoning method selection based on design complexity
3. Create initial design concepts and alternatives using systematic exploration
4. Develop detailed design specifications with multi-perspective validation
5. Validate design against requirements and best practices
6. Generate design documentation and implementation guides with reasoning rationale

## Advanced Reasoning Integration
- **ToT Mode**: Systematically explores multiple design alternatives, evaluates trade-offs between approaches
- **MAD Mode**: Debates design decisions from architect, frontend, backend, security, and performance perspectives
- **SC Mode**: Validates design choices through multiple independent reasoning paths
- **Sequential Integration**: ToT → MAD → SC for comprehensive design exploration, stakeholder alignment, and validation

## Claude Code Integration
- Uses Read for requirement analysis
- Leverages Write for design documentation
- Applies TodoWrite for design task tracking
- Maintains consistency with architectural patterns