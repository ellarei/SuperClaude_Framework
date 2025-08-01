---
allowed-tools: [Read, Grep, Glob, Write, Edit]
description: "Create focused documentation for specific components or features"
---

# /sc:document - Focused Documentation

## Purpose
Generate precise, focused documentation for specific components, functions, or features.

## Usage
```
/sc:document [target] [--type inline|external|api|guide] [--scope file|module|project] [--style brief|detailed] [--plan] [--validate] [--uc] [--c7] [--seq]
```

## Arguments
- `target` - Specific file, function, or component to document

### Core Documentation Flags
- `--type` - Documentation type (inline, external, api, guide, tutorial, reference)
- `--scope` - Documentation scope (file, module, project, system)
- `--style` - Documentation style (brief, detailed, comprehensive)
- `--template` - Use specific documentation template
- `--format` - Output format (markdown, html, pdf, json)
- `--language` - Documentation language (en, es, fr, de, etc.)

### Planning & Analysis Flags
- `--plan` - Display documentation plan and structure
- `--think` - Multi-file documentation analysis for comprehensive coverage
- `--validate` - Pre-documentation validation and completeness checks

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized documentation generation
- `--safe-mode` - Conservative documentation with extensive validation
- `--verbose` - Detailed documentation generation process

### MCP Server Control Flags
- `--c7` / `--context7` - Enable Context7 for documentation patterns and standards
- `--seq` / `--sequential` - Enable Sequential for complex documentation orchestration
- `--all-mcp` - Enable all MCP servers for comprehensive documentation support
- `--no-mcp` - Native tools only for faster documentation generation

### Documentation Quality Flags
- `--accessibility` - Ensure documentation accessibility compliance
- `--seo-optimized` - Optimize documentation for search engines
- `--interactive` - Include interactive examples and code snippets
- `--multilingual` - Generate documentation in multiple languages

### Persona Integration Flags
- `--persona-scribe` - Professional writer and documentation specialist
- `--persona-mentor` - Educational specialist for tutorial content
- `--persona-architect` - Systems architect for technical documentation

## Execution
1. Analyze target component and extract key information
2. Identify documentation requirements and audience
3. Generate appropriate documentation based on type and style
4. Apply consistent formatting and structure
5. Integrate with existing documentation ecosystem

## Claude Code Integration
- Uses Read for deep component analysis
- Leverages Edit for inline documentation updates
- Applies Write for external documentation creation
- Maintains documentation standards and conventions