# REASONING.md - SuperClaude Advanced Reasoning Reference

Comprehensive reference for advanced reasoning methods in Claude Code SuperClaude framework.

## Overview

Advanced reasoning framework providing three core methods for complex problem-solving:

1. **Tree-of-Thoughts (ToT)**: Systematic exploration of solution spaces
2. **Self-Consistency (SC)**: Multiple validation paths with consensus building
3. **Multi-Agent Debate (MAD)**: Adversarial reasoning with synthesis

**Core Philosophy**: "Systematic exploration | Multiple perspectives | Evidence-based synthesis"

## Method Selection Framework

### Decision Matrix

**Selection Criteria**:
- **Problem Complexity**: Simple (0.0-0.4) → Moderate (0.4-0.7) → Complex (0.7-1.0)
- **Solution Space**: Single path → Multiple paths → Exploration required
- **Validation Needs**: Basic → High confidence → Critical accuracy
- **Stakeholder Count**: Individual → Team → Cross-functional
- **Time Constraints**: Immediate → Balanced → Deep analysis
- **Token Budget**: Limited → Moderate → Extensive

### Method Suitability Matrix

| Problem Type | Primary Method | Secondary | Integration Pattern |
|--------------|----------------|-----------|---------------------|
| Architecture design | ToT | MAD | ToT → MAD → SC |
| Critical bug analysis | SC | ToT | SC + ToT validation |
| Cross-team decisions | MAD | SC | MAD → SC consensus |
| Security analysis | ToT | MAD | ToT → MAD → SC |
| Performance optimization | SC | ToT | SC + metrics validation |
| Feature implementation | ToT | SC | ToT → implementation → SC |
| Emergency decisions | SC | - | SC rapid validation |
| Research questions | ToT | MAD | ToT → MAD synthesis |

## Tree-of-Thoughts (ToT) Method

### Purpose
Systematic exploration of solution spaces through structured tree search with branch generation, evaluation, and pruning.

### Core Process
```yaml
1_generate_branches:
  - Create diverse solution approaches
  - Generate 2-8 initial branches based on complexity
  - Ensure branch diversity through different angles

2_evaluate_branches:
  - Score each branch on: feasibility, impact, complexity, risk
  - Use 0-100 scoring with detailed rationale
  - Consider resource requirements and constraints

3_prune_branches:
  - Remove branches below threshold (default: 25/100)
  - Maintain minimum 2 branches for comparison
  - Document pruning rationale

4_explore_selected:
  - Develop promising branches in depth
  - Generate sub-branches for complex solutions
  - Maximum depth: 3-5 levels based on criticality

5_synthesize_solution:
  - Compare final branches with evidence
  - Select optimal solution or hybrid approach
  - Document decision rationale and trade-offs
```

### Implementation Templates

#### Basic ToT Template
```yaml
tot_session:
  problem: "[Clear problem statement]"
  branches: 4
  depth: 3
  prune_threshold: 25
  
  branch_evaluation_criteria:
    - feasibility (weight: 30%)
    - impact (weight: 25%)
    - complexity (weight: 20%)
    - risk (weight: 15%)
    - resources (weight: 10%)
  
  branch_1:
    approach: "[Approach description]"
    feasibility_score: 0-100
    impact_score: 0-100
    complexity_score: 0-100
    risk_score: 0-100
    resource_score: 0-100
    total_score: calculated
    rationale: "[Why this approach]"
  
  # Repeat for other branches
  
  selected_branches: [list]
  final_recommendation: "[Chosen solution]"
  rationale: "[Why this solution]"
```

#### Advanced ToT with Sub-Branches
```yaml
tot_advanced:
  problem: "[Complex problem statement]"
  
  branch_1:
    approach: "[Primary approach]"
    score: 85
    
    sub_branch_1_1:
      refinement: "[Specific implementation]"
      score: 78
      details: "[Implementation details]"
    
    sub_branch_1_2:
      refinement: "[Alternative implementation]"
      score: 82
      details: "[Implementation details]"
  
  synthesis:
    chosen_path: "branch_1 → sub_branch_1_2"
    rationale: "[Evidence-based selection]"
    implementation_plan: "[Step-by-step plan]"
```

