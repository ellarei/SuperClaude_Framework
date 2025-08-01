# FLAGS.md - SuperClaude Flag Reference

Flag system for Claude Code SuperClaude framework with auto-activation and conflict resolution.

## Flag System Architecture

**Priority Order**:
1. Explicit user flags override auto-detection
2. Safety flags override optimization flags
3. Advanced reasoning flags override standard analysis
4. Performance flags activate under resource pressure
5. Persona flags based on task patterns (enhanced by reasoning methods)
6. MCP server flags with context-sensitive activation
7. Wave flags based on complexity thresholds

## Planning & Analysis Flags

**`--plan`**
- Display execution plan before operations
- Shows tools, outputs, and step sequence

**`--think`**
- Multi-file analysis (~4K tokens)
- Enables Sequential MCP for structured problem-solving
- Auto-activates: Import chains >5 files, cross-module calls >10 references
- Auto-enables `--seq` and suggests `--persona-analyzer`

**`--think-hard`**
- Deep architectural analysis (~10K tokens)
- System-wide analysis with cross-module dependencies
- Auto-activates: System refactoring, bottlenecks >3 modules, security vulnerabilities
- Auto-enables `--seq --c7` and suggests `--persona-architect`

**`--ultrathink`**
- Critical system redesign analysis (~32K tokens)
- Maximum depth analysis for complex problems
- Auto-activates: Legacy modernization, critical vulnerabilities, performance degradation >50%
- Auto-enables `--seq --c7 --all-mcp` for comprehensive analysis

## Compression & Efficiency Flags

**`--uc` / `--ultracompressed`**
- 30-50% token reduction using symbols and structured output
- Auto-activates: Context usage >75% or large-scale operations
- Auto-generated symbol legend, maintains technical accuracy

**`--answer-only`**
- Direct response without task creation or workflow automation
- Explicit use only, no auto-activation

**`--validate`**
- Pre-operation validation and risk assessment
- Auto-activates: Risk score >0.7 or resource usage >75%
- Risk algorithm: complexity*0.3 + vulnerabilities*0.25 + resources*0.2 + failure_prob*0.15 + time*0.1

**`--safe-mode`**
- Maximum validation with conservative execution
- Auto-activates: Resource usage >85% or production environment
- Enables validation checks, forces --uc mode, blocks risky operations

**`--verbose`**
- Maximum detail and explanation
- High token usage for comprehensive output

## MCP Server Control Flags

**`--c7` / `--context7`**
- Enable Context7 for library documentation lookup
- Auto-activates: External library imports, framework questions
- Detection: import/require/from/use statements, framework keywords
- Workflow: resolve-library-id → get-library-docs → implement

**`--seq` / `--sequential`**
- Enable Sequential for complex multi-step analysis
- Auto-activates: Complex debugging, system design, --think flags
- Detection: debug/trace/analyze keywords, nested conditionals, async chains

**`--magic`**
- Enable Magic for UI component generation
- Auto-activates: UI component requests, design system queries
- Detection: component/button/form keywords, JSX patterns, accessibility requirements

**`--play` / `--playwright`**
- Enable Playwright for cross-browser automation and E2E testing
- Detection: test/e2e keywords, performance monitoring, visual testing, cross-browser requirements

**`--all-mcp`**
- Enable all MCP servers simultaneously
- Auto-activates: Problem complexity >0.8, multi-domain indicators
- Higher token usage, use judiciously

**`--no-mcp`**
- Disable all MCP servers, use native tools only
- 40-60% faster execution, WebSearch fallback

**`--no-[server]`**
- Disable specific MCP server (e.g., --no-magic, --no-seq)
- Server-specific fallback strategies, 10-30% faster per disabled server

## Sub-Agent Delegation Flags

**`--delegate [files|folders|auto]`**
- Enable Task tool sub-agent delegation for parallel processing
- **files**: Delegate individual file analysis to sub-agents
- **folders**: Delegate directory-level analysis to sub-agents  
- **auto**: Auto-detect delegation strategy based on scope and complexity
- Auto-activates: >7 directories or >50 files
- 40-70% time savings for suitable operations

