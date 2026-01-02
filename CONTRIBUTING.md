# Contributing to Unified Projects Monorepo

Thank you for your interest in contributing to this unified monorepo project!

## Getting Started

1. **Fork the repository**
2. **Clone your fork:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/unified-projects-monorepo.git
   cd unified-projects-monorepo
   ```

3. **Install dependencies:**
   ```bash
   npm install
   ```

## Project Structure

The monorepo contains three main packages under `packages/`:

- **monobank-sdk** - TypeScript SDK for Monobank API
- **manus-zapier** - Zapier integration for Manus AI Agent  
- **smart-bakhmach-iot** - IoT platform for smart city

## Development Workflow

### Working on a specific package

```bash
# Install packages from root
npm install

# Run build for all packages
npm run build:all

# Run tests for all packages
npm run test:all
```

### Submitting Changes

1. Create a feature branch: `git checkout -b feature/your-feature`
2. Commit your changes: `git commit -m "Add some feature"`
3. Push to branch: `git push origin feature/your-feature`
4. Open a Pull Request

## Code Style

- Use TypeScript where possible
- Follow existing code style in each package
- Add tests for new features
- Update documentation as needed

## Pull Request Process

1. Ensure all tests pass locally
2. Update README.md if needed
3. Reference any related issues
4. Request review from maintainers

## Issues

Before creating an issue, please check if it's already been reported. When creating an issue, please include:

- Clear description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Environment details

## License

By contributing to this project, you agree that your contributions will be licensed under its MIT License.

---

For more details, see individual package READMEs in their respective directories.
