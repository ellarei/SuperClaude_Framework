---
allowed-tools: [Read, Write, Edit, MultiEdit, Bash, Glob, TodoWrite, Task]
description: "Feature and code implementation with intelligent persona activation and MCP integration"
---

# /sc:implement - Feature Implementation

## Purpose
Implement features, components, and code functionality with intelligent expert activation and comprehensive development support.

## Usage
```
/sc:implement [feature-description] [--type component|api|service|feature] [--framework react|vue|express|etc] [--scope file|module|project] [--safe] [--plan] [--validate] [--uc] [--c7] [--magic] [--seq]
```

## Arguments
- `feature-description` - Description of what to implement

### Core Implementation Flags
- `--type` - Implementation type (component, api, service, feature, module)
- `--framework` - Target framework or technology stack
- `--scope` - Implementation scope (file, module, project)
- `--safe` - Use conservative implementation approach
- `--iterative` - Enable iterative development with validation steps
- `--with-tests` - Include test implementation
- `--documentation` - Generate documentation alongside implementation

### Planning & Analysis Flags
- `--plan` - Display implementation plan before execution
- `--think` - Multi-file implementation analysis for complex features
- `--validate` - Pre-implementation validation and feasibility checks

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized implementation reporting
- `--safe-mode` - Maximum validation with conservative implementation
- `--verbose` - Detailed implementation progress and explanations

### MCP Server Control Flags
- `--c7` / `--context7` - Enable Context7 for framework patterns and best practices
- `--magic` - Enable Magic for UI component generation and design systems
- `--seq` / `--sequential` - Enable Sequential for complex implementation logic
- `--all-mcp` - Enable all MCP servers for comprehensive implementation support
- `--no-mcp` - Native tools only for faster implementation

### Persona Integration Flags
- `--persona-frontend` - Frontend specialist for UI/UX development
- `--persona-backend` - Backend specialist for API and service implementation
- `--persona-security` - Security specialist for secure implementation practices
- `--persona-architect` - Systems architect for complex feature architecture

## Execution
1. Analyze implementation requirements and detect technology context
2. Auto-activate relevant personas (frontend, backend, security, etc.)
3. Coordinate with MCP servers (Magic for UI, Context7 for patterns, Sequential for complex logic)
4. Generate implementation code with best practices
5. Apply security and quality validation
6. Provide testing recommendations and next steps

## Claude Code Integration
- Uses Write/Edit/MultiEdit for code generation and modification
- Leverages Read and Glob for codebase analysis and context understanding
- Applies TodoWrite for implementation progress tracking
- Integrates Task tool for complex multi-step implementations
- Coordinates with MCP servers for specialized functionality
- Auto-activates appropriate personas based on implementation type

## Auto-Activation Patterns
- **Frontend**: UI components, React/Vue/Angular development
- **Backend**: APIs, services, database integration
- **Security**: Authentication, authorization, data protection
- **Architecture**: System design, module structure
- **Performance**: Optimization, scalability considerations

## Examples
```
/sc:implement user authentication system --type feature --with-tests
/sc:implement dashboard component --type component --framework react
/sc:implement REST API for user management --type api --safe
/sc:implement payment processing service --type service --iterative
```