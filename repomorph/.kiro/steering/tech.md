# RepoMorph Technical Architecture

## Technology Stack
- **Runtime**: Node.js 18+ with TypeScript for type safety
- **CLI Framework**: Commander.js for command-line interface
- **AST Parsing**: Python AST parser via `python-ast` or `py-ast-parser`
- **Code Analysis**: Custom analyzers built on AST traversal
- **Web UI**: React with Vite for fast development
- **Visualization**: D3.js for dependency graphs, CodeMirror for code display
- **AI Integration**: Kiro CLI for intent analysis and transformation logic

## Architecture Overview
```
RepoMorph CLI
├── Analysis Engine (src/analyzers/)
│   ├── PythonAnalyzer - AST parsing and pattern detection
│   ├── IntentAnalyzer - AI-powered code understanding
│   └── RiskAssessor - Safety classification
├── Transformation Engine (src/transformers/)
│   ├── SyntaxTransformer - Direct syntax updates
│   ├── PatternTransformer - Common pattern modernization
│   └── IntentTransformer - AI-guided refactoring
├── Web UI (src/ui/)
│   ├── CodeViewer - Before/after comparison
│   ├── RiskDashboard - Migration planning interface
│   └── ProgressTracker - Conversion status
└── CLI Interface (bin/)
    └── repomorph - Main command entry point
```

## Development Environment
- **Node.js 18+** with npm/yarn package management
- **TypeScript 5+** for static typing and better IDE support
- **ESLint + Prettier** for code quality and formatting
- **Jest** for unit testing
- **Kiro CLI** for AI-powered development assistance

## Code Standards
- **TypeScript strict mode** with comprehensive type definitions
- **Functional programming** patterns for analyzers and transformers
- **Error handling** with Result types for safe operations
- **Modular architecture** with clear separation of concerns
- **Comprehensive logging** for debugging and user feedback

## Testing Strategy
- **Unit tests** for all analyzers and transformers (>80% coverage)
- **Integration tests** for end-to-end CLI workflows
- **Sample codebases** for testing different Python 2→3 scenarios
- **Performance benchmarks** for large codebase analysis
- **Manual testing** with real-world legacy projects

## Performance Requirements
- **Analysis speed**: <30 seconds for 10,000 line codebases
- **Memory usage**: <512MB for typical projects
- **Accuracy**: >95% correct pattern detection
- **Risk assessment**: <5% false positive rate for safety classification

## Security Considerations
- **Input validation** for all file paths and code inputs
- **Sandboxed execution** for any dynamic code analysis
- **No external API calls** for sensitive code analysis
- **Local-only processing** to protect proprietary codebases
