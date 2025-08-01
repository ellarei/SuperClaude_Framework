---
allowed-tools: [Read, Grep, Glob, Bash]
description: "Provide development estimates for tasks, features, or projects"
---

# /sc:estimate - Development Estimation

## Purpose
Generate accurate development estimates for tasks, features, or projects based on complexity analysis.

## Usage
```
/sc:estimate [target] [--type time|effort|complexity|cost] [--scope file|module|project|system] [--unit hours|days|weeks] [--plan] [--validate] [--uc] [--seq] [--c7]
```

## Arguments
- `target` - Task, feature, or project to estimate

### Core Estimation Flags
- `--type` - Estimation type (time, effort, complexity, cost, risk, resources)
- `--scope` - Estimation scope (file, module, project, system)
- `--unit` - Time unit for estimates (hours, days, weeks, months)
- `--breakdown` - Provide detailed breakdown of estimates
- `--confidence` - Include confidence intervals for estimates
- `--methodology` - Estimation methodology (agile, waterfall, bottom-up, top-down)

### Planning & Analysis Flags
- `--plan` - Display estimation plan and approach
- `--think` - Multi-file analysis for complex estimation scenarios
- `--think-hard` - Deep estimation analysis for large projects
- `--validate` - Pre-estimation validation and feasibility checks

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized estimation reporting
- `--safe-mode` - Conservative estimates with risk buffers
- `--verbose` - Detailed estimation rationale and assumptions

### MCP Server Control Flags
- `--seq` / `--sequential` - Enable Sequential for systematic estimation analysis
- `--c7` / `--context7` - Enable Context7 for estimation patterns and benchmarks
- `--all-mcp` - Enable all MCP servers for comprehensive estimation support
- `--no-mcp` - Native tools only for faster estimation generation

### Estimation Quality Flags
- `--historical` - Use historical data for estimation accuracy
- `--team-velocity` - Factor in team velocity and capacity
- `--risk-adjusted` - Include risk adjustments in estimates
- `--dependencies` - Account for external dependencies

### Persona Integration Flags
- `--persona-architect` - Systems architect for technical complexity estimation
- `--persona-analyzer` - Analysis specialist for detailed breakdown
- `--persona-performance` - Performance specialist for optimization estimates

## Execution
1. Analyze scope and requirements of target
2. Identify complexity factors and dependencies
3. Apply estimation methodologies and historical data
4. Generate estimates with confidence intervals
5. Present detailed breakdown with risk factors

## Claude Code Integration
- Uses Read for requirement analysis
- Leverages Glob for codebase complexity assessment
- Applies Grep for pattern-based estimation
- Maintains structured estimation documentation