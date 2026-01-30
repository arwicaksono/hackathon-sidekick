# Hackathon Sidekick Commands

Quick reference guide for all Hackathon Sidekick commands and recommended workflows.

## 🎯 Main Interface

### `@sidekick`
**Purpose**: Main menu interface for all hackathon workflows  
**When to use**: Starting point for all hackathon activities  
**What it does**: 
- Provides guided menu of all available workflows
- Shows current project status and next recommended steps
- Offers quick access to evaluation, progress tracking, and documentation
- Guides users through the complete hackathon development process

**Usage**: Simply type `@sidekick` - interactive menu will guide you

---

## 🚀 Project Setup & Evaluation Commands

### `@evaluate-idea`
**Purpose**: Analyze project ideas against hackathon judging criteria  
**When to use**: Before starting development, when considering new features  
**What it does**:
- Evaluates ideas against the 100-point judging rubric
- Provides score predictions and feasibility assessment
- Identifies strengths, weaknesses, and improvement opportunities
- Generates detailed evaluation reports with winning probability

**Usage**: `@evaluate-idea` (will ask for project description and details)

---

### `@init-project`
**Purpose**: Set up optimal Kiro CLI configuration for hackathon development  
**When to use**: After completing idea evaluation  
**What it does**:
- Configures Kiro CLI settings for hackathon workflows
- Sets up custom agents and automation hooks
- Initializes progress tracking and documentation systems
- Prepares development environment for maximum efficiency

**Usage**: `@init-project` (requires completed evaluation)

---

## 📊 Progress Tracking & Documentation Commands

### `@update-progress`
**Purpose**: Track development progress and update project state  
**When to use**: After completing work sessions or major milestones  
**What it does**:
- Records time spent and features completed
- Updates progress tracking files
- Calculates current score against judging criteria
- Identifies next priority tasks and improvements

**Usage**: `@update-progress` (will ask about recent work completed)

---

### `@progress-report`
**Purpose**: Generate comprehensive progress summary and score analysis  
**When to use**: Regular check-ins, before major decisions, submission preparation  
**What it does**:
- Shows current score breakdown across all 5 judging categories
- Provides detailed analysis of strengths and improvement areas
- Recommends next steps to maximize score
- Tracks progress toward submission readiness

**Usage**: `@progress-report` - comprehensive project status

---

### `@update-devlog`
**Purpose**: Maintain comprehensive development log automatically  
**When to use**: Daily development sessions, after completing features  
**What it does**:
- Updates DEVLOG.md with recent development activities
- Documents technical decisions and challenges
- Tracks time spent and Kiro CLI usage
- Maintains professional development history

**Usage**: `@update-devlog` (will ask about recent development work)

---

### `@update-readme`
**Purpose**: Keep project README.md current and professional  
**When to use**: After major features, before submission, regular maintenance  
**What it does**:
- Updates project description and feature lists
- Ensures setup instructions are current
- Maintains professional presentation standards
- Optimizes for hackathon judging criteria

**Usage**: `@update-readme` - automatic README maintenance

---

## 🔍 Quality Assurance & Submission Commands

### `@submission-check`
**Purpose**: Final validation and submission readiness checklist  
**When to use**: Before final submission, periodic readiness checks  
**What it does**:
- Validates all submission requirements are met
- Checks documentation completeness and quality
- Verifies demo video and presentation materials
- Provides final optimization recommendations

**Usage**: `@submission-check` - comprehensive submission validation

---

### `@code-review-hackathon`
**Purpose**: Hackathon-specific evaluation against judging criteria  
**When to use**: Periodic score checks, before submission  
**What it does**:
- Evaluates project against all 5 hackathon judging categories
- Provides detailed score breakdown and improvement suggestions
- Identifies specific areas to increase points
- Validates submission quality and competitiveness

**Usage**: `@code-review-hackathon` - comprehensive hackathon evaluation

---

## 📈 Recommended Workflows

### 🎯 **Initial Project Setup**
```
1. @sidekick              # Access main menu
2. @evaluate-idea         # Analyze your concept
3. @init-project          # Configure Kiro setup
```

### 🔄 **Daily Development Cycle**
```
1. @sidekick              # Check current status
2. [Development work]     # Build features
3. @update-progress       # Track completed work
4. @update-devlog         # Document progress
5. @progress-report       # Check score status
```

### 📋 **Documentation Maintenance**
```
1. @update-devlog         # Maintain development log
2. @update-readme         # Keep README current
3. @progress-report       # Verify documentation score
```

### 🏆 **Submission Preparation**
```
1. @progress-report       # Check current score
2. @update-readme         # Finalize documentation
3. @submission-check      # Validate requirements
4. @code-review-hackathon # Final evaluation
```

### 🔍 **Score Optimization**
```
1. @progress-report       # Identify weak areas
2. [Targeted improvements] # Address specific issues
3. @update-progress       # Track improvements
4. @code-review-hackathon # Verify score increase
```

---

## 💡 Usage Tips

### **Start with @sidekick**
The main menu provides guided access to all workflows and shows your current status and recommended next steps.

### **Regular Progress Tracking**
Use `@update-progress` and `@progress-report` frequently to stay on track for maximum score.

### **Documentation First**
Maintain your DEVLOG.md continuously with `@update-devlog` - it's worth significant points in judging.

### **Score Awareness**
Run `@code-review-hackathon` regularly to understand your current competitive position.

### **Submission Readiness**
Use `@submission-check` early and often to ensure you're meeting all requirements.

---

## 🎯 Quick Command Reference

| Command | Purpose | When to Use |
|---------|---------|-------------|
| `@sidekick` | Main menu interface | Starting point for all workflows |
| `@evaluate-idea` | Analyze project ideas | Before development starts |
| `@init-project` | Configure Kiro setup | After idea evaluation |
| `@update-progress` | Track development | After work sessions |
| `@progress-report` | Score analysis | Regular check-ins |
| `@update-devlog` | Maintain DEVLOG | Daily development |
| `@update-readme` | Update README | Documentation maintenance |
| `@submission-check` | Validate submission | Before final submission |
| `@code-review-hackathon` | Hackathon evaluation | Score optimization |

---

**Remember**: Start with `@sidekick` to access the main menu, use `@evaluate-idea` to analyze your concept, and maintain regular progress tracking with `@update-progress` and `@progress-report` for maximum hackathon success!
