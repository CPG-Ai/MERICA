# Contributing to MERICA Trader

Thank you for your interest in contributing to MERICA Trader! This document provides guidelines and instructions for contributing to the project.

## 🚀 Getting Started

1. **Fork the repository** (if you're an external contributor)
2. **Clone your fork**:
   ```bash
   git clone https://github.com/YOUR-USERNAME/MERICA.git
   cd MERICA
   ```
3. **Install dependencies**:
   ```bash
   pnpm install
   ```
4. **Set up your environment**:
   ```bash
   cp apps/web/.env.example apps/web/.env.local
   # Edit .env.local with your credentials
   ```

## 🌿 Branch Naming

Use descriptive branch names following this pattern:
- `feature/description` - New features
- `fix/description` - Bug fixes
- `docs/description` - Documentation updates
- `refactor/description` - Code refactoring
- `test/description` - Adding tests

Examples:
- `feature/stripe-checkout`
- `fix/search-distance-calculation`
- `docs/update-readme`

## 💻 Development Workflow

1. **Create a new branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**:
   - Write clean, readable code
   - Follow the existing code style
   - Add comments where necessary
   - Update documentation if needed

3. **Test your changes**:
   ```bash
   pnpm test              # Run tests
   pnpm type-check        # Check TypeScript types
   pnpm lint              # Check code style
   ```

4. **Commit your changes**:
   ```bash
   git add .
   git commit -m "feat: add stripe checkout flow"
   ```

## 📝 Commit Message Convention

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation changes
- `style:` - Code style changes (formatting, etc.)
- `refactor:` - Code refactoring
- `test:` - Adding or updating tests
- `chore:` - Maintenance tasks

Examples:
```
feat: add zip code search functionality
fix: resolve distance calculation bug
docs: update API documentation
refactor: simplify fee calculation logic
test: add tests for listing creation
chore: update dependencies
```

## 🧪 Testing

- Write tests for new features
- Ensure existing tests pass
- Aim for good test coverage
- Test edge cases

```bash
# Run all tests
pnpm test

# Run tests in watch mode
pnpm test --watch

# Run tests for a specific package
pnpm --filter shared test
```

## 📦 Code Organization

- **apps/web** - Next.js frontend
- **apps/ios** - SwiftUI iOS app
- **packages/functions** - Firebase Cloud Functions
- **packages/shared** - Shared code (models, utils, validators)
- **packages/rules** - Firestore security rules
- **config** - Configuration files

## 🎨 Code Style

- Use TypeScript for all code
- Follow the existing ESLint and Prettier configuration
- Use meaningful variable and function names
- Keep functions small and focused
- Add JSDoc comments for complex functions

## 🔍 Pull Request Process

1. **Push your branch**:
   ```bash
   git push origin feature/your-feature-name
   ```

2. **Create a Pull Request**:
   - Go to the repository on GitHub
   - Click "New Pull Request"
   - Select your branch
   - Fill out the PR template with:
     - Description of changes
     - Related issues (if any)
     - Screenshots (if UI changes)
     - Testing instructions

3. **Address review feedback**:
   - Make requested changes
   - Push updates to your branch
   - Re-request review if needed

4. **Merge**:
   - Once approved, your PR will be merged
   - Delete your feature branch after merge

## 🐛 Bug Reports

When reporting bugs, please include:
- Clear description of the issue
- Steps to reproduce
- Expected behavior
- Actual behavior
- Screenshots (if applicable)
- Environment details (OS, browser, Node version)

## 💡 Feature Requests

When suggesting features:
- Explain the problem you're trying to solve
- Describe your proposed solution
- Consider alternative solutions
- Explain why this benefits the project

## 📚 Documentation

- Update README.md for major changes
- Add JSDoc comments for new functions
- Update PROJECT_STRUCTURE.md if adding new files/folders
- Keep inline comments up to date

## ❓ Questions?

If you have questions:
- Check existing documentation
- Search closed issues
- Ask in a new issue with the "question" label

## 📄 License

By contributing, you agree that your contributions will be licensed under the same license as the project (Proprietary).

---

Thank you for contributing to MERICA Trader! 🎉
