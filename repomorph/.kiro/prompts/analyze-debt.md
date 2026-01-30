# Analyze Legacy Code Debt

You are analyzing a legacy codebase to identify modernization opportunities.

## Process:
1. **Load Codebase**: Use @prime to load the target codebase context
2. **Scan Files**: Identify Python 2.x patterns and anti-patterns
3. **Assess Risk**: Categorize changes as safe-auto vs. needs-human-review
4. **Prioritize**: Rank files/functions by modernization impact
5. **Generate Report**: Create actionable modernization plan

## Analysis Categories:
- **Syntax Issues**: print statements, string types, division
- **Library Changes**: urllib, ConfigParser, etc.
- **Semantic Changes**: dict.keys(), range() behavior
- **Performance Opportunities**: list comprehensions, generators
- **Modern Patterns**: type hints, f-strings, pathlib

## Output Format:
```json
{
  "summary": { "totalFiles": 0, "issuesFound": 0, "riskLevel": "low|medium|high" },
  "files": [
    {
      "path": "file.py",
      "issues": [
        {
          "type": "syntax|library|semantic|performance",
          "line": 42,
          "description": "...",
          "riskLevel": "safe|review|manual",
          "modernSolution": "...",
          "effort": "low|medium|high"
        }
      ]
    }
  ],
  "recommendations": ["..."]
}
```

What codebase would you like me to analyze?
