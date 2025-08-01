# SuperClaude Advanced Reasoning Usage Examples

Practical examples demonstrating SuperClaude's advanced reasoning capabilities with Tree-of-Thoughts, Self-Consistency, and Multi-Agent Debate methods.

## Quick Reference

### Method Selection Guide
- **`--tot`**: Use when exploring multiple solution approaches (design, architecture, optimization)
- **`--sc`**: Use when validation and confidence are critical (production deployments, security decisions)
- **`--mad`**: Use when stakeholder perspectives conflict (cross-team decisions, trade-offs)
- **Combined**: Use for ultra-critical decisions requiring exploration + debate + validation

---

## Tree-of-Thoughts Examples

### Architecture Design with Multiple Approaches
```bash
/sc:design microservices-api --type architecture --tot --tot-branches 5 --tot-depth 3
```
**Use Case**: Designing a new microservices API with multiple viable architectures
- **ToT explores**: Event-driven, REST-based, GraphQL, hybrid, and serverless approaches
- **Branches evaluated**: Scalability, complexity, team expertise, timeline constraints
- **Output**: Systematic comparison with trade-off analysis and recommendation

### Performance Optimization Strategy
```bash
/sc:improve @backend/services --type performance --tot --tot-branches 4 --focus performance
```
**Use Case**: Optimizing backend services with multiple optimization strategies
- **ToT explores**: Caching layers, database optimization, algorithm improvements, infrastructure scaling
- **Evaluation criteria**: Performance impact, implementation cost, maintenance overhead
- **Output**: Prioritized optimization roadmap with expected performance gains

### Component Library Design
```bash
/sc:design component-library --type component --tot --mad --persona-frontend --persona-architect
```
**Use Case**: Designing a reusable component library with multiple design approaches
- **ToT explores**: Atomic design, compound components, headless components, styled-system
- **MAD debate**: Frontend (UX) vs Architect (maintainability) perspectives
- **Output**: Balanced design that satisfies both user experience and architectural requirements

---

## Self-Consistency Examples

### Critical Security Validation
```bash
/sc:analyze @src/auth --focus security --sc --sc-paths 5 --sc-consensus confidence-based
```
**Use Case**: Validating authentication system security before production deployment
- **SC validates**: Security analysis through 5 independent reasoning paths
- **Validation aspects**: OWASP compliance, token handling, session management, input validation
- **Output**: High-confidence security assessment with uncertainty bounds

### Production Deployment Readiness
```bash
/sc:analyze @production-config --sc --sc-paths 3 --validate --persona-devops --persona-security
```
**Use Case**: Ensuring production configuration is ready for deployment
- **SC validates**: Configuration correctness through multiple verification approaches
- **Validation paths**: Infrastructure readiness, security compliance, monitoring setup
- **Output**: Deployment confidence score with specific readiness criteria

### Code Quality Assessment
```bash
/sc:improve @legacy-codebase --type quality --sc --safe --sc-consensus weighted
```
**Use Case**: Assessing code quality improvements for legacy codebase
- **SC validates**: Quality improvement recommendations through multiple assessment methods
- **Assessment paths**: Technical debt analysis, maintainability metrics, refactoring opportunities
- **Output**: Weighted consensus on improvement priorities with confidence levels

---

## Multi-Agent Debate Examples

### Cross-Team Feature Decision
```bash
/sc:design user-dashboard --mad --mad-agents frontend,backend,qa,devops --mad-rounds 3
```
**Use Case**: Designing user dashboard with competing team priorities
- **MAD participants**: Frontend (UX), Backend (performance), QA (testability), DevOps (deployability)
- **Debate topics**: Real-time updates vs caching, client-side vs server-side rendering
- **Output**: Synthesized solution addressing all team concerns

### Security vs Performance Trade-off
```bash
/sc:implement authentication-system --mad --mad-agents security,performance,backend --mad-resolution synthesis
```
**Use Case**: Implementing authentication with security and performance constraints
- **MAD participants**: Security (zero-trust), Performance (speed), Backend (maintainability)
- **Debate focus**: Token validation frequency, session storage, encryption overhead
- **Output**: Balanced implementation with acceptable trade-offs for all perspectives

