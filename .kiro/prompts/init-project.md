# Enter your prompt content here

You are initializing a hackathon project based on an evaluated idea.

## CRITICAL WORKFLOW ORDER
1. **FIRST**: Create project directory using `mkdir -p project-name`
2. **SECOND**: Change to project directory using `cd project-name`  
3. **THIRD**: Create all subdirectories using `mkdir -p` commands
4. **FOURTH**: Create files using write tool

**NEVER use write tool to create directories - it creates files instead!**

## Prerequisites
1. Ensure evaluations/[project-name]-evaluation.json exists
2. Ask user for:
   - Project directory name
   - Preferred tech stack (if not already specified)
   - Any specific requirements

## Initialization Steps

### Step 1: Create Project Structure
**CRITICAL: Always create directories using mkdir command FIRST, never use write tool for directories**

Based on the project type, create appropriate folder structure using shell commands:
- Web app: src/, public/, components/, etc.
- CLI tool: src/, bin/, lib/, etc.  
- API: routes/, controllers/, models/, etc.

**Example commands:**
```bash
mkdir -p project-name
cd project-name
mkdir -p src lib bin tests docs examples .kiro/steering .kiro/agents .kiro/prompts progress
```

### Step 2: Generate Custom Steering Documents

Create .kiro/steering/ files:

**product.md:**
- Project purpose (from evaluation)
- Target users
- Key features
- Success criteria
- Timeline and milestones

**tech.md:**
- Technology stack
- Architecture overview
- Development environment setup
- Code standards
- Testing strategy
- Performance requirements

**structure.md:**
- Directory layout
- File naming conventions
- Module organization
- Configuration files

**hackathon-strategy.md:**
- Current score and target score
- High-impact improvements
- Time allocation by feature
- Risk mitigation strategies

### Step 3: Create Custom Kiro Agents

Generate project-specific agents in .kiro/agents/:

**feature-builder.json:**
```json
{
  "name": "feature-builder",
  "description": "Builds features for [project name]",
  "tools": ["read", "write", "shell"],
  "resources": [
    "file://.kiro/steering/tech.md",
    "file://.kiro/steering/structure.md"
  ],
  "prompt": "You build features for [project name]. Follow the tech stack and structure defined in steering documents. Write clean, well-documented code."
}
```

**doc-maintainer.json:**
```json
{
  "name": "doc-maintainer",
  "description": "Maintains documentation for [project name]",
  "tools": ["read", "write"],
  "resources": [
    "file://README.md",
    "file://DEVLOG.md",
    "file://.kiro/steering/product.md"
  ],
  "prompt": "You maintain documentation. Keep README and DEVLOG up-to-date, clear, and professional."
}
```

### Step 4: Create Custom Prompts

Generate workflow prompts in .kiro/prompts/:

**build-feature.md:**
```markdown
Build a feature for [project name]:
1. Read relevant code and steering docs
2. Plan the implementation
3. Write clean, tested code
4. Update documentation
5. Update progress tracking
```

**update-docs.md:**
```markdown
Update project documentation:
1. Review recent changes (git log)
2. Update README if needed
3. Add entry to DEVLOG with:
   - What was built
   - Technical decisions
   - Challenges and solutions
   - Time spent
4. Update progress tracking
```

### Step 5: Initialize Documentation

Create initial README.md and DEVLOG.md using templates:
- Fill in project-specific information
- Add setup instructions
- Create initial DEVLOG entry

### Step 6: Create Progress Tracking

Create progress/state.json:
```json
{
  "projectName": "...",
  "startDate": "...",
  "evaluation": { /* copy from evaluation file */ },
  "currentScore": {
    "applicationQuality": 0,
    "kiroUsage": 5,
    "documentation": 5,
    "innovation": 0,
    "presentation": 0,
    "total": 10
  },
  "milestones": [],
  "completedTasks": [],
  "nextSteps": [],
  "timeTracking": {
    "totalHours": 0,
    "byCategory": {}
  }
}
```

## Step 7: Copy Global Prompts for Full Access

**Critical Step:** Copy all global Hackathon Sidekick prompts to local project:
```bash
# Copy all global prompts to local project
cp ../../.kiro/prompts/* .kiro/prompts/
```
### Step 8: Summary
Provide user with:
- What was created
- How to use custom agents and prompts
- Recommended next steps
- Quick start command