### Integration Patterns

**ToT + Persona Integration**:
- **Architect Persona**: Branch evaluation considers long-term maintainability
- **Security Persona**: Additional security-focused branches and evaluation criteria
- **Performance Persona**: Performance-optimized branches with benchmarking
- **Frontend Persona**: User experience branches with accessibility considerations

**ToT + MCP Server Integration**:
- **Context7**: Research patterns and best practices for each branch
- **Sequential**: Structured analysis of complex branch implications
- **Magic**: UI component alternatives for frontend branches
- **Playwright**: Performance testing for optimization branches

## Self-Consistency (SC) Method

### Purpose
Validate reasoning through multiple independent paths, building confidence through consensus and identifying uncertainty through disagreement.

### Core Process
```yaml
1_generate_paths:
  - Create 2-5 independent reasoning paths
  - Use different approaches and starting points
  - Avoid cross-contamination between paths

2_execute_reasoning:
  - Follow each path to completion independently
  - Document assumptions and reasoning steps
  - Generate concrete conclusions for each path

3_analyze_consistency:
  - Compare path conclusions and confidence levels
  - Identify areas of agreement and disagreement
  - Calculate consensus strength and uncertainty bounds

4_synthesize_consensus:
  - Apply consensus method (voting, weighted, confidence-based)
  - Resolve minor disagreements through evidence
  - Flag major disagreements for further investigation

5_validate_result:
  - Test consensus against original requirements
  - Assess confidence level and uncertainty bounds
  - Generate actionable recommendations with risk assessment
```

### Implementation Templates

#### Basic SC Template
```yaml
sc_session:
  problem: "[Problem statement]"
  paths: 3
  consensus_method: "confidence-based"
  
  path_1:
    approach: "[Reasoning approach]"
    assumptions: "[Key assumptions]"
    steps:
      - step_1: "[Reasoning step]"
      - step_2: "[Reasoning step]"
      - step_3: "[Reasoning step]"
    conclusion: "[Final conclusion]"
    confidence: 0-100
    
  path_2:
    approach: "[Different approach]"
    assumptions: "[Key assumptions]"
    steps:
      - step_1: "[Reasoning step]"
      - step_2: "[Reasoning step]"
      - step_3: "[Reasoning step]"
    conclusion: "[Final conclusion]"
    confidence: 0-100
  
  # Repeat for additional paths
  
  consensus_analysis:
    agreement_areas: "[Where paths agree]"
    disagreement_areas: "[Where paths disagree]"
    consensus_strength: 0-100
    
  final_synthesis:
    conclusion: "[Consensus conclusion]"
    confidence: 0-100
    uncertainty_bounds: "[Areas of uncertainty]"
    recommendations: "[Actionable next steps]"
```

#### Critical Decision SC Template
```yaml
sc_critical:
  problem: "[High-stakes problem]"
  paths: 5
  consensus_method: "weighted"
  
  validation_criteria:
    - accuracy_requirement: ">95%"
    - risk_tolerance: "minimal"
    - reversibility: "required"
  
  path_analysis:
    convergent_paths: "[Paths reaching same conclusion]"
    divergent_paths: "[Paths with different conclusions]"
    outlier_paths: "[Unusual reasoning paths]"
    
  risk_assessment:
    consensus_risk: "[Risk if consensus is wrong]"
    disagreement_risk: "[Risk if outliers are right]"
    action_risk: "[Risk of taking action]"
    inaction_risk: "[Risk of no action]"
    
  decision_framework:
    go_condition: "[When to proceed with consensus]"
    stop_condition: "[When to seek more input]"
    escalation_condition: "[When to escalate decision]"
```

### Consensus Methods

**Voting Consensus**:
```yaml
voting:
  method: "simple_majority"
  threshold: ">50%"
  tie_breaking: "highest_confidence"
  
  example:
    path_1_conclusion: "Solution A"
    path_2_conclusion: "Solution A" 
    path_3_conclusion: "Solution B"
    result: "Solution A (2/3 majority)"
```

