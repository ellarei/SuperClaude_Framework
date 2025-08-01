---
allowed-tools: [Read, Grep, Glob, Bash, Write]
description: "Load and analyze project context, configurations, and dependencies"
---

# /sc:load - Project Context Loading

## Purpose
Load and analyze project context, configurations, dependencies, and environment setup.

## Usage
```
/sc:load [target] [--type project|config|deps|env] [--scope file|module|project|system] [--cache] [--plan] [--validate] [--uc] [--c7] [--seq]
```

## Arguments
- `target` - Project directory or specific configuration to load

### Core Loading Flags
- `--type` - Loading type (project, config, deps, env, schema, state)
- `--scope` - Loading scope (file, module, project, system)
- `--cache` - Cache loaded context for faster subsequent access
- `--refresh` - Force refresh of cached context
- `--deep` - Deep loading with dependency analysis
- `--lazy` - Lazy loading for large projects

### Planning & Analysis Flags
- `--plan` - Display loading plan and strategy
- `--think` - Multi-file analysis for complex project loading
- `--validate` - Pre-loading validation and integrity checks

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized loading reports
- `--safe-mode` - Conservative loading with extensive validation
- `--verbose` - Detailed loading process and diagnostics

### MCP Server Control Flags
- `--c7` / `--context7` - Enable Context7 for configuration patterns
- `--seq` / `--sequential` - Enable Sequential for complex loading orchestration
- `--all-mcp` - Enable all MCP servers for comprehensive loading support
- `--no-mcp` - Native tools only for faster loading operations

### Loading Quality Flags
- `--integrity` - Verify data integrity during loading
- `--performance` - Optimize loading for performance
- `--incremental` - Incremental loading for large datasets
- `--parallel` - Parallel loading for multiple resources

### Persona Integration Flags
- `--persona-architect` - Systems architect for complex project analysis
- `--persona-analyzer` - Analysis specialist for detailed context loading
- `--persona-devops` - DevOps specialist for environment and configuration loading

## Execution
1. Discover and analyze project structure and configuration files
2. Load dependencies, environment variables, and settings
3. Parse and validate configuration consistency
4. Create comprehensive project context map
5. Cache context for efficient future access

## Claude Code Integration
- Uses Glob for comprehensive project discovery
- Leverages Read for configuration analysis
- Applies Bash for environment validation
- Maintains efficient context caching mechanisms