**`--concurrency [n]`**
- Control max concurrent sub-agents and tasks (default: 7, range: 1-15)
- Dynamic allocation based on resources and complexity
- Prevents resource exhaustion in complex scenarios

## Wave Orchestration Flags

**`--wave-mode [auto|force|off]`**
- Control wave orchestration activation
- **auto**: Auto-activates based on complexity >0.8 AND file_count >20 AND operation_types >2
- **force**: Override auto-detection and force wave mode for borderline cases
- **off**: Disable wave mode, use Sub-Agent delegation instead
- 30-50% better results through compound intelligence and progressive enhancement

**`--wave-strategy [progressive|systematic|adaptive|enterprise]`**
- Select wave orchestration strategy
- **progressive**: Iterative enhancement for incremental improvements
- **systematic**: Comprehensive methodical analysis for complex problems
- **adaptive**: Dynamic configuration based on varying complexity
- **enterprise**: Large-scale orchestration for >100 files with >0.7 complexity
- Auto-selects based on project characteristics and operation type

**`--wave-delegation [files|folders|tasks]`**
- Control how Wave system delegates work to Sub-Agent
- **files**: Sub-Agent delegates individual file analysis across waves
- **folders**: Sub-Agent delegates directory-level analysis across waves
- **tasks**: Sub-Agent delegates by task type (security, performance, quality, architecture)
- Integrates with `--delegate` flag for coordinated multi-phase execution

## Scope & Focus Flags

**`--scope [level]`**
- file: Single file analysis
- module: Module/directory level
- project: Entire project scope
- system: System-wide analysis

**`--focus [domain]`**
- performance: Performance optimization
- security: Security analysis and hardening
- quality: Code quality and maintainability
- architecture: System design and structure
- accessibility: UI/UX accessibility compliance
- testing: Test coverage and quality

## Iterative Improvement Flags

**`--loop`**
- Enable iterative improvement mode for commands
- Auto-activates: Quality improvement requests, refinement operations, polish tasks
- Compatible commands: /improve, /refine, /enhance, /fix, /cleanup, /analyze
- Default: 3 iterations with automatic validation

**`--iterations [n]`**
- Control number of improvement cycles (default: 3, range: 1-10)
- Overrides intelligent default based on operation complexity

**`--interactive`**
- Enable user confirmation between iterations
- Pauses for review and approval before each cycle
- Allows manual guidance and course correction

## Persona Activation Flags

**Available Personas**:
- `--persona-architect`: Systems architecture specialist
- `--persona-frontend`: UX specialist, accessibility advocate
- `--persona-backend`: Reliability engineer, API specialist
- `--persona-analyzer`: Root cause specialist
- `--persona-security`: Threat modeler, vulnerability specialist
- `--persona-mentor`: Knowledge transfer specialist
- `--persona-refactorer`: Code quality specialist
- `--persona-performance`: Optimization specialist
- `--persona-qa`: Quality advocate, testing specialist
- `--persona-devops`: Infrastructure specialist
- `--persona-scribe=lang`: Professional writer, documentation specialist

## Advanced Reasoning Flags

**`--tot` / `--tree-of-thoughts`**
- Enable systematic tree search reasoning with branch generation and pruning
- Auto-activates: Design decisions, architecture choices, multiple viable approaches
- Detection: "design", "architecture", "options", "trade-offs", complexity >0.7
- Integration: Works with --think flags for deeper branch analysis
- Token cost: High (3x-5x baseline) for comprehensive exploration

**`--tot-branches [n]`**
- Number of initial branches to generate (default: 4, range: 2-8)
- Higher values for complex design spaces, lower for focused decisions

**`--tot-depth [n]`**
- Maximum tree search depth (default: 3, range: 1-5)
- Deeper searches for critical architectural decisions

**`--tot-prune-threshold [n]`**
- Score threshold for branch pruning (default: 25, range: 15-40)
- Lower thresholds = more aggressive pruning, faster execution

**`--sc` / `--self-consistency`**
- Enable multiple independent reasoning paths with consensus validation
- Auto-activates: Critical decisions, accuracy requirements >90%, validation needs
- Detection: "critical", "validate", "verify", "accuracy", high-stakes decisions
- Token cost: Medium (2x-3x baseline) for multiple reasoning paths