### Technical Debt vs Feature Velocity
```bash
/sc:analyze @codebase --focus quality --mad --mad-agents refactorer,architect,devops --mad-rounds 2
```
**Use Case**: Balancing technical debt cleanup with feature development pressure
- **MAD participants**: Refactorer (code quality), Architect (long-term health), DevOps (delivery speed)
- **Debate focus**: Refactoring timeline, risk assessment, delivery impact
- **Output**: Strategic technical debt reduction plan with delivery considerations

---

## Combined Method Examples

### Ultra-Critical System Design
```bash
/sc:design payment-processing --type architecture --tot --mad --sc --ultrathink
```
**Use Case**: Designing payment processing system with maximum rigor
- **Sequential flow**: ToT (explore approaches) → MAD (stakeholder alignment) → SC (validation)
- **ToT explores**: Multiple payment architectures and integration patterns
- **MAD debates**: Security, performance, compliance, and UX perspectives
- **SC validates**: Final design through independent verification paths
- **Output**: Thoroughly vetted payment system design with high confidence

### Production-Critical Bug Analysis
```bash
/sc:analyze @payment-service --tot --sc --mad-agents analyzer,security,performance --think-hard
```
**Use Case**: Analyzing critical production bug affecting payment processing
- **ToT explores**: Multiple root cause hypotheses and investigation approaches
- **MAD debates**: Analyzer (systematic), Security (threat assessment), Performance (impact analysis)
- **SC validates**: Root cause findings through independent investigation paths
- **Output**: High-confidence root cause with validated fix recommendations

### Legacy System Modernization
```bash
/sc:design modernization-strategy --tot --mad --sc --wave-mode --enterprise
```
**Use Case**: Planning complete modernization of legacy monolith system
- **Wave orchestration**: Multi-phase modernization across teams and timelines
- **ToT explores**: Strangler fig, big bang rewrite, microservices extraction, API-first approaches
- **MAD debates**: Architect (design), DevOps (deployment), QA (risk), Performance (scalability)
- **SC validates**: Modernization strategy through multiple assessment frameworks
- **Output**: Comprehensive modernization roadmap with stakeholder buy-in

---

## Advanced Flag Combinations

### High-Confidence Design Decisions
```bash
/sc:design api-gateway --tot --sc --mad --persona-architect --persona-security --c7 --validate
```
**Features**:
- `--tot`: Explores multiple API gateway approaches
- `--sc`: Validates design through independent reasoning
- `--mad`: Debates security vs performance trade-offs
- `--c7`: Researches industry best practices
- `--validate`: Pre-execution risk assessment

### Iterative Quality Improvement
```bash
/sc:improve @frontend --tot --loop --iterations 3 --interactive --mad-agents frontend,qa,performance
```
**Features**:
- `--tot`: Explores improvement approaches systematically
- `--loop`: Iterative improvement cycles
- `--interactive`: User approval between cycles
- `--mad`: Multi-perspective quality assessment

### Enterprise-Scale Analysis
```bash
/sc:analyze @monorepo --tot --mad --sc --wave-mode enterprise --delegate auto --all-mcp
```
**Features**:
- `--tot`: Systematic analysis exploration
- `--mad`: Multi-team perspective integration
- `--sc`: High-confidence validation
- `--wave-mode enterprise`: Large-scale orchestration
- `--delegate auto`: Intelligent sub-agent coordination
- `--all-mcp`: Full server integration for comprehensive analysis

---

## Domain-Specific Examples

### Frontend Development
```bash
# Component design with UX focus
/sc:design checkout-flow --type component --tot --mad-agents frontend,qa,backend --magic

# Performance optimization
/sc:improve @components --type performance --sc --persona-performance --play

# Accessibility validation
/sc:analyze @ui-components --focus accessibility --sc --sc-paths 3 --persona-frontend
```

### Backend Development
```bash
# API design with multiple approaches
/sc:design user-api --type api --tot --tot-branches 4 --persona-backend --c7

# Database schema optimization
/sc:improve @database --type performance --mad-agents backend,architect,performance --seq

# Security hardening
/sc:analyze @api-endpoints --focus security --sc --persona-security --validate
```

