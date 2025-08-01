---
allowed-tools: [Read, Bash, Glob, TodoWrite, Edit]
description: "Build, compile, and package projects with error handling and optimization"
---

# /sc:build - Project Building

## Purpose
Build, compile, and package projects with comprehensive error handling and optimization.

## Usage
```
/sc:build [target] [--type dev|prod|test] [--scope project|module|component] [--clean] [--optimize] [--plan] [--validate] [--uc] [--c7] [--magic]
```

## Arguments
- `target` - Project or specific component to build

### Core Build Flags
- `--type` - Build type (dev, prod, test)
- `--scope` - Build scope (project, module, component)
- `--clean` - Clean build artifacts before building
- `--optimize` - Enable build optimizations
- `--watch` - Enable watch mode for continuous building

### Planning & Analysis Flags
- `--plan` - Display build execution plan before operations
- `--think` - Multi-file build analysis for complex project structures
- `--think-hard` - Deep dependency analysis for monorepo builds
- `--validate` - Pre-build validation and dependency checks (auto-activates for complex builds)

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized build reporting
- `--safe-mode` - Conservative build with extensive validation
- `--verbose` - Detailed build output and progress reporting

### MCP Server Control Flags
- `--c7` / `--context7` - Enable Context7 for build framework patterns and documentation
- `--magic` - Enable Magic for UI component builds and design system integration
- `--seq` / `--sequential` - Enable Sequential for complex build orchestration
- `--all-mcp` - Enable all MCP servers for comprehensive build support
- `--no-mcp` - Native tools only for faster builds (40-60% performance improvement)

### Framework Integration Flags
- `--framework [name]` - Target specific framework (react, vue, angular, express, etc.)
- `--bundle-analysis` - Generate bundle analysis reports
- `--performance-budget` - Enforce performance budgets during build

### Persona Integration Flags
- `--persona-frontend` - Frontend specialist for UI/UX optimization
- `--persona-backend` - Backend specialist for API and service builds
- `--persona-architect` - Systems architect for complex build orchestration
- `--persona-performance` - Performance specialist for build optimization

### Sub-Agent Delegation Flags
- `--delegate [files|folders|auto]` - Enable parallel build processing
- `--concurrency [n]` - Control max concurrent build processes

## Auto-Activation Patterns

### Build Context Auto-Activation
- `--validate` - Auto-activates: Complex build configurations, monorepo structures, dependency conflicts
- `--c7` - Auto-activates: Framework-specific builds, unknown build tools detected
- `--magic` - Auto-activates: UI component builds, design system integration
- `--think` - Auto-activates: Complex project structures, build configuration conflicts

### Persona Auto-Activation
- `frontend` - Auto-activates: UI/UX builds, React/Vue/Angular projects
- `backend` - Auto-activates: API builds, server-side applications
- `architect` - Auto-activates: Complex build orchestration, multi-service builds
- `performance` - Auto-activates: Production builds, optimization requests

### Efficiency Auto-Activation
- `--uc` - Auto-activates: Large build outputs, extensive logging
- `--safe-mode` - Auto-activates: Production builds, CI/CD environments

## Execution
1. **Pre-Build Planning** - Apply --plan flag for build strategy and dependency analysis
2. **Environment Validation** - Auto-activate validation for complex configurations
3. **Framework Detection** - Auto-enable Context7 for framework-specific patterns
4. **Build Orchestration** - Execute build process with intelligent tool selection
5. **Error Monitoring** - Real-time error detection and diagnostic reporting
6. **Optimization** - Apply performance optimizations and bundle analysis
7. **Results Reporting** - Generate comprehensive build reports with metrics

## Claude Code Integration
- Uses Bash for build command execution
- Leverages Read for build configuration analysis
- Applies TodoWrite for build progress tracking
- Maintains comprehensive error handling and reporting