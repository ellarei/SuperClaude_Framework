---
allowed-tools: [Read, Grep, Glob, Bash, Edit, MultiEdit]
description: "Clean up code, remove dead code, and optimize project structure"
---

# /sc:cleanup - Code and Project Cleanup

## Purpose
Systematically clean up code, remove dead code, optimize imports, and improve project structure.

## Usage
```
/sc:cleanup [target] [--type code|imports|files|all] [--scope file|module|project|system] [--safe|--aggressive] [--plan] [--validate] [--uc] [--seq]
```

## Arguments
- `target` - Files, directories, or entire project to clean

### Core Cleanup Flags
- `--type` - Cleanup type (code, imports, files, all, dependencies, cache)
- `--scope` - Cleanup scope (file, module, project, system)
- `--safe` - Conservative cleanup with minimal risk (default)
- `--aggressive` - More thorough cleanup with higher impact
- `--dry-run` - Preview changes without applying them
- `--backup` - Create backup before cleanup operations

### Planning & Analysis Flags
- `--plan` - Display cleanup plan and impact analysis
- `--think` - Multi-file cleanup analysis for complex projects
- `--validate` - Pre-cleanup validation and dependency checks

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized cleanup reporting
- `--safe-mode` - Maximum validation with conservative cleanup
- `--verbose` - Detailed cleanup process and explanations

### MCP Server Control Flags
- `--seq` / `--sequential` - Enable Sequential for systematic cleanup orchestration
- `--c7` / `--context7` - Enable Context7 for cleanup patterns and best practices
- `--all-mcp` - Enable all MCP servers for comprehensive cleanup support
- `--no-mcp` - Native tools only for faster cleanup operations

### Cleanup Quality Flags
- `--dead-code` - Focus on dead code elimination
- `--unused-deps` - Remove unused dependencies
- `--optimize-imports` - Optimize and organize import statements
- `--format-code` - Apply code formatting during cleanup

### Persona Integration Flags
- `--persona-refactorer` - Code quality specialist for systematic cleanup
- `--persona-performance` - Performance specialist for optimization-focused cleanup
- `--persona-architect` - Systems architect for structural cleanup

## Execution
1. Analyze target for cleanup opportunities
2. Identify dead code, unused imports, and redundant files
3. Create cleanup plan with risk assessment
4. Execute cleanup operations with appropriate safety measures
5. Validate changes and report cleanup results

## Claude Code Integration
- Uses Glob for systematic file discovery
- Leverages Grep for dead code detection
- Applies MultiEdit for batch cleanup operations
- Maintains backup and rollback capabilities