**Weighted Consensus**:
```yaml
weighted:
  method: "confidence_weighted"
  calculation: "sum(conclusion * confidence) / sum(confidence)"
  
  example:
    path_1: {conclusion: "85% Solution A", confidence: 90}
    path_2: {conclusion: "90% Solution A", confidence: 85}
    path_3: {conclusion: "70% Solution B", confidence: 75}
    weighted_result: "84% Solution A"
```

**Confidence-Based Consensus**:
```yaml
confidence_based:
  method: "highest_confidence_wins"
  minimum_threshold: 70
  uncertainty_flagging: true
  
  example:
    path_1: {conclusion: "Solution A", confidence: 95}
    path_2: {conclusion: "Solution A", confidence: 80}
    path_3: {conclusion: "Solution B", confidence: 75}
    result: "Solution A (95% confidence path)"
```

## Multi-Agent Debate (MAD) Method

### Purpose
Leverage diverse perspectives through structured adversarial reasoning, with personas representing different stakeholder viewpoints and domain expertise.

### Core Process
```yaml
1_agent_selection:
  - Choose 2-5 relevant personas based on problem domain
  - Ensure diverse perspectives and potential conflicts
  - Assign specific roles and priorities to each agent

2_position_establishment:
  - Each agent presents initial position with evidence
  - Document assumptions, priorities, and constraints
  - Establish success criteria from each perspective

3_debate_rounds:
  - 2-5 rounds of structured challenge and response
  - Agents present counter-arguments and new evidence
  - Focus on evidence quality and logical consistency

4_synthesis_phase:
  - Identify common ground and irreconcilable differences
  - Generate hybrid solutions incorporating multiple perspectives
  - Evaluate synthesis options against all agent criteria

5_resolution:
  - Apply resolution method (consensus, synthesis, escalation)
  - Document final decision and dissenting opinions
  - Create implementation plan addressing all concerns
```

### Implementation Templates

#### Basic MAD Template
```yaml
mad_session:
  problem: "[Problem statement]"
  agents: ["architect", "security", "performance"]
  rounds: 3
  resolution_method: "synthesis"
  
  round_1_positions:
    architect:
      position: "[Long-term architecture view]"
      evidence: "[Supporting evidence]"
      priorities: [maintainability, scalability, modularity]
      concerns: "[Concerns about other approaches]"
      
    security:
      position: "[Security-first approach]"
      evidence: "[Security evidence]"
      priorities: [security, compliance, risk_mitigation]
      concerns: "[Security risks in other approaches]"
    
    performance:
      position: "[Performance-optimized approach]"
      evidence: "[Performance data]"
      priorities: [speed, efficiency, resource_usage]
      concerns: "[Performance impact of other approaches]"
  
  round_2_challenges:
    architect_challenges:
      to_security: "[Challenge security approach]"
      to_performance: "[Challenge performance approach]"
    security_challenges:
      to_architect: "[Challenge architecture approach]"
      to_performance: "[Challenge performance approach]"
    performance_challenges:
      to_architect: "[Challenge architecture approach]"
      to_security: "[Challenge security approach]"
  
  round_3_synthesis:
    common_ground: "[Areas of agreement]"
    irreconcilable_differences: "[Fundamental conflicts]"
    hybrid_solutions: "[Compromise approaches]"
    
  final_resolution:
    chosen_approach: "[Selected solution]"
    rationale: "[Why this synthesis]"
    implementation_plan: "[How to address all concerns]"
    dissenting_opinions: "[Unresolved concerns]"
```

