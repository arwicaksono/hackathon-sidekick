# Project Structure

## Directory Layout
```
Hackathon Sidekick/
├── .kiro/
│   ├── prompts/           # Custom Kiro prompts for hackathon workflows
│   │   ├── evaluate-idea.md
│   │   ├── track-progress.md
│   │   ├── generate-docs.md
│   │   └── validate-submission.md
│   ├── steering/          # Project context and guidelines
│   │   ├── product.md
│   │   ├── tech.md
│   │   └── structure.md
│   └── agents/            # Specialized agents for different tasks
│       ├── hackathon-mentor.json
│       └── documentation-specialist.json
├── templates/             # JSON templates for different hackathon types
│   ├── web-app-template.json
│   ├── mobile-app-template.json
│   ├── ai-ml-template.json
│   └── blockchain-template.json
├── rubrics/              # Judging criteria and scoring frameworks
│   ├── general-rubric.json
│   ├── technical-rubric.json
│   └── innovation-rubric.json
├── examples/             # Sample projects and documentation
│   ├── sample-readme.md
│   ├── sample-pitch-deck.md
│   └── sample-devlog.md
├── cli/                  # Optional CLI wrapper components
│   ├── package.json      # Node.js dependencies
│   ├── index.js          # Main CLI entry point
│   └── commands/         # CLI command implementations
├── docs/                 # Project documentation
│   ├── user-guide.md
│   ├── setup-instructions.md
│   └── api-reference.md
└── README.md             # Main project documentation
```

## File Naming Conventions
**Kiro Prompts:**
- Use kebab-case: `evaluate-idea.md`, `track-progress.md`
- Descriptive action-based names
- `.md` extension for all prompts

**Templates & Configurations:**
- Use kebab-case with descriptive suffixes: `web-app-template.json`
- JSON files for structured data
- Clear category prefixes where applicable

**Documentation:**
- Use kebab-case: `user-guide.md`, `setup-instructions.md`
- Markdown format for all documentation
- Descriptive, searchable filenames

## Module Organization
**Kiro Prompt Categories:**
- **Core Workflow**: Idea evaluation, progress tracking, documentation generation
- **Specialized Tasks**: Submission validation, timeline management, team coordination
- **Utility Prompts**: Setup wizards, troubleshooting, help systems

**Template Categories:**
- **Project Types**: Web apps, mobile apps, AI/ML, blockchain, hardware
- **Hackathon Types**: Corporate hackathons, open source, themed competitions
- **Judging Frameworks**: Technical excellence, innovation, business impact

## Configuration Files
**Kiro Configuration:**
- `.kiro/steering/`: Project context and guidelines
- `.kiro/prompts/`: Custom workflow prompts
- `.kiro/agents/`: Specialized AI agents

**Project Configuration:**
- `package.json`: Node.js dependencies and scripts (if using CLI wrapper)
- `requirements.txt`: Python dependencies (if using Python wrapper)
- Template JSON files: Hackathon-specific configurations

## Documentation Structure
**User Documentation:**
- `README.md`: Project overview and quick start
- `docs/user-guide.md`: Comprehensive usage instructions
- `docs/setup-instructions.md`: Installation and configuration

**Developer Documentation:**
- `docs/api-reference.md`: Prompt and template specifications
- `examples/`: Sample implementations and use cases
- Inline comments in all prompt files

## Asset Organization
**Templates:**
- Organized by hackathon type and complexity
- JSON schema validation for consistency
- Example data included in each template

**Examples:**
- Real-world sample projects
- Documentation templates
- Best practice demonstrations

## Build Artifacts
**Generated Files:**
- User-generated project documentation
- Customized templates based on user input
- Progress tracking and scoring reports
- Submission validation checklists

**Distribution:**
- Git repository for source code
- npm/pip packages for optional CLI wrappers
- Documentation hosted on GitHub Pages

## Environment-Specific Files
**Development:**
- Local Kiro CLI configuration
- Development templates and test data
- Debug logging and validation tools

**Production:**
- Optimized prompt templates
- Production-ready documentation generators
- Performance monitoring and analytics
