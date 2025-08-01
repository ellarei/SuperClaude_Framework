---
allowed-tools: [Read, Grep, Glob, Bash, TodoWrite]
description: "Diagnose and resolve issues in code, builds, or system behavior"
---

# /sc:troubleshoot - Issue Diagnosis and Resolution

## Purpose
Systematically diagnose and resolve issues in code, builds, deployments, or system behavior.

## Usage
```
/sc:troubleshoot [issue] [--type bug|build|performance|deployment] [--scope file|module|project|system] [--trace] [--fix] [--plan] [--validate] [--uc] [--seq] [--play]
```

## Arguments
- `issue` - Description of the problem or error message

### Core Troubleshooting Flags
- `--type` - Issue category (bug, build, performance, deployment, security, integration)
- `--scope` - Troubleshooting scope (file, module, project, system)
- `--trace` - Enable detailed tracing and logging
- `--fix` - Automatically apply fixes when safe
- `--reproduce` - Attempt to reproduce the issue systematically
- `--root-cause` - Focus on root cause analysis rather than quick fixes

### Planning & Analysis Flags
- `--plan` - Display troubleshooting plan and investigation strategy
- `--think` - Multi-file analysis for complex issue investigation
- `--think-hard` - Deep system analysis for complex bugs
- `--validate` - Pre-fix validation and impact assessment

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized troubleshooting reports
- `--safe-mode` - Conservative fixes with extensive validation
- `--verbose` - Detailed investigation steps and reasoning

### MCP Server Control Flags
- `--seq` / `--sequential` - Enable Sequential for systematic debugging analysis
- `--play` / `--playwright` - Enable Playwright for E2E testing and browser issues
- `--c7` / `--context7` - Enable Context7 for framework-specific troubleshooting
- `--all-mcp` - Enable all MCP servers for comprehensive issue analysis
- `--no-mcp` - Native tools only for faster troubleshooting

### Persona Integration Flags
- `--persona-analyzer` - Root cause specialist for systematic investigation
- `--persona-qa` - Quality assurance specialist for testing-related issues
- `--persona-performance` - Performance specialist for optimization issues
- `--persona-security` - Security specialist for vulnerability-related problems

## Execution
1. Analyze issue description and gather initial context
2. Identify potential root causes and investigation paths
3. Execute systematic debugging and diagnosis
4. Propose and validate solution approaches
5. Apply fixes and verify resolution

## Claude Code Integration
- Uses Read for error log analysis
- Leverages Bash for runtime diagnostics
- Applies Grep for pattern-based issue detection
- Maintains structured troubleshooting documentation