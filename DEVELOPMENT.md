# Local Development Guide

This guide covers how to set up and work with the unified monorepo locally.

## Prerequisites

- **Node.js** >= 18.0.0
- **npm** >= 9.0.0
- **Git** >= 2.0.0

Verify installations:
```bash
node --version
npm --version
git --version
```

## Initial Setup

### 1. Clone the Repository

```bash
git clone https://github.com/romanchaa997/unified-projects-monorepo.git
cd unified-projects-monorepo
```

### 2. Install Dependencies

```bash
# Install all package dependencies at once
npm install

# This will install:
# - Root node_modules
# - Dependencies for all packages in packages/*
```

## Working with Packages

### Directory Structure

Each package in `packages/` is a self-contained project:

```
packages/
├── monobank-sdk/           # TypeScript SDK
│   ├── src/
│   ├── tests/
│   ├── package.json
│   └── ...
├── manus-zapier/           # Zapier Integration
│   ├── src/
│   ├── tests/
│   ├── package.json
│   └── ...
└── smart-bakhmach-iot/     # IoT Platform
    ├── src/
    ├── tests/
    ├── package.json
    └── ...
```

### Available Commands

#### Build All Packages

```bash
npm run build:all
```

This runs the `build` script in each package's package.json.

#### Test All Packages

```bash
npm run test:all
```

This runs the `test` script in each package.

#### Install Specific Package

```bash
# Install dependencies only for monobank-sdk
npm install --workspace=packages/monobank-sdk
```

#### Run Script in Specific Package

```bash
# Run build only for monobank-sdk
npm run build --workspace=packages/monobank-sdk
```

#### Add Dependency to Package

```bash
# Add a dependency to monobank-sdk
npm install lodash --workspace=packages/monobank-sdk

# Add a dev dependency
npm install --save-dev jest --workspace=packages/monobank-sdk
```

## Development Workflow

### 1. Create Feature Branch

```bash
git checkout -b feature/your-feature-name
```

### 2. Make Changes

Edit files in the appropriate package(s):
- TypeScript changes should include type definitions
- Add tests for new functionality
- Update relevant documentation

### 3. Build & Test

```bash
# Build all packages
npm run build:all

# Run all tests
npm run test:all
```

### 4. Commit Changes

```bash
git add .
git commit -m "feat: add new feature"
```

Follow [Conventional Commits](https://www.conventionalcommits.org/) format:
- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation
- `style:` - Code style
- `refactor:` - Refactoring
- `test:` - Tests
- `chore:` - Maintenance

### 5. Push & Create PR

```bash
git push origin feature/your-feature-name
```

Create a Pull Request on GitHub.

## Debugging

### View Workspace Structure

```bash
# Show npm workspace configuration
cat package.json
```

### Check Package Versions

```bash
# List all workspaces and their versions
npm ls --depth=0 -w
```

### Clean Install

If you encounter issues, try a clean installation:

```bash
# Remove all node_modules and lock files
rm -rf node_modules package-lock.json
rm -rf packages/*/node_modules

# Reinstall
npm install
```

## Common Issues

### Issue: `npm: command not found`
- **Solution:** Install Node.js from https://nodejs.org/

### Issue: `npm ERR! code ERESOLVE`
- **Solution:** Try `npm install --legacy-peer-deps` or update npm: `npm install -g npm@latest`

### Issue: Module not found errors
- **Solution:** Run `npm install` in the root directory

### Issue: Build failing in specific package
- **Solution:** Check the package's README for specific setup requirements

## Git Workflow

### Before Starting

```bash
# Update main branch
git checkout main
git pull origin main
```

### After Features

```bash
# Update from main
git fetch origin
git rebase origin/main

# Or merge if rebasing fails
git merge origin/main
```

## Performance Tips

1. **Use npm workspaces cache:**
   ```bash
   npm ci  # Use instead of npm install in CI/CD
   ```

2. **Build only changed packages:**
   ```bash
   npm run build --workspace=packages/monobank-sdk
   ```

3. **Watch mode for development:**
   Check individual package's scripts for `watch` commands

## Resources

- [npm Workspaces Documentation](https://docs.npmjs.com/cli/using-npm/workspaces)
- [Node.js Documentation](https://nodejs.org/docs/)
- [Git Documentation](https://git-scm.com/doc)
- [Conventional Commits](https://www.conventionalcommits.org/)

## Getting Help

If you encounter issues:

1. Check the specific package's README
2. Review CONTRIBUTING.md for guidelines
3. Check GitHub Issues for similar problems
4. Ask in the project's discussions

---

**Happy coding!** 🚀
