---
allowed-tools: [Read, Grep, Glob, Bash, TodoWrite]
description: "Analyze code quality, security, performance, and architecture"
---

# /sc:analyze - Code Analysis

## Purpose
Execute comprehensive code analysis across quality, security, performance, and architecture domains.

## Usage
```
/sc:analyze [target] [--focus quality|security|performance|architecture] [--scope file|module|project|system] [--depth quick|deep] [--tot] [--sc] [--mad] [--plan] [--think] [--uc] [--validate]
```

## Arguments
- `target` - Files, directories, or project to analyze

### Core Analysis Flags
- `--focus` - Analysis focus area (quality, security, performance, architecture, accessibility, testing)
- `--scope` - Analysis scope (file, module, project, system)
- `--depth` - Analysis depth (quick, deep)
- `--format` - Output format (text, json, report)

### Planning & Analysis Flags
- `--plan` - Display execution plan before analysis operations
- `--think` - Multi-file analysis (~4K tokens) with Sequential MCP integration
- `--think-hard` - Deep architectural analysis (~10K tokens) for system-wide analysis
- `--ultrathink` - Critical system redesign analysis (~32K tokens) for complex problems

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - 30-50% token reduction using symbols and structured output
- `--validate` - Pre-operation validation and risk assessment (auto-activates for risk >0.7)
- `--safe-mode` - Maximum validation with conservative execution
- `--verbose` - Maximum detail and explanation (high token usage)

### MCP Server Control Flags
- `--seq` / `--sequential` - Enable Sequential for complex multi-step analysis (auto-activates for complex debugging)
- `--c7` / `--context7` - Enable Context7 for framework documentation and patterns
- `--all-mcp` - Enable all MCP servers simultaneously (auto-activates for complexity >0.8)
- `--no-mcp` - Disable all MCP servers, use native tools only (40-60% faster execution)

### Advanced Reasoning Flags
- `--tot` / `--tree-of-thoughts` - Systematic tree search reasoning with branch generation
- `--tot-branches [n]` - Number of initial branches (default: 4, range: 2-8)
- `--tot-depth [n]` - Maximum tree search depth (default: 3, range: 1-5)
- `--sc` / `--self-consistency` - Multiple independent reasoning paths with consensus validation
- `--sc-paths [n]` - Number of reasoning paths (default: 3, range: 2-5)
- `--mad` / `--multi-agent-debate` - Adversarial reasoning with persona-based debate
- `--mad-agents [personas]` - Specific personas for debate (e.g., "architect,security,performance")
- `--mad-rounds [n]` - Number of debate rounds (default: 3, range: 2-5)

### Persona Integration Flags
- `--persona-analyzer` - Root cause specialist for systematic investigation
- `--persona-architect` - Systems architecture specialist for structural analysis
- `--persona-security` - Threat modeler for vulnerability assessment
- `--persona-performance` - Optimization specialist for bottleneck identification

### Sub-Agent Delegation Flags
- `--delegate [files|folders|auto]` - Enable parallel processing delegation (auto-activates >7 directories)
- `--concurrency [n]` - Control max concurrent sub-agents (default: 7, range: 1-15)

## Auto-Activation Patterns

### Planning & Analysis Auto-Activation
- `--think` - Auto-activates: Import chains >5 files, cross-module calls >10 references
- `--think-hard` - Auto-activates: System refactoring, bottlenecks >3 modules, security vulnerabilities
- `--ultrathink` - Auto-activates: Legacy modernization, critical vulnerabilities, performance degradation >50%

### Efficiency Auto-Activation
- `--uc` - Auto-activates: Context usage >75% or large-scale operations
- `--validate` - Auto-activates: Risk score >0.7 or resource usage >75%
- `--safe-mode` - Auto-activates: Resource usage >85% or production environment

### MCP Server Auto-Activation
- `--seq` - Auto-activates: Complex debugging, system design, --think flags
- `--c7` - Auto-activates: External library imports, framework questions
- `--all-mcp` - Auto-activates: Problem complexity >0.8, multi-domain indicators

### Persona Auto-Activation
- `analyzer` - Auto-activates: Debug/troubleshoot keywords, complex issue investigation
- `architect` - Auto-activates: Architecture keywords, system design, complexity >0.7
- `security` - Auto-activates: Vulnerability/threat keywords, security audit requests
- `performance` - Auto-activates: Performance issues, optimization requests, bottlenecks

### Sub-Agent Auto-Activation
- `--delegate` - Auto-activates: >7 directories or >50 files detected
- `--concurrency` - Auto-adjusts based on system resources and complexity

## Execution
1. **Pre-Analysis Planning** - Apply --plan flag for execution strategy
2. **Context Loading** - Auto-activate MCP servers based on analysis domain
3. **Reasoning Selection** - Choose optimal reasoning method (ToT/SC/MAD) based on complexity
4. **File Discovery** - Systematically discover and categorize files for analysis
5. **Multi-Perspective Analysis** - Apply appropriate analysis tools with persona integration
6. **Advanced Reasoning** - Generate findings with severity ratings using selected reasoning methods
7. **Quality Validation** - Apply validation gates and safety checks
8. **Report Generation** - Create actionable recommendations with reasoning transparency

## Advanced Reasoning Integration
- **ToT Mode**: Explores multiple analysis approaches systematically, evaluates different perspectives with configurable branch depth
- **SC Mode**: Validates critical findings through multiple independent analysis paths with consensus mechanisms
- **MAD Mode**: Debates findings from quality, security, performance, and architecture perspectives with structured rounds
- **Combined Integration**: Uses ToT for exploration, MAD for perspective integration, SC for validation with full reasoning transparency

## Claude Code Integration
- Uses Glob for systematic file discovery
- Leverages Grep for pattern-based analysis
- Applies Read for deep code inspection
- Maintains structured analysis reporting