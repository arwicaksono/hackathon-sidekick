# Hackathon Sidekick Architecture

## Overview

Hackathon Sidekick is built as a **Kiro CLI-native framework** that leverages AI-powered development assistance to guide users through successful hackathon participation. The architecture emphasizes modularity, extensibility, and seamless integration with existing development workflows.

## System Components

### 🧠 AI-Powered Prompts
**Location**: `.kiro/prompts/`  
**Purpose**: Specialized commands for hackathon-specific workflows

```
.kiro/prompts/
├── sidekick.md               # Main menu interface for all workflows
├── evaluate-idea.md          # Project idea analysis and scoring
├── init-project.md           # Optimal Kiro configuration setup
├── update-progress.md        # Development progress tracking
├── progress-report.md        # Progress summary and score analysis
├── update-devlog.md          # Automated DEVLOG.md maintenance
├── update-readme.md          # README.md updates and formatting
├── submission-check.md       # Final submission validation
├── code-review-hackathon.md  # Hackathon-specific evaluation
├── prime.md                  # Project context loading
├── plan-feature.md           # Feature planning and breakdown
├── execute.md                # Systematic implementation
├── code-review.md            # Technical code review
├── code-review-fix.md        # Issue resolution
├── system-review.md          # Process analysis
├── create-prd.md             # Product requirements
├── execution-report.md       # Implementation documentation
├── rca.md                    # Root cause analysis
└── implement-fix.md          # Fix implementation
```

**Characteristics**:
- **Menu-driven interface**: @sidekick provides guided access to all workflows
- **Hackathon-optimized**: Focused on winning hackathon submissions
- **Score-aware**: Integration with 100-point judging rubric
- **Documentation-first**: Automated maintenance of DEVLOG and README

### 📋 Steering Documents
**Location**: `.kiro/steering/`  
**Purpose**: Persistent project knowledge and context

```
.kiro/steering/
├── product.md             # Product vision and requirements
├── tech.md               # Technical architecture and standards
├── structure.md          # Project organization guidelines
└── kiro-cli-reference.md # Kiro CLI usage patterns
```

**Data Flow**:
- **Input**: User responses during `@init-project` setup
- **Processing**: Template population with project-specific details
- **Output**: Persistent context for all AI interactions
- **Updates**: Continuous refinement throughout development

### 📊 Evaluation & Scoring System
**Location**: `rubrics/` and `examples/`  
**Purpose**: Hackathon submission evaluation and optimization

```
rubrics/
└── dynamous-kiro.json     # 100-point evaluation framework

examples/
├── sample-evaluation.json  # Example scoring output
├── sample-progress.json   # Progress tracking example
└── sample-devlog-entry.md # Professional DEVLOG sample
```

**Scoring Categories**:
1. **Application Quality** (40 points) - Functionality, value, code quality
2. **Kiro CLI Usage** (20 points) - Feature usage, custom commands, innovation
3. **Documentation** (20 points) - Completeness, clarity, process transparency
4. **Innovation** (15 points) - Uniqueness, creative problem-solving
5. **Presentation** (5 points) - Demo video, README quality

### 🎯 Template System
**Location**: `templates/`  
**Purpose**: Professional project structure and documentation

```
templates/
├── README-template.md     # Professional project documentation
├── DEVLOG-template.md     # Development log format
└── project-structure.txt  # Tech stack-specific organizations
```

**Template Categories**:
- **Documentation**: README, DEVLOG, API docs
- **Project Structures**: Web apps, mobile, AI/ML, blockchain, APIs, desktop, CLI
- **Configuration**: Environment setup, deployment, testing

### ⚡ Automation System
**Location**: `.kiro/settings/`  
**Purpose**: Workflow automation and optimization

```
.kiro/settings/
└── hooks.json            # Automated workflow triggers
```

**Hook Types**:
- **postToolUse**: Progress tracking after file operations
- **userPromptSubmit**: Context-aware reminders based on user input
- **agentSpawn**: Hackathon-specific setup reminders
- **stop**: Session completion and documentation reminders

## Data Flow Architecture

### 1. Project Initialization Flow
```
User Input → @sidekick → @evaluate-idea → @init-project → Project Setup
```

**Process**:
1. User runs `@sidekick` for main menu
2. `@evaluate-idea` analyzes project concept against judging criteria
3. Score prediction and feasibility assessment provided
4. `@init-project` configures optimal Kiro CLI setup
5. Development environment ready for hackathon workflow

### 2. Development Workflow Flow
```
@sidekick → @update-progress → Development Work → @update-devlog → @progress-report
```

**Process**:
1. `@sidekick` provides workflow guidance and menu access
2. `@update-progress` tracks current development state
3. Regular development work with standard Kiro CLI features
4. `@update-devlog` maintains comprehensive development log
5. `@progress-report` shows current score and next priorities

### 3. Evaluation & Optimization Flow
```
@progress-report → Score Analysis → @update-readme → @submission-check → Final Submission
```

**Process**:
1. `@progress-report` evaluates current project against 100-point rubric
2. Detailed scoring breakdown with improvement recommendations
3. `@update-readme` ensures professional project presentation
4. `@submission-check` validates all submission requirements
5. Final optimization and submission preparation

### 4. Issue Resolution Flow
```
Problem Detection → @rca → Root Cause Analysis → @implement-fix → Solution Implementation → @system-review → Process Improvement
```

**Process**:
1. Issue identified during development or testing
2. `@rca` performs systematic root cause analysis
3. Detailed investigation with timeline and contributing factors
4. `@implement-fix` creates and implements solution
5. `@system-review` analyzes process for future improvements

## Component Interactions