### DevOps & Infrastructure
```bash
# Deployment strategy design
/sc:design ci-cd-pipeline --tot --mad-agents devops,security,qa --persona-devops

# Infrastructure scaling analysis
/sc:analyze @infrastructure --focus performance --tot --persona-devops --persona-performance

# Monitoring system design
/sc:design observability --mad --mad-agents devops,backend,qa --c7 --seq
```

### Quality Assurance
```bash
# Test strategy development
/sc:design test-automation --tot --persona-qa --play --mad-agents qa,frontend,backend

# Risk assessment
/sc:analyze @critical-path --focus quality --sc --persona-qa --validate --safe-mode

# Performance testing strategy
/sc:design load-testing --mad-agents qa,performance,devops --play --seq
```

---

## Performance Optimization Tips

### Token Budget Management
```bash
# Light reasoning for quick decisions
/sc:analyze @component --sc --sc-paths 2

# Moderate reasoning for balanced analysis
/sc:design feature --tot --tot-branches 3 --mad-rounds 2

# Full reasoning for critical decisions
/sc:design system --tot --mad --sc --ultrathink
```

### Time-Constrained Scenarios
```bash
# Parallel validation for speed
/sc:improve @code --tot --sc  # Runs ToT and SC in parallel

# Progressive reasoning depth
/sc:analyze @system --think    # Start with standard analysis
/sc:analyze @system --tot      # Escalate to ToT if needed
/sc:analyze @system --tot --sc # Add validation if critical
```

### Resource-Efficient Combinations
```bash
# Efficient multi-perspective analysis
/sc:design feature --mad --mad-agents frontend,backend --mad-rounds 2

# Focused validation
/sc:analyze @security --sc --sc-paths 2 --focus security

# Smart auto-activation
/sc:improve @codebase  # Let SuperClaude choose optimal reasoning method
```

---

## Common Patterns

### Decision Making Framework
1. **Exploration**: Use `--tot` to systematically explore options
2. **Alignment**: Use `--mad` to integrate stakeholder perspectives
3. **Validation**: Use `--sc` to build confidence in the decision
4. **Documentation**: Results include reasoning transparency

### Quality Assurance Workflow
1. **Analysis**: `--sc` for high-confidence quality assessment
2. **Planning**: `--tot` for improvement approach exploration
3. **Implementation**: Standard execution with validation
4. **Review**: `--mad` for multi-perspective validation

### Architecture Design Process
1. **Research**: `--c7` for industry patterns and best practices
2. **Exploration**: `--tot` for systematic architecture evaluation
3. **Stakeholder Review**: `--mad` for cross-functional alignment
4. **Validation**: `--sc` for design confidence building

---

## Best Practices

### When to Use Advanced Reasoning
- **Always use** for production-critical decisions
- **Consider using** for cross-team coordination
- **Evaluate using** for complex technical trade-offs
- **Skip for** simple, low-risk operations

### Method Selection Guidelines
- **Single method**: Clear problem domain with straightforward requirements
- **Two methods**: Moderate complexity with validation needs
- **Three methods**: Ultra-critical decisions affecting multiple stakeholders

### Flag Combination Patterns
- `--tot + --sc`: Design exploration with validation
- `--mad + --sc`: Stakeholder alignment with confidence building
- `--tot + --mad`: Systematic exploration with perspective integration
- `--tot + --mad + --sc`: Complete advanced reasoning workflow

### Performance Considerations
- Start with auto-activation (no explicit flags)
- Add specific methods based on problem complexity
- Use `--uc` flag if token budget is constrained
- Monitor reasoning effectiveness and adjust accordingly

---

## Emergency Response Scenarios

### Production Outage Investigation
```bash
/sc:analyze @production-logs --focus performance --sc --sc-paths 3 --mad-agents devops,backend,security --urgent
```
**Use Case**: Critical production system down, need rapid root cause identification
- **SC validates**: Root cause analysis through multiple investigation approaches
- **MAD coordinates**: DevOps (infrastructure), Backend (application), Security (breach assessment)
- **Output**: High-confidence root cause with validated recovery steps
- **Timeline**: Minutes to hours for business-critical systems