#### Cross-Functional MAD Template
```yaml
mad_cross_functional:
  problem: "[Feature implementation decision]"
  agents: ["frontend", "backend", "qa", "devops"]
  
  stakeholder_analysis:
    frontend_concerns: [user_experience, performance, accessibility]
    backend_concerns: [scalability, security, maintenance]
    qa_concerns: [testability, quality, risk]
    devops_concerns: [deployability, monitoring, reliability]
  
  conflict_mapping:
    frontend_vs_backend: "[UX vs security trade-offs]"
    qa_vs_devops: "[Testing depth vs deployment speed]"
    performance_vs_security: "[Speed vs safety conflicts]"
    
  synthesis_strategies:
    incremental_implementation: "[Phased approach addressing concerns]"
    parallel_solutions: "[Multiple approaches for different aspects]"
    compromise_solution: "[Balanced approach with trade-offs]"
    
  validation_plan:
    frontend_validation: "[How to validate UX concerns]"
    backend_validation: "[How to validate technical concerns]"
    qa_validation: "[Testing strategy]"
    devops_validation: "[Deployment and monitoring plan]"
```

### Agent Selection Patterns

**Technical Triad**:
```yaml
technical_triad:
  agents: ["architect", "security", "performance"]
  use_case: "System design decisions"
  strength: "Balanced technical perspective"
  resolution: "Evidence-based synthesis"
```

**User-Focused Triad**:
```yaml
user_focused:
  agents: ["frontend", "backend", "qa"]
  use_case: "Feature implementation"
  strength: "User value maximization"
  resolution: "User testing validation"
```

**Quality Triad**:
```yaml
quality_focused:
  agents: ["analyzer", "refactorer", "qa"]
  use_case: "Code quality decisions"
  resolution: "Long-term maintainability"
```

**Full Stakeholder**:
```yaml
full_stakeholder:
  agents: ["architect", "frontend", "backend", "security", "qa"]
  use_case: "Major system changes"
  strength: "Comprehensive perspective"
  resolution: "Consensus or escalation"
```

## Integration Patterns

### Sequential Integration
**Pattern**: Method → Method → Method
**Use Case**: Ultra-critical decisions requiring full analysis

```yaml
sequential_tot_mad_sc:
  phase_1_tot:
    purpose: "Explore solution space systematically"
    output: "3-5 viable solution branches"
    
  phase_2_mad:
    purpose: "Debate solutions from stakeholder perspectives"
    input: "ToT solution branches"
    output: "Stakeholder-validated solutions with trade-offs"
    
  phase_3_sc:
    purpose: "Validate final decision through multiple reasoning paths"
    input: "MAD consensus or synthesis"
    output: "High-confidence final decision"
    
  integration_points:
    tot_to_mad: "ToT branches become MAD debate topics"
    mad_to_sc: "MAD synthesis becomes SC validation target"
    
  quality_gates:
    - ToT branch diversity score >70%
    - MAD synthesis addresses all stakeholder concerns
    - SC consensus confidence >90%
```

### Parallel Integration
**Pattern**: Method || Method (simultaneous)
**Use Case**: Time-constrained decisions with validation needs

```yaml
parallel_tot_sc:
  parallel_execution:
    tot_branch:
      focus: "Solution exploration"
      timeline: "parallel_execution"
      
    sc_branch:
      focus: "Validation of current best approach"
      timeline: "parallel_execution"
      
  integration_strategy:
    convergence_check: "Do ToT and SC agree on solution?"
    divergence_handling: "If different, use MAD to resolve"
    time_boxing: "Maximum 60% of available time"
    
  decision_matrix:
    both_agree: "High confidence, proceed"
    tot_stronger: "Explore ToT recommendation with SC validation"
    sc_stronger: "Validate SC paths with ToT exploration"
    both_disagree: "Escalate to MAD or seek more input"
```

### Iterative Integration
**Pattern**: Method → Refinement → Method → Refinement
**Use Case**: Evolving requirements or complex learning scenarios

```yaml
iterative_refinement:
  cycle_1:
    method: "ToT"
    output: "Initial solution space"
    learning: "Understanding of problem complexity"
    
  refinement_1:
    action: "Refine problem definition"
    input: "ToT insights"
    output: "Updated requirements"
    
  cycle_2:
    method: "MAD"
    input: "Refined requirements + ToT solutions"
    output: "Stakeholder perspectives"
    learning: "Stakeholder conflicts and alignments"
    
  refinement_2:
    action: "Synthesize stakeholder needs"
    output: "Balanced requirements"
    
  cycle_3:
    method: "SC"
    input: "Synthesized solution"
    output: "Validated decision"
    
  convergence_criteria:
    - Solution addresses all refined requirements
    - Stakeholder concerns resolved or managed
    - Validation confidence >85%
```

