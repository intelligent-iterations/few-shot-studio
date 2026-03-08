# Contributing to Few-Shot Studio

Thank you for your interest in contributing! This guide will help you get started.

## Development Setup

```bash
# Prerequisites: Node.js 22+, pnpm
node --version  # v22.x.x
pnpm --version  # 10.x.x

# Clone and install
git clone https://github.com/intelligent-iterations/few-shot-studio.git
cd few-shot-studio
pnpm install

# Verify everything works
pnpm check
pnpm lint
pnpm test
pnpm build
```

## Development Workflow

1. Fork the repository and create a feature branch from `main`
2. Make your changes
3. Ensure all checks pass: `pnpm check && pnpm lint && pnpm test && pnpm build`
4. Commit using [Conventional Commits](#commit-messages)
5. Open a pull request against `main`

## Commit Messages

This project uses [Conventional Commits](https://www.conventionalcommits.org/) enforced by commitlint. Format:

```
type(scope): description

[optional body]
```

**Types:** `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`

Examples:

- `feat: add prompt template builder`
- `fix: handle empty example arrays`
- `docs: update API reference`

## Code Style

- **TypeScript** — strict mode, no `any`
- **ESLint** — flat config with strict type-checked rules
- **Prettier** — auto-formatted on commit via lint-staged

The pre-commit hook runs lint-staged automatically. If you need to bypass it (not recommended): `git commit --no-verify`

## Testing

Tests use [Vitest](https://vitest.dev/) and are colocated with source files as `*.test.ts`.

```bash
pnpm test          # Run once
pnpm test:watch    # Watch mode
pnpm test:coverage # With coverage report
```

## Pull Requests

- Keep PRs focused — one feature or fix per PR
- Include tests for new functionality
- Update documentation if behavior changes
- All CI checks must pass

## License

By contributing, you agree that your contributions will be licensed under the [Apache License 2.0](LICENSE).