### Security Breach Response
```bash
/sc:analyze @security-logs --focus security --tot --mad-agents security,devops,legal --validate --safe-mode
```
**Use Case**: Suspected security breach requiring immediate containment
- **ToT explores**: Multiple containment strategies (isolate, monitor, patch, rollback)
- **MAD coordinates**: Security (technical response), DevOps (system isolation), Legal (compliance)
- **Output**: Comprehensive breach response plan with legal compliance
- **Critical**: Evidence preservation and regulatory notification requirements

### Data Corruption Recovery
```bash
/sc:design recovery-strategy --tot --sc --mad-agents backend,devops,qa --persona-security --ultrathink
```
**Use Case**: Critical data corruption detected, multiple recovery options available
- **ToT explores**: Backup restoration, transaction log replay, partial recovery, rebuild strategies
- **SC validates**: Data integrity verification through multiple validation methods
- **MAD coordinates**: Risk assessment across technical and business perspectives
- **Output**: Recovery plan with data loss minimization and integrity guarantees

### Critical Bug Hotfix Validation
```bash
/sc:analyze @hotfix-branch --sc --sc-paths 5 --mad-agents qa,backend,devops --validate --safe-mode
```
**Use Case**: Critical bug fix needs immediate deployment with high confidence
- **SC validates**: Fix effectiveness through multiple testing and analysis approaches
- **MAD assesses**: QA (testing completeness), Backend (code correctness), DevOps (deployment risk)
- **Output**: Deployment confidence score with rollback plan
- **Goal**: Zero-regression hotfix deployment

---

## Business and Strategic Decision Support

### Technology Stack Selection
```bash
/sc:design tech-stack --type architecture --tot --mad-agents architect,frontend,backend,devops --c7 --estimate
```
**Use Case**: Choosing between React vs Vue vs Angular for new product development
- **ToT explores**: Framework capabilities, ecosystem, learning curve, long-term support
- **MAD debates**: Architect (maintainability), Frontend (developer experience), Backend (integration), DevOps (deployment)
- **C7 research**: Industry trends, community support, enterprise adoption patterns
- **Output**: Strategic technology decision with 5-year outlook and migration considerations

### Build vs Buy Decision Analysis
```bash
/sc:estimate custom-solution --tot --mad-agents architect,manager,devops --focus cost --c7
```
**Use Case**: Deciding whether to build custom authentication system or use Auth0/Okta
- **ToT explores**: Development cost, maintenance overhead, feature gaps, time-to-market
- **MAD perspectives**: Architect (technical debt), Manager (resource allocation), DevOps (operational complexity)
- **Output**: Cost-benefit analysis with risk assessment and timeline projections

### Vendor Evaluation and Selection
```bash
/sc:analyze @vendor-proposals --tot --mad-agents procurement,security,architect --sc --validate
```
**Use Case**: Selecting cloud infrastructure vendor (AWS vs Azure vs GCP)
- **ToT explores**: Pricing models, service capabilities, migration complexity, vendor lock-in
- **MAD evaluation**: Procurement (cost), Security (compliance), Architect (technical fit)
- **SC validates**: Vendor scoring through multiple evaluation frameworks
- **Output**: Vendor recommendation with contract negotiation points

### Resource Allocation and Team Sizing
```bash
/sc:estimate team-structure --tot --mad-agents architect,manager,devops --focus quality
```
**Use Case**: Determining optimal team size and skill mix for new product development
- **ToT explores**: Team topologies, skill distribution, communication overhead, delivery velocity
- **MAD balances**: Architect (technical leadership), Manager (budget constraints), DevOps (deployment capability)
- **Output**: Team structure recommendation with hiring plan and timeline

---

## Compliance and Regulatory Scenarios

### GDPR Compliance Assessment
```bash
/sc:analyze @data-processing --focus security --sc --mad-agents security,legal,backend --validate --c7
```
**Use Case**: Ensuring user data processing complies with GDPR requirements
- **SC validates**: Data processing legality through multiple compliance frameworks
- **MAD coordinates**: Security (technical controls), Legal (regulatory requirements), Backend (implementation)
- **C7 research**: GDPR best practices, enforcement patterns, technical solutions
- **Output**: Compliance gap analysis with remediation roadmap