### AI Context Management
```
Steering Documents ←→ Kiro CLI ←→ Custom Prompts
       ↓                ↓              ↓
Project Knowledge → AI Processing → Specialized Workflows
```

**Integration Points**:
- **Steering → Prompts**: Persistent context influences all AI responses
- **Prompts → Evaluation**: Commands generate data for scoring analysis
- **Evaluation → Documentation**: Scoring results inform improvement strategies
- **Hooks → Workflow**: Automation triggers enhance development process

### Data Persistence Strategy
```
User Actions → JSON State Files → Progress Tracking → Evaluation Input
     ↓              ↓                    ↓               ↓
Documentation ← Template System ← Automation Hooks ← Scoring System
```

**Storage Patterns**:
- **Configuration**: JSON files for structured data (rubrics, progress, state)
- **Documentation**: Markdown files for human-readable content
- **Templates**: Reusable patterns for consistent project structure
- **Examples**: Reference implementations showing best practices

## Extension Points

### 1. Custom Prompt Development
**Location**: `.kiro/prompts/`  
**Extension Method**: Add new Markdown files with specialized workflows

**Example Extensions**:
```markdown
# @deploy-hackathon.md
Specialized deployment workflow for hackathon submissions

# @team-coordination.md  
Multi-developer coordination and task management

# @presentation-prep.md
Demo video and presentation preparation
```

### 2. Specialized Agent Creation
**Location**: `.kiro/agents/`  
**Extension Method**: JSON configuration files for domain experts

**Example Agents**:
```json
{
  "name": "hackathon-mentor",
  "description": "Specialized hackathon strategy and optimization",
  "tools": ["read", "write", "@code-review-hackathon"],
  "resources": ["file://rubrics/**/*.json", "file://examples/**/*"]
}
```

### 3. Additional Rubric Systems
**Location**: `rubrics/`  
**Extension Method**: JSON files for different hackathon types

**Example Rubrics**:
- `corporate-hackathon.json` - Enterprise-focused evaluation criteria
- `ai-ml-hackathon.json` - Machine learning competition rubric
- `blockchain-hackathon.json` - Web3 and cryptocurrency focus
- `social-impact.json` - Social good and sustainability criteria

### 4. Template Expansion
**Location**: `templates/`  
**Extension Method**: Additional templates for emerging technologies

**Example Templates**:
- `AR-VR-template.md` - Augmented/Virtual Reality projects
- `IoT-template.md` - Internet of Things applications
- `quantum-template.md` - Quantum computing projects
- `sustainability-template.md` - Environmental impact projects

### 5. MCP Server Integration
**Location**: `.kiro/settings/mcp.json`  
**Extension Method**: External tool and service connections

**Example Integrations**:
```json
{
  "mcpServers": {
    "github-integration": {
      "command": "github-mcp-server",
      "args": ["--repo", "hackathon-project"]
    },
    "deployment-tools": {
      "command": "deployment-mcp-server", 
      "args": ["--platform", "vercel"]
    },
    "analytics-tracker": {
      "command": "analytics-mcp-server",
      "args": ["--hackathon", "dynamous-kiro"]
    }
  }
}
```

### 6. Automation Hook Expansion
**Location**: `.kiro/settings/hooks.json`  
**Extension Method**: Additional lifecycle triggers

**Example Hooks**:
```json
{
  "hooks": {
    "preCommit": [
      {"command": "npm test && npm run lint"}
    ],
    "postDeploy": [
      {"command": "echo 'Deployment complete! Update DEVLOG.md'"}
    ],
    "milestoneReached": [
      {"command": "@execution-report && @code-review-hackathon"}
    ]
  }
}
```

## Scalability & Performance

### Modular Design Benefits
- **Independent Components**: Each system component can be modified without affecting others
- **Incremental Adoption**: Users can adopt features progressively based on needs
- **Technology Agnostic**: Framework works with any programming language or tech stack
- **Version Control Friendly**: All components are text-based and git-compatible

### Performance Characteristics
- **Minimal Overhead**: No runtime dependencies beyond Kiro CLI
- **Fast Initialization**: Template-based setup completes in under 30 seconds
- **Efficient Context**: Steering documents provide persistent knowledge without repeated setup
- **Scalable Evaluation**: JSON-based scoring system handles complex rubrics efficiently

### Extensibility Patterns
- **Plugin Architecture**: New prompts and agents can be added without core modifications
- **Template Inheritance**: New templates can extend existing patterns
- **Configuration Override**: Local settings can override global defaults
- **Community Contributions**: Framework designed for easy sharing and collaboration

## Security Considerations

### Data Privacy
- **Local Storage**: All project data remains on user's machine
- **No External Dependencies**: Framework operates entirely within Kiro CLI ecosystem
- **Configurable Sharing**: Users control what information is included in templates

### Access Control
- **File System Permissions**: Standard OS-level access controls apply
- **Kiro CLI Security**: Inherits security model from Kiro CLI platform
- **Template Validation**: JSON schemas prevent malformed configuration

### Best Practices
- **Sensitive Data Handling**: Templates include placeholders for secrets and API keys
- **Input Validation**: Prompts include guidance for secure coding practices
- **Audit Trail**: DEVLOG.md provides complete development history for security review

---

## Summary

Hackathon Sidekick's architecture prioritizes **modularity**, **extensibility**, and **seamless integration** with existing development workflows. By leveraging Kiro CLI's native capabilities and providing structured templates, examples, and automation, the framework enables developers to focus on building innovative solutions while maintaining professional development practices.

The system's **component-based design** allows for easy customization and extension, while the **template-driven approach** ensures consistency and quality across different project types and skill levels. This architecture directly supports the goal of democratizing hackathon success by providing systematic guidance and automation for all participants.
