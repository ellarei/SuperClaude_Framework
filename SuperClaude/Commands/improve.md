---
allowed-tools: [Read, Grep, Glob, Edit, MultiEdit, TodoWrite]
description: "Apply systematic improvements to code quality, performance, and maintainability"
---

# /sc:improve - Code Improvement

## Purpose
Apply systematic improvements to code quality, performance, maintainability, and best practices.

## Usage
```
/sc:improve [target] [--type quality|performance|maintainability|style] [--scope file|module|project|system] [--safe] [--tot] [--sc] [--mad] [--plan] [--validate] [--uc] [--loop]
```

## Arguments
- `target` - Files, directories, or project to improve

### Core Improvement Flags
- `--type` - Improvement type (quality, performance, maintainability, style, security, accessibility)
- `--scope` - Improvement scope (file, module, project, system)
- `--safe` - Apply only safe, low-risk improvements
- `--preview` - Show improvements without applying them
- `--aggressive` - More thorough improvements with higher impact

### Planning & Analysis Flags
- `--plan` - Display improvement plan before execution
- `--think` - Multi-file improvement analysis for complex refactoring
- `--think-hard` - Deep architectural improvement analysis
- `--validate` - Pre-improvement validation and impact assessment

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized improvement reporting
- `--safe-mode` - Conservative improvements with extensive validation
- `--verbose` - Detailed improvement explanations and rationale

### Iterative Improvement Flags
- `--loop` - Enable iterative improvement mode (auto-activates for polish/refine requests)
- `--iterations [n]` - Control number of improvement cycles (default: 3, range: 1-10)
- `--interactive` - User confirmation between improvement iterations

### MCP Server Control Flags
- `--seq` / `--sequential` - Enable Sequential for systematic improvement analysis
- `--c7` / `--context7` - Enable Context7 for improvement patterns and best practices
- `--all-mcp` - Enable all MCP servers for comprehensive improvement support
- `--no-mcp` - Native tools only for faster improvements

### Advanced Reasoning Flags
- `--tot` / `--tree-of-thoughts` - Explore multiple improvement approaches systematically
- `--tot-branches [n]` - Number of improvement branches (default: 4, range: 2-8)
- `--sc` / `--self-consistency` - Validate improvement effectiveness through multiple paths
- `--sc-paths [n]` - Number of validation paths (default: 3, range: 2-5)
- `--mad` / `--multi-agent-debate` - Resolve quality trade-offs through expert debate
- `--mad-agents [personas]` - Specific personas for improvement debate (e.g., "refactorer,performance,security")

### Persona Integration Flags
- `--persona-refactorer` - Code quality specialist for maintainability improvements
- `--persona-performance` - Optimization specialist for performance improvements
- `--persona-security` - Security specialist for security hardening
- `--persona-architect` - Systems architect for structural improvements

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