### SOC 2 Audit Preparation
```bash
/sc:design audit-controls --tot --mad-agents security,devops,qa --sc --validate --c7
```
**Use Case**: Implementing security controls for SOC 2 Type II certification
- **ToT explores**: Control implementation approaches, automation strategies, evidence collection
- **MAD coordinates**: Security (control design), DevOps (implementation), QA (testing)
- **SC validates**: Control effectiveness through multiple assessment methods
- **Output**: SOC 2 readiness plan with control implementation timeline

### HIPAA Compliance for Healthcare Systems
```bash
/sc:design patient-data-system --focus security --tot --mad-agents security,legal,healthcare --ultrathink
```
**Use Case**: Designing patient data management system with HIPAA compliance
- **ToT explores**: Encryption strategies, access controls, audit logging, data minimization
- **MAD coordinates**: Security (technical safeguards), Legal (regulatory requirements), Healthcare (clinical workflows)
- **Output**: HIPAA-compliant architecture with privacy impact assessment

### PCI DSS Compliance for Payment Processing
```bash
/sc:analyze @payment-system --focus security --sc --mad-agents security,backend,compliance --validate
```
**Use Case**: Validating payment processing system for PCI DSS compliance
- **SC validates**: Security controls through multiple assessment frameworks
- **MAD coordinates**: Security (technical requirements), Backend (implementation), Compliance (audit readiness)
- **Output**: PCI DSS compliance status with remediation priorities

---

## Team Coordination and Process Design

### Code Review Standards Establishment
```bash
/sc:design review-process --mad-agents qa,architect,mentor --sc --c7
```
**Use Case**: Establishing consistent code review standards across multiple development teams
- **MAD coordinates**: QA (quality gates), Architect (design standards), Mentor (knowledge transfer)
- **C7 research**: Industry best practices, tool comparisons, effectiveness metrics
- **SC validates**: Review criteria effectiveness through multiple quality frameworks
- **Output**: Standardized review process with team-specific adaptations

### Remote Team Workflow Optimization
```bash
/sc:improve @team-processes --tot --mad-agents manager,devops,qa --focus quality
```
**Use Case**: Optimizing development workflow for distributed remote teams
- **ToT explores**: Async vs sync collaboration, communication tools, delivery pipelines
- **MAD balances**: Manager (productivity), DevOps (automation), QA (quality assurance)
- **Output**: Remote workflow optimization with productivity metrics and communication protocols

### Technical Interview Process Design
```bash
/sc:design interview-process --tot --mad-agents mentor,architect,manager --c7
```
**Use Case**: Creating fair and effective technical interview process
- **ToT explores**: Assessment methods, bias reduction, skill evaluation approaches
- **MAD coordinates**: Mentor (candidate experience), Architect (technical depth), Manager (hiring goals)
- **C7 research**: Interview best practices, bias research, assessment validity
- **Output**: Structured interview process with standardized evaluation criteria

---

## Migration and Transformation Projects

### Cloud Migration Strategy
```bash
/sc:design cloud-migration --type architecture --tot --mad-agents devops,security,architect --estimate --c7
```
**Use Case**: Migrating on-premises infrastructure to AWS/Azure/GCP
- **ToT explores**: Lift-and-shift vs re-architecture, multi-cloud vs single-cloud, migration phases
- **MAD coordinates**: DevOps (operational complexity), Security (compliance), Architect (technical debt)
- **C7 research**: Migration patterns, cost optimization, security frameworks
- **Output**: Cloud migration roadmap with cost projections and risk mitigation

### Monolith to Microservices Decomposition
```bash
/sc:design microservices-strategy --tot --mad-agents architect,backend,devops --wave-mode --ultrathink
```
**Use Case**: Decomposing legacy monolith into microservices architecture
- **ToT explores**: Service boundaries, data decomposition, communication patterns, deployment strategies
- **MAD coordinates**: Architect (design principles), Backend (implementation complexity), DevOps (operational overhead)
- **Wave mode**: Multi-phase transformation with validation checkpoints
- **Output**: Microservices transformation strategy with service design and migration timeline

