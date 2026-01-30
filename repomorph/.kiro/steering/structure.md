# RepoMorph Project Structure

## Directory Layout
```
repomorph/
├── src/
│   ├── analyzers/           # Code analysis engines
│   │   ├── PythonAnalyzer.ts
│   │   ├── IntentAnalyzer.ts
│   │   └── RiskAssessor.ts
│   ├── transformers/        # Code transformation logic
│   │   ├── SyntaxTransformer.ts
│   │   ├── PatternTransformer.ts
│   │   └── IntentTransformer.ts
│   ├── ui/                  # Web interface components
│   │   ├── components/
│   │   ├── pages/
│   │   └── utils/
│   ├── types/               # TypeScript type definitions
│   └── utils/               # Shared utilities
├── lib/                     # Compiled JavaScript output
├── bin/                     # CLI executables
│   └── repomorph.js
├── test/                    # Test files
│   ├── analyzers/
│   ├── transformers/
│   └── fixtures/            # Sample code for testing
├── examples/                # Demo codebases
│   ├── python2-legacy/
│   └── python3-modern/
├── .kiro/                   # Kiro CLI configuration
│   ├── steering/
│   ├── agents/
│   └── prompts/
├── progress/                # Progress tracking
└── docs/                    # Documentation
```

## File Naming Conventions
- **TypeScript files**: PascalCase for classes, camelCase for utilities
- **Test files**: `*.test.ts` or `*.spec.ts`
- **Configuration**: kebab-case (e.g., `tsconfig.json`, `package.json`)
- **Documentation**: kebab-case with `.md` extension

## Module Organization
- **Analyzers**: Single responsibility, composable analysis functions
- **Transformers**: Pure functions that take AST and return modified AST
- **Types**: Shared interfaces and type definitions
- **Utils**: Helper functions used across modules

## Configuration Files
- `package.json`: Dependencies and scripts
- `tsconfig.json`: TypeScript compilation settings
- `.eslintrc.js`: Code quality rules
- `jest.config.js`: Testing configuration
- `vite.config.ts`: Web UI build configuration

## Import/Export Patterns
- **Barrel exports** from index files for clean imports
- **Named exports** preferred over default exports
- **Absolute imports** using TypeScript path mapping
- **Type-only imports** where appropriate

## Build Artifacts
- `lib/`: Compiled JavaScript for distribution
- `dist/`: Web UI build output
- `coverage/`: Test coverage reports
- `docs/`: Generated API documentation