**`--sc-paths [n]`**
- Number of independent reasoning paths (default: 3, range: 2-5)
- More paths increase confidence but consume more tokens

**`--sc-consensus [method]`**
- Consensus method: voting, weighted, confidence-based (default: confidence-based)
- **voting**: Simple majority rule
- **weighted**: Confidence-weighted averaging
- **confidence-based**: Highest confidence path wins

**`--mad` / `--multi-agent-debate`**
- Enable adversarial reasoning with persona-based debate
- Auto-activates: Cross-functional decisions, stakeholder conflicts, trade-off analysis
- Detection: "stakeholders", "competing priorities", decisions affecting 3+ domains
- Token cost: Medium-High (2.5x-4x baseline) for multi-perspective analysis

**`--mad-agents [personas]`**
- Specific personas for debate (e.g., "architect,security,performance")
- Auto-selects relevant personas based on problem domain if not specified

**`--mad-rounds [n]`**
- Number of debate rounds (default: 3, range: 2-5)
- More rounds for complex stakeholder scenarios with deep conflicts

**`--mad-resolution [method]`**
- Resolution method: consensus, synthesis, escalation (default: synthesis)
- **consensus**: Agreement required across all agents
- **synthesis**: Integrate best elements from all perspectives
- **escalation**: Defer unresolved conflicts to user or architect persona

## Introspection & Transparency Flags

**`--introspect` / `--introspection`**
- Deep transparency mode exposing thinking process
- Auto-activates: SuperClaude framework work, complex debugging
- Transparency markers: 🤔 Thinking, 🎯 Decision, ⚡ Action, 📊 Check, 💡 Learning
- Conversational reflection with shared uncertainties

## Flag Integration Patterns

### MCP Server Auto-Activation

**Auto-Activation Logic**:
- **Context7**: External library imports, framework questions, documentation requests
- **Sequential**: Complex debugging, system design, any --think flags  
- **Magic**: UI component requests, design system queries, frontend persona
- **Playwright**: Testing workflows, performance monitoring, QA persona

### Flag Precedence

1. Safety flags (--safe-mode) > optimization flags
2. Explicit flags > auto-activation
3. Thinking depth: --ultrathink > --think-hard > --think
4. Reasoning depth: --tot + --mad + --sc > individual reasoning flags > standard analysis
5. --no-mcp overrides all individual MCP flags
6. Scope: system > project > module > file
7. Last specified persona takes precedence (unless --mad overrides for debate)
8. Wave mode: --wave-mode off > --wave-mode force > --wave-mode auto
9. Sub-Agent delegation: explicit --delegate > auto-detection
10. Loop mode: explicit --loop > auto-detection based on refinement keywords
11. --uc auto-activation overrides verbose flags (except for reasoning transparency)

### Context-Based Auto-Activation

**Advanced Reasoning Auto-Activation**:
```yaml
tree_of_thoughts:
  keywords: ["design", "architecture", "options", "approaches", "trade-offs"]
  complexity_threshold: 0.7
  solution_paths: "multiple_viable"
  confidence: 85%
  
self_consistency:
  keywords: ["critical", "validate", "verify", "accuracy", "mission-critical"]
  accuracy_requirements: ">90%"
  stakes: "high"
  confidence: 90%
  
multi_agent_debate:
  keywords: ["stakeholders", "competing", "trade-offs", "cross-functional"]
  affected_domains: ">2"
  persona_involvement: ">2"
  confidence: 80%
```

**Integration Auto-Activation**:
- **Ultra-critical decisions**: --tot + --mad + --sc (complexity >0.9, stakes = critical)
- **Architecture decisions**: --tot + --mad (design + multi-domain impact)
- **Validation requirements**: --sc + --tot (accuracy >90% + multiple approaches)

**Wave Auto-Activation**: complexity ≥0.7 AND files >20 AND operation_types >2
**Sub-Agent Auto-Activation**: >7 directories OR >50 files OR complexity >0.8
**Loop Auto-Activation**: polish, refine, enhance, improve keywords detected