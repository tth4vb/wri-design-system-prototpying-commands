# WRI Design System Slash Commands

These slash commands help maintain WRI Design System compliance in your prototypes.

## Available Commands

### `/validate-wri`
**Deep validation with detailed analysis**

Performs comprehensive validation of the current file:
- Reads TypeScript type definitions from the design system
- Checks all component props against actual types
- Validates color usage (must use `getThemedColor()`)
- Flags native HTML elements
- Checks for common API mistakes

Provides detailed report with:
- Line numbers and code snippets
- Correct code examples
- Links to Storybook documentation

**When to use**: When you need detailed analysis and want to understand exactly what's wrong.

---

### `/validate-quick`
**Fast automated validation**

Runs the bash validation script (`npm run validate`) and summarizes results.

**When to use**: Quick check during development to catch obvious issues.

---

### `/fix-wri`
**Automatic fix for common issues**

Automatically fixes common compliance issues:
- Hardcoded colors → `getThemedColor()`
- Modal API mistakes
- Select API mistakes
- RadioGroup missing props
- Missing imports

**When to use**: After validation finds issues, let this command fix them automatically.

---

## Workflow

1. **While coding**: Use `/validate-quick` periodically
2. **Found issues**: Use `/fix-wri` to auto-fix
3. **Need details**: Use `/validate-wri` for deep analysis
4. **Before commit**: Pre-commit hook runs automatically

## Examples

```
# Quick check
/validate-quick

# Auto-fix issues
/fix-wri

# Detailed analysis
/validate-wri
```

## Manual Validation

You can also run validation manually:

```bash
# From example-prototype directory
npm run validate

# Or directly
./scripts/validate-wri-compliance.sh
```