### Database Migration Planning
```bash
/sc:design db-migration --tot --sc --mad-agents backend,architect,qa --validate --estimate
```
**Use Case**: Migrating from SQL Server to PostgreSQL with zero downtime
- **ToT explores**: Migration approaches (blue-green, rolling, dual-write), schema transformation, data validation
- **SC validates**: Data integrity through multiple verification methods
- **MAD coordinates**: Backend (application changes), Architect (schema design), QA (validation testing)
- **Output**: Zero-downtime migration plan with rollback procedures

### Legacy System Modernization
```bash
/sc:design modernization --tot --mad --sc --wave-mode enterprise --all-mcp
```
**Use Case**: Modernizing 15-year-old COBOL system to modern web architecture
- **ToT explores**: Strangler fig pattern, big bang rewrite, API-first transformation, gradual migration
- **MAD coordinates**: Multiple stakeholder perspectives across business and technical domains
- **SC validates**: Modernization approach through multiple risk assessment frameworks
- **Wave orchestration**: Enterprise-scale transformation with parallel workstreams
- **Output**: Comprehensive modernization strategy with business continuity plan

---

## Innovation and Research Scenarios

### AI/ML Model Selection and Integration
```bash
/sc:design ai-integration --tot --mad-agents ai-specialist,backend,performance,ethics --c7 --validate
```
**Use Case**: Selecting and integrating AI models for customer service chatbot
- **ToT explores**: GPT-4 vs Claude vs Llama vs custom training, API vs self-hosted, fine-tuning strategies
- **MAD coordinates**: AI-specialist (capabilities), Backend (integration), Performance (latency), Ethics (bias/safety)
- **C7 research**: Model benchmarks, integration patterns, cost analysis
- **Output**: AI integration strategy with performance benchmarks and ethical guidelines

### Proof of Concept Evaluation
```bash
/sc:estimate poc-feasibility --tot --mad-agents architect,business,performance --sc --validate
```
**Use Case**: Evaluating blockchain integration for supply chain traceability
- **ToT explores**: Technical feasibility, implementation approaches, scalability considerations
- **MAD coordinates**: Architect (technical complexity), Business (value proposition), Performance (scalability)
- **SC validates**: Feasibility assessment through multiple evaluation frameworks
- **Output**: Go/no-go recommendation with implementation roadmap and success criteria

### Performance Benchmarking Strategy
```bash
/sc:design benchmark-suite --tot --sc --mad-agents performance,qa,devops --play
```
**Use Case**: Creating comprehensive performance benchmarking for e-commerce platform
- **ToT explores**: Benchmarking methodologies, load patterns, measurement tools, baseline establishment
- **SC validates**: Benchmark validity through multiple measurement approaches
- **MAD coordinates**: Performance (metrics), QA (test design), DevOps (infrastructure)
- **Playwright integration**: Automated performance testing and monitoring
- **Output**: Benchmarking framework with automated performance regression detection

---

## Cost and Resource Optimization

### Infrastructure Cost Analysis
```bash
/sc:analyze @infrastructure-costs --tot --mad-agents devops,architect,finance --estimate --focus cost
```
**Use Case**: Reducing cloud infrastructure costs by 40% without impacting performance
- **ToT explores**: Right-sizing, reserved instances, spot instances, architectural optimization
- **MAD coordinates**: DevOps (operational impact), Architect (technical constraints), Finance (cost targets)
- **Output**: Cost optimization roadmap with risk assessment and savings projections

### Development Tool Consolidation
```bash
/sc:improve @development-tools --tot --mad-agents devops,developer,manager --estimate
```
**Use Case**: Consolidating 15+ development tools into integrated development platform
- **ToT explores**: Tool integration strategies, migration complexity, feature gap analysis
- **MAD coordinates**: DevOps (operational efficiency), Developer (productivity impact), Manager (cost savings)
- **Output**: Tool consolidation plan with productivity impact assessment and change management

