---
allowed-tools: [Bash, Read, Glob, TodoWrite, Edit]
description: "Git operations with intelligent commit messages and branch management"
---

# /sc:git - Git Operations

## Purpose
Execute Git operations with intelligent commit messages, branch management, and workflow optimization.

## Usage
```
/sc:git [operation] [args] [--smart-commit] [--branch-strategy] [--scope project|module|feature] [--plan] [--validate] [--uc] [--seq]
```

## Arguments
- `operation` - Git operation (add, commit, push, pull, merge, branch, status, rebase, cherry-pick)
- `args` - Operation-specific arguments

### Core Git Flags
- `--smart-commit` - Generate intelligent commit messages with conventional format
- `--branch-strategy` - Apply branch naming conventions (feature/, bugfix/, hotfix/)
- `--scope` - Operation scope (project, module, feature)
- `--interactive` - Interactive mode for complex operations
- `--dry-run` - Preview git operations without executing
- `--force-safe` - Safe force operations with additional validation

### Planning & Analysis Flags
- `--plan` - Display git operation plan and impact analysis
- `--think` - Multi-file analysis for complex git operations
- `--validate` - Pre-operation validation and conflict detection

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized git reporting
- `--safe-mode` - Conservative git operations with extensive validation
- `--verbose` - Detailed git operation output and explanations

### MCP Server Control Flags
- `--seq` / `--sequential` - Enable Sequential for complex git workflow orchestration
- `--c7` / `--context7` - Enable Context7 for git best practices and patterns
- `--all-mcp` - Enable all MCP servers for comprehensive git support
- `--no-mcp` - Native git tools only for faster operations

### Workflow Integration Flags
- `--conventional-commits` - Enforce conventional commit message format
- `--semantic-versioning` - Apply semantic versioning for releases
- `--changelog` - Generate changelog entries from commits
- `--pr-template` - Use pull request templates for commits

### Persona Integration Flags
- `--persona-devops` - DevOps specialist for CI/CD integration
- `--persona-scribe` - Documentation specialist for commit message quality
- `--persona-architect` - Systems architect for merge and branching strategies

## Execution
1. Analyze current Git state and repository context
2. Execute requested Git operations with validation
3. Apply intelligent commit message generation
4. Handle merge conflicts and branch management
5. Provide clear feedback and next steps

## Claude Code Integration
- Uses Bash for Git command execution
- Leverages Read for repository analysis
- Applies TodoWrite for operation tracking
- Maintains Git best practices and conventions