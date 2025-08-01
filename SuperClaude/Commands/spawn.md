---
allowed-tools: [Read, Grep, Glob, Bash, TodoWrite, Edit, MultiEdit, Write]
description: "Break complex tasks into coordinated subtasks with efficient execution"
---

# /sc:spawn - Task Orchestration

## Purpose
Decompose complex requests into manageable subtasks and coordinate their execution.

## Usage
```
/sc:spawn [task] [--sequential|--parallel] [--scope module|project|system] [--validate] [--plan] [--uc] [--delegate] [--wave-mode] [--seq]
```

## Arguments
- `task` - Complex task or project to orchestrate

### Core Orchestration Flags
- `--sequential` - Execute tasks in dependency order (default)
- `--parallel` - Execute independent tasks concurrently
- `--scope` - Orchestration scope (module, project, system)
- `--validate` - Enable quality checkpoints between tasks
- `--priority` - Task priority ordering (high, medium, low)
- `--timeout` - Set execution timeout for task orchestration

### Planning & Analysis Flags
- `--plan` - Display orchestration plan and task breakdown
- `--think` - Multi-task analysis for complex orchestration
- `--think-hard` - Deep orchestration analysis for enterprise-scale tasks

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized orchestration reporting
- `--safe-mode` - Conservative orchestration with extensive validation
- `--verbose` - Detailed orchestration process and progress

### Advanced Orchestration Flags
- `--delegate [files|folders|tasks]` - Enable sub-agent delegation for parallel processing
- `--concurrency [n]` - Control max concurrent tasks (default: 7, range: 1-15)
- `--wave-mode [auto|force|off]` - Enable wave orchestration for complex tasks
- `--wave-strategy [progressive|systematic|adaptive]` - Select wave orchestration strategy

### MCP Server Control Flags
- `--seq` / `--sequential` - Enable Sequential for complex task orchestration
- `--c7` / `--context7` - Enable Context7 for orchestration patterns
- `--all-mcp` - Enable all MCP servers for comprehensive orchestration support
- `--no-mcp` - Native tools only for faster task execution

### Quality & Monitoring Flags
- `--checkpoint` - Create checkpoints for rollback capability
- `--monitoring` - Enable real-time task monitoring
- `--recovery` - Enable automatic recovery from task failures
- `--analytics` - Generate orchestration analytics and metrics

### Persona Integration Flags
- `--persona-architect` - Systems architect for complex orchestration design
- `--persona-devops` - DevOps specialist for deployment orchestration
- `--persona-analyzer` - Analysis specialist for task breakdown and dependencies

## Execution
1. Parse request and create hierarchical task breakdown
2. Map dependencies between subtasks
3. Choose optimal execution strategy (sequential/parallel)
4. Execute subtasks with progress monitoring
5. Integrate results and validate completion

## Claude Code Integration
- Uses TodoWrite for task breakdown and tracking
- Leverages file operations for coordinated changes
- Applies efficient batching for related operations
- Maintains clear dependency management