### License Optimization Analysis
```bash
/sc:analyze @software-licenses --sc --mad-agents legal,finance,architect --validate --estimate
```
**Use Case**: Optimizing enterprise software licenses to reduce annual costs by $500K
- **SC validates**: Usage analysis through multiple measurement methods
- **MAD coordinates**: Legal (compliance requirements), Finance (cost targets), Architect (technical dependencies)
- **Output**: License optimization strategy with compliance risk assessment

---

## Educational and Knowledge Transfer

### Technical Training Program Design
```bash
/sc:design training-curriculum --tot --mad-agents mentor,manager,architect --c7
```
**Use Case**: Creating comprehensive onboarding program for junior developers
- **ToT explores**: Curriculum structure, hands-on vs theoretical, mentorship integration, assessment methods
- **MAD coordinates**: Mentor (learning effectiveness), Manager (time investment), Architect (technical depth)
- **C7 research**: Training best practices, adult learning principles, skill development frameworks
- **Output**: Structured training program with progress tracking and effectiveness metrics

### Knowledge Documentation Strategy
```bash
/sc:design documentation-system --tot --mad-agents scribe,architect,mentor --c7
```
**Use Case**: Creating comprehensive technical documentation system for complex product
- **ToT explores**: Documentation approaches, tool selection, maintenance strategies, user experience
- **MAD coordinates**: Scribe (writing quality), Architect (technical accuracy), Mentor (learning value)
- **Output**: Documentation strategy with authoring guidelines and maintenance processes

### Code Style Guide Establishment
```bash
/sc:design style-guide --mad-agents refactorer,frontend,backend --sc --c7
```
**Use Case**: Establishing consistent code style across multiple programming languages and teams
- **MAD coordinates**: Refactorer (maintainability), Frontend (specific needs), Backend (performance impact)
- **SC validates**: Style guide effectiveness through multiple quality metrics
- **C7 research**: Industry standards, tool integration, enforcement patterns
- **Output**: Comprehensive style guide with automated enforcement and team adoption plan

---

## Specialized Technical Domains

### Real-time System Design
```bash
/sc:design realtime-trading --type architecture --tot --mad-agents performance,architect,finance --ultrathink
```
**Use Case**: Designing ultra-low latency trading system with <1ms response time
- **ToT explores**: Hardware optimization, algorithm selection, network topology, data structures
- **MAD coordinates**: Performance (latency requirements), Architect (system design), Finance (business requirements)
- **Ultra-high reliability and performance requirements**
- **Output**: Real-time architecture with latency budgets and performance guarantees

### Distributed System Consensus
```bash
/sc:design consensus-algorithm --tot --sc --mad-agents architect,backend,performance --c7
```
**Use Case**: Selecting consensus algorithm for distributed blockchain network
- **ToT explores**: Raft vs PBFT vs PoS vs custom protocols, performance characteristics, fault tolerance
- **SC validates**: Correctness proofs through multiple verification approaches
- **MAD coordinates**: Architect (correctness), Backend (implementation), Performance (throughput)
- **C7 research**: Consensus algorithm comparisons, implementation patterns, security analysis
- **Output**: Consensus protocol selection with formal verification and performance analysis

### Data Pipeline Architecture
```bash
/sc:design data-pipeline --tot --mad-agents data-engineer,backend,devops --estimate --c7
```
**Use Case**: Processing 100TB daily data with real-time analytics and batch processing
- **ToT explores**: Lambda vs Kappa architecture, stream processing frameworks, storage optimization
- **MAD coordinates**: Data-engineer (processing logic), Backend (integration), DevOps (operational complexity)
- **Output**: Scalable data pipeline architecture with cost optimization and monitoring

---

## Cross-Industry Applications

### Healthcare System Integration
```bash
/sc:design hl7-integration --tot --mad-agents healthcare,security,architect --c7 --validate
```
**Use Case**: Integrating electronic health records with HIPAA compliance and interoperability
- **ToT explores**: HL7 FHIR implementation, integration patterns, data mapping strategies
- **MAD coordinates**: Healthcare (clinical workflows), Security (privacy compliance), Architect (technical integration)
- **C7 research**: Healthcare interoperability standards, HIPAA technical safeguards
- **Output**: Healthcare integration architecture with compliance validation

