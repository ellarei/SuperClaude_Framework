---
allowed-tools: [Read, Grep, Glob, Write, Edit, TodoWrite]
description: "Design system architecture, APIs, and component interfaces"
---

# /sc:design - System and Component Design

## Purpose
Design system architecture, APIs, component interfaces, and technical specifications.

## Usage
```
/sc:design [target] [--type architecture|api|component|database] [--scope file|module|project|system] [--format diagram|spec|code] [--tot] [--mad] [--sc] [--plan] [--validate] [--uc] [--c7] [--magic]
```

## Arguments
- `target` - System, component, or feature to design

### Core Design Flags
- `--type` - Design type (architecture, api, component, database, ui, service)
- `--scope` - Design scope (file, module, project, system)
- `--format` - Output format (diagram, spec, code, documentation)
- `--iterative` - Enable iterative design refinement
- `--methodology` - Design methodology (ddd, clean-architecture, microservices)

### Planning & Analysis Flags
- `--plan` - Display design plan and approach before execution
- `--think` - Multi-file design analysis for complex systems
- `--think-hard` - Deep architectural design analysis
- `--ultrathink` - Critical system design for enterprise-scale architectures
- `--validate` - Pre-design validation and feasibility assessment

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized design documentation
- `--safe-mode` - Conservative design with extensive validation
- `--verbose` - Detailed design rationale and explanations

### MCP Server Control Flags
- `--c7` / `--context7` - Enable Context7 for design patterns and architectural documentation
- `--magic` - Enable Magic for UI/UX design and component architecture
- `--seq` / `--sequential` - Enable Sequential for complex design orchestration
- `--all-mcp` - Enable all MCP servers for comprehensive design support
- `--no-mcp` - Native tools only for faster design generation

### Advanced Reasoning Flags
- `--tot` / `--tree-of-thoughts` - Explore multiple design approaches systematically
- `--tot-branches [n]` - Number of design branches (default: 4, range: 2-8)
- `--tot-depth [n]` - Design exploration depth (default: 3, range: 1-5)
- `--mad` / `--multi-agent-debate` - Stakeholder-driven design decisions through expert debate
- `--mad-agents [personas]` - Specific personas for design debate (e.g., "architect,frontend,security")
- `--mad-rounds [n]` - Number of design debate rounds (default: 3, range: 2-5)
- `--sc` / `--self-consistency` - Validate design choices through multiple reasoning paths
- `--sc-paths [n]` - Number of validation paths (default: 3, range: 2-5)

### Persona Integration Flags
- `--persona-architect` - Systems architecture specialist for structural design
- `--persona-frontend` - UI/UX specialist for interface design
- `--persona-backend` - API and service design specialist
- `--persona-security` - Security architect for secure design patterns
- `--persona-performance` - Performance specialist for scalable design

## Execution
1. Analyze requirements and design constraints
2. Apply advanced reasoning method selection based on design complexity
3. Create initial design concepts and alternatives using systematic exploration
4. Develop detailed design specifications with multi-perspective validation
5. Validate design against requirements and best practices
6. Generate design documentation and implementation guides with reasoning rationale

## Advanced Reasoning Integration
- **ToT Mode**: Systematically explores multiple design alternatives, evaluates trade-offs between approaches
- **MAD Mode**: Debates design decisions from architect, frontend, backend, security, and performance perspectives
- **SC Mode**: Validates design choices through multiple independent reasoning paths
- **Sequential Integration**: ToT → MAD → SC for comprehensive design exploration, stakeholder alignment, and validation

## Claude Code Integration
- Uses Read for requirement analysis
- Leverages Write for design documentation
- Applies TodoWrite for design task tracking
- Maintains consistency with architectural patterns