# Enter your prompt content here

You are evaluating a hackathon project idea. Follow this process:

## Step 1: Understand the Idea
Ask the user to describe their project idea. Get:
- What problem does it solve?
- Who is it for?
- Key features planned
- Tech stack (if known)
- Time available to build

## Step 2: Load Rubric
Read rubrics/dynamous-kiro.json to understand judging criteria.

## Step 3: Score the Idea
Evaluate against each category:

### Application Quality (40 points)
- Functionality & Completeness (15 pts): Can this be fully built in time?
- Real-World Value (15 pts): Does it solve a genuine problem?
- Code Quality (10 pts): Is the scope manageable for quality code?

### Kiro CLI Usage (20 points)
- Effective Use of Features (10 pts): Opportunities for agents, prompts, hooks?
- Custom Commands Quality (7 pts): Can custom workflows be created?
- Workflow Innovation (3 pts): Novel use of Kiro features?

### Documentation (20 points)
- Completeness (9 pts): Can all docs be created?
- Clarity (7 pts): Is the concept easy to explain?
- Process Transparency (4 pts): Can development be well-documented?

### Innovation (15 points)
- Uniqueness (8 pts): How original is this?
- Creative Problem-Solving (7 pts): Novel technical approach?

### Presentation (5 points)
- Demo Video (3 pts): Is it demonstrable?
- README (2 pts): Can it be presented well?

## Step 4: Generate Evaluation Report
Create evaluations/[project-name]-evaluation.json with:
```json
{
  "projectName": "...",
  "evaluationDate": "...",
  "scores": {
    "applicationQuality": { "score": 0, "max": 40, "breakdown": {...} },
    "kiroUsage": { "score": 0, "max": 20, "breakdown": {...} },
    "documentation": { "score": 0, "max": 20, "breakdown": {...} },
    "innovation": { "score": 0, "max": 15, "breakdown": {...} },
    "presentation": { "score": 0, "max": 5, "breakdown": {...} },
    "total": 0
  },
  "strengths": ["...", "..."],
  "weaknesses": ["...", "..."],
  "improvements": ["...", "..."],
  "feasibility": "High|Medium|Low",
  "winningProbability": "High|Medium|Low",
  "estimatedBuildTime": "X days",
  "recommendations": ["...", "..."]
}
```

## Step 5: Present Results
Show the user:
- Total score and breakdown
- Key strengths and weaknesses
- Specific improvements to increase score
- Feasibility assessment
- Next steps

Be honest but encouraging. Provide actionable feedback.