### Financial System Design
```bash
/sc:design payment-processor --type architecture --tot --mad --sc --ultrathink --validate
```
**Use Case**: Designing payment processing system with PCI DSS compliance and 99.999% uptime
- **ToT explores**: Payment flow architectures, fraud detection integration, regulatory compliance
- **MAD coordinates**: Security (PCI requirements), Backend (reliability), Legal (regulatory compliance)
- **SC validates**: System design through multiple reliability and security frameworks
- **Ultra-critical**: Financial transaction integrity and regulatory compliance
- **Output**: Payment system architecture with formal reliability guarantees

### Manufacturing IoT Platform
```bash
/sc:design iot-platform --tot --mad-agents architect,performance,security --estimate --c7
```
**Use Case**: Designing IoT platform for smart manufacturing with predictive maintenance
- **ToT explores**: Edge computing vs cloud processing, communication protocols, data analytics
- **MAD coordinates**: Architect (system design), Performance (real-time requirements), Security (device security)
- **C7 research**: IoT platforms, industrial protocols, edge computing patterns
- **Output**: IoT architecture with scalability and security for industrial environments

---

## Edge Cases and Unique Scenarios

### Post-Mortem Analysis
```bash
/sc:analyze @incident-data --sc --mad-agents devops,qa,manager --persona-analyzer --c7
```
**Use Case**: Comprehensive analysis of major production incident for learning and prevention
- **SC validates**: Root cause analysis through multiple investigation methodologies
- **MAD coordinates**: DevOps (technical causes), QA (process failures), Manager (organizational factors)
- **Persona-analyzer**: Systematic investigation and evidence-based conclusions
- **Output**: Comprehensive post-mortem with actionable prevention measures

### Technical Debt Bankruptcy Decision
```bash
/sc:estimate rewrite-vs-refactor --tot --mad-agents architect,manager,devops --estimate --ultrathink
```
**Use Case**: Deciding whether to rewrite legacy system or continue incremental improvements
- **ToT explores**: Complete rewrite, gradual refactoring, hybrid approaches, parallel development
- **MAD coordinates**: Architect (technical debt), Manager (business continuity), DevOps (deployment risk)
- **Ultra-critical business decision with long-term implications**
- **Output**: Strategic recommendation with detailed cost-benefit analysis and risk assessment

### Open Source vs Proprietary Strategy
```bash
/sc:design licensing-strategy --tot --mad-agents legal,architect,business --c7 --validate
```
**Use Case**: Deciding whether to open-source core product components or maintain proprietary approach
- **ToT explores**: Licensing models, community building, competitive advantage, development models
- **MAD coordinates**: Legal (intellectual property), Architect (technical strategy), Business (competitive position)
- **C7 research**: Open source business models, licensing implications, community management
- **Output**: Licensing strategy with competitive analysis and legal risk assessment

### Disaster Recovery Planning
```bash
/sc:design disaster-recovery --tot --sc --mad-agents devops,security,business --validate --ultrathink
```
**Use Case**: Creating comprehensive disaster recovery plan for mission-critical systems
- **ToT explores**: Recovery strategies, backup approaches, failover mechanisms, testing procedures
- **SC validates**: Recovery time and point objectives through multiple scenario analyses
- **MAD coordinates**: DevOps (technical implementation), Security (data protection), Business (continuity requirements)
- **Output**: Disaster recovery plan with tested procedures and recovery guarantees

### API Versioning and Deprecation Strategy
```bash
/sc:design api-versioning --tot --mad-agents backend,frontend,qa --c7 --estimate
```
**Use Case**: Evolving public API while maintaining backward compatibility for 10,000+ integrations
- **ToT explores**: Versioning strategies, deprecation timelines, migration tools, backward compatibility
- **MAD coordinates**: Backend (implementation complexity), Frontend (client impact), QA (testing strategy)
- **C7 research**: API versioning best practices, deprecation patterns, migration strategies
- **Output**: API evolution strategy with migration timeline and developer communication plan