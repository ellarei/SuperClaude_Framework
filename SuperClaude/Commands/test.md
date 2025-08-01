---
allowed-tools: [Read, Bash, Glob, TodoWrite, Edit, Write]
description: "Execute tests, generate test reports, and maintain test coverage"
---

# /sc:test - Testing and Quality Assurance

## Purpose
Execute tests, generate comprehensive test reports, and maintain test coverage standards.

## Usage
```
/sc:test [target] [--type unit|integration|e2e|all] [--scope file|module|project|system] [--coverage] [--watch] [--plan] [--validate] [--uc] [--play] [--seq]
```

## Arguments
- `target` - Specific tests, files, or entire test suite

### Core Testing Flags
- `--type` - Test type (unit, integration, e2e, all, performance, security)
- `--scope` - Testing scope (file, module, project, system)
- `--coverage` - Generate coverage reports with thresholds
- `--watch` - Run tests in watch mode for continuous testing
- `--fix` - Automatically fix failing tests when possible
- `--parallel` - Run tests in parallel for faster execution
- `--bail` - Stop on first test failure

### Planning & Analysis Flags
- `--plan` - Display test execution plan and strategy
- `--think` - Multi-file test analysis for complex test suites
- `--validate` - Pre-test validation and environment checks

### Efficiency & Safety Flags
- `--uc` / `--ultracompressed` - Token-optimized test reporting
- `--safe-mode` - Conservative test execution with extensive validation
- `--verbose` - Detailed test output and progress reporting

### MCP Server Control Flags
- `--play` / `--playwright` - Enable Playwright for E2E and browser testing
- `--seq` / `--sequential` - Enable Sequential for complex test orchestration
- `--c7` / `--context7` - Enable Context7 for testing framework patterns
- `--all-mcp` - Enable all MCP servers for comprehensive testing support
- `--no-mcp` - Native tools only for faster test execution

### Test Quality Flags
- `--threshold [n]` - Coverage threshold percentage (default: 80)
- `--flaky-detection` - Detect and report flaky tests
- `--performance-budget` - Enforce performance budgets in tests
- `--accessibility` - Include accessibility testing

### Persona Integration Flags
- `--persona-qa` - Quality assurance specialist for comprehensive testing
- `--persona-performance` - Performance specialist for load and stress testing
- `--persona-security` - Security specialist for security testing
- `--persona-frontend` - Frontend specialist for UI/UX testing

## Execution
1. Discover and categorize available tests
2. Execute tests with appropriate configuration
3. Monitor test results and collect metrics
4. Generate comprehensive test reports
5. Provide recommendations for test improvements

## Claude Code Integration
- Uses Bash for test execution and monitoring
- Leverages Glob for test discovery
- Applies TodoWrite for test result tracking
- Maintains structured test reporting and coverage analysis