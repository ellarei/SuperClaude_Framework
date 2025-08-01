---
allowed-tools: [Read, Grep, Glob, Bash, Write]
description: "Generate comprehensive project documentation and knowledge base"
---

# /sc:index - Project Documentation

## Purpose
Create and maintain comprehensive project documentation, indexes, and knowledge bases.

## Usage
```
/sc:index [target] [--type docs|api|structure|readme] [--scope file|module|project|system] [--format md|json|yaml] [--plan] [--validate] [--uc] [--c7] [--seq]
```

## Arguments
- `target` - Project directory or specific component to document

### Core Indexing Flags
- `--type` - Documentation type (docs, api, structure, readme, changelog, wiki)
- `--scope` - Indexing scope (file, module, project, system)
- `--format` - Output format (md, json, yaml, html, pdf)
- `--update` - Update existing documentation indices
- `--recursive` - Recursively index subdirectories
- `--exclude` - Exclude specific files or directories

### Planning & Analysis Flags
- `--plan` - Display indexing plan and structure
- `--think` - Multi-file analysis for comprehensive indexing
- `--validate` - Pre-indexing validation and completeness checks

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized index generation
- `--safe-mode` - Conservative indexing with extensive validation
- `--verbose` - Detailed indexing process and explanations

### MCP Server Control Flags
- `--c7` / `--context7` - Enable Context7 for documentation patterns and standards
- `--seq` / `--sequential` - Enable Sequential for complex indexing orchestration
- `--all-mcp` - Enable all MCP servers for comprehensive indexing support
- `--no-mcp` - Native tools only for faster index generation

### Index Quality Flags
- `--searchable` - Generate searchable index with keywords
- `--categorized` - Organize index by categories and tags
- `--navigation` - Include navigation structure and breadcrumbs
- `--metadata` - Include file metadata and statistics

### Persona Integration Flags
- `--persona-scribe` - Documentation specialist for professional indexing
- `--persona-architect` - Systems architect for structural organization

## Execution
1. Analyze project structure and identify key components
2. Extract documentation from code comments and README files
3. Generate comprehensive documentation based on type
4. Create navigation structure and cross-references
5. Output formatted documentation with proper organization

## Claude Code Integration
- Uses Glob for systematic file discovery
- Leverages Grep for extracting documentation patterns
- Applies Write for creating structured documentation
- Maintains consistency with project conventions