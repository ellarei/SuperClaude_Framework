---
allowed-tools: [Read, Grep, Glob, Bash]
description: "Provide clear explanations of code, concepts, or system behavior"
---

# /sc:explain - Code and Concept Explanation

## Purpose
Deliver clear, comprehensive explanations of code functionality, concepts, or system behavior.

## Usage
```
/sc:explain [target] [--level basic|intermediate|advanced] [--scope file|module|project|system] [--format text|diagram|examples] [--plan] [--validate] [--uc] [--c7] [--seq]
```

## Arguments
- `target` - Code file, function, concept, or system to explain

### Core Explanation Flags
- `--level` - Explanation complexity (basic, intermediate, advanced, expert)
- `--scope` - Explanation scope (file, module, project, system)
- `--format` - Output format (text, diagram, examples, interactive, video-script)
- `--context` - Additional context for explanation
- `--audience` - Target audience (developer, manager, student, expert)
- `--language` - Explanation language (en, es, fr, de, etc.)

### Planning & Analysis Flags
- `--plan` - Display explanation plan and structure
- `--think` - Multi-file analysis for comprehensive explanations
- `--validate` - Pre-explanation validation and accuracy checks

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized explanations
- `--safe-mode` - Conservative explanations with extensive validation
- `--verbose` - Detailed explanation process and reasoning

### MCP Server Control Flags
- `--c7` / `--context7` - Enable Context7 for framework-specific explanations
- `--seq` / `--sequential` - Enable Sequential for complex explanation orchestration
- `--all-mcp` - Enable all MCP servers for comprehensive explanation support
- `--no-mcp` - Native tools only for faster explanation generation

### Explanation Quality Flags
- `--interactive` - Include interactive examples and code snippets
- `--analogies` - Use analogies and metaphors for complex concepts
- `--step-by-step` - Break down explanations into step-by-step guides
- `--visual` - Include visual diagrams and illustrations

### Persona Integration Flags
- `--persona-mentor` - Educational specialist for learning-focused explanations
- `--persona-scribe` - Professional writer for clear communication
- `--persona-architect` - Systems architect for technical architecture explanations

## Execution
1. Analyze target code or concept thoroughly
2. Identify key components and relationships
3. Structure explanation based on complexity level
4. Provide relevant examples and use cases
5. Present clear, accessible explanation with proper formatting

## Claude Code Integration
- Uses Read for comprehensive code analysis
- Leverages Grep for pattern identification
- Applies Bash for runtime behavior analysis
- Maintains clear, educational communication style