## Performance Optimization

### Token Budget Management

**Method Cost Analysis**:
```yaml
baseline_reasoning: 1x
tree_of_thoughts: 3x-5x
self_consistency: 2x-3x
multi_agent_debate: 2.5x-4x

combined_methods:
  tot_mad: 4x-7x
  tot_sc: 4x-6x
  mad_sc: 3x-5x
  tot_mad_sc: 6x-10x
```

**Budget Allocation Strategy**:
```yaml
token_budget_5k:
  method: "SC only"
  paths: 2
  depth: "shallow"
  
token_budget_15k:
  method: "ToT or MAD"
  branches: 3-4
  rounds: 2-3
  
token_budget_30k:
  method: "ToT + SC or MAD + SC"
  comprehensive: "moderate"
  
token_budget_50k:
  method: "ToT + MAD + SC"
  comprehensive: "full"
```

### Efficiency Techniques

**Parallel Processing**:
- Independent reasoning paths executed simultaneously
- Branch evaluation in parallel where possible
- Concurrent persona analysis for MAD

**Caching Strategies**:
- Reuse branch evaluations across similar problems
- Cache persona positions for related debates
- Store consensus patterns for repeated decision types

**Progressive Refinement**:
- Start with quick SC validation
- Escalate to ToT if uncertainty detected
- Add MAD only if stakeholder conflicts identified

**Quality Gates**:
- Early termination if confidence thresholds met
- Automatic method selection based on problem characteristics
- Resource-based degradation (fewer branches/paths under constraints)

## Quality Validation

### Reasoning Quality Metrics

**Branch Quality (ToT)**:
- Diversity score: How different are solution approaches?
- Feasibility score: How implementable are solutions?
- Coverage score: Do branches cover the full solution space?

**Path Consistency (SC)**:
- Agreement percentage: How often do paths converge?
- Confidence correlation: Do higher confidence paths agree?
- Assumption validity: Are path assumptions realistic?

**Debate Quality (MAD)**:
- Perspective diversity: How different are agent positions?
- Evidence quality: How well-supported are arguments?
- Resolution completeness: Does synthesis address all concerns?

### Validation Framework

**10-Step Enhanced Validation Cycle**:
```yaml
step_1_method_selection:
  validation: "Optimal method for problem characteristics"
  criteria: "Problem type, complexity, stakeholders, constraints"
  
step_2_resource_validation:
  validation: "Token budget and time constraints feasible"
  criteria: "Available resources vs. method requirements"
  
step_3_branch_path_quality:
  validation: "ToT branches/SC paths sufficiently diverse and viable"
  criteria: "Coverage, feasibility, independence"
  
step_4_reasoning_consistency:
  validation: "Internal logical consistency within method"
  criteria: "Logical flow, assumption validity, evidence quality"
  
step_5_cross_method_coherence:
  validation: "Multiple methods produce coherent results"
  criteria: "Agreement across methods, explanation of disagreements"
  
step_6_stakeholder_representation:
  validation: "All relevant perspectives considered (MAD)"
  criteria: "Stakeholder coverage, concern representation"
  
step_7_confidence_calibration:
  validation: "Uncertainty explicitly identified and bounded"
  criteria: "Confidence accuracy, risk assessment, uncertainty quantification"
  
step_8_actionability:
  validation: "Results provide clear implementation guidance"
  criteria: "Specificity, feasibility, resource requirements"
  
step_9_reversibility:
  validation: "Decision enables rollback if outcomes don't match"
  criteria: "Monitoring plan, rollback triggers, alternative options"
  
step_10_learning_integration:
  validation: "Insights captured for future reasoning improvement"
  criteria: "Pattern documentation, success factors, failure modes"
```

## Troubleshooting Guide

### Common Issues and Solutions

**Low Branch Diversity (ToT)**:
- *Symptom*: All branches very similar
- *Cause*: Narrow problem framing or limited perspective
- *Solution*: Reframe problem, involve different personas, expand constraints

**Path Disagreement (SC)**:
- *Symptom*: Reasoning paths reach different conclusions
- *Cause*: Different assumptions or reasoning approaches
- *Solution*: Examine assumption differences, add validation path, escalate to ToT

**Debate Deadlock (MAD)**:
- *Symptom*: Agents cannot reach synthesis
- *Cause*: Fundamental value conflicts or missing information
- *Solution*: Escalate to architect persona, seek external input, implement parallel solutions

**Resource Exhaustion**:
- *Symptom*: Token budget exceeded before completion
- *Cause*: Too many branches/paths/rounds for available resources
- *Solution*: Reduce complexity, use progressive refinement, implement time-boxing

**Low Confidence Results**:
- *Symptom*: Final decisions have low confidence scores
- *Cause*: Insufficient analysis depth or conflicting evidence
- *Solution*: Add validation paths, gather more evidence, escalate complexity level

### Performance Tuning

**Speed Optimization**:
```yaml
quick_decisions:
  method: "SC with 2 paths"
  time: "minimal"
  confidence: "moderate"
  
balanced_decisions:
  method: "ToT with 3 branches or MAD with 3 agents"
  time: "moderate"
  confidence: "high"
  
comprehensive_decisions:
  method: "ToT + MAD + SC"
  time: "extensive"
  confidence: "maximum"
```

**Quality Optimization**:
```yaml
accuracy_critical:
  minimum_methods: 2
  validation_required: true
  confidence_threshold: 90%
  
stakeholder_critical:
  mad_required: true
  synthesis_method: "consensus"
  dissent_documentation: true
  
implementation_critical:
  tot_exploration: true
  feasibility_validation: true
  rollback_planning: true
```

## Best Practices

### Method Selection Guidelines

1. **Use ToT when**:
   - Multiple viable solution approaches exist
   - Solution space needs systematic exploration
   - Design decisions with long-term implications
   - Architecture or system design problems

2. **Use SC when**:
   - High accuracy requirements (>90%)
   - Critical decisions with significant consequences
   - Validation of existing solutions needed
   - Mathematical or analytical problems

3. **Use MAD when**:
   - Cross-functional stakeholder involvement
   - Competing priorities or value conflicts
   - Trade-off analysis with multiple perspectives
   - Consensus building required

4. **Use Combined Methods when**:
   - Ultra-critical decisions (ToT + MAD + SC)
   - Complex problems requiring exploration and validation (ToT + SC)
   - Stakeholder decisions needing validation (MAD + SC)

### Quality Assurance

**Before Reasoning**:
- Clear problem definition and success criteria
- Appropriate method selection based on problem characteristics
- Adequate resource allocation (time, tokens, complexity)

**During Reasoning**:
- Monitor branch/path diversity and quality
- Validate assumptions and evidence quality
- Track progress against quality gates

**After Reasoning**:
- Validate results against original requirements
- Document decision rationale and trade-offs
- Plan implementation with monitoring and rollback options

### Integration with SuperClaude Framework

**Persona Integration**:
- Leverage persona expertise for branch evaluation (ToT)
- Use persona debate capabilities for adversarial reasoning (MAD)
- Apply persona validation frameworks for quality assurance (SC)

**MCP Server Integration**:
- Context7 for research and best practices
- Sequential for structured analysis and coordination
- Magic for UI-related reasoning branches
- Playwright for testing and validation scenarios

**Command Integration**:
- `/analyze` with reasoning flags for comprehensive analysis
- `/design` with ToT for architecture exploration
- `/improve` with SC for validation of improvements
- `/implement` with MAD for stakeholder alignment

**Quality Gate Integration**:
- Reasoning validation as steps 2.5, 5.5, and 7.5 in 10-step cycle
- Method-specific quality criteria and success thresholds
- Automated confidence calibration and uncertainty quantification