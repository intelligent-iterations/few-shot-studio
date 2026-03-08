# Few-Shot Studio

**Type:** Open-source library (Apache 2.0)
**Repo:** `https://github.com/intelligent-iterations/few-shot-studio`

---

## Public Repository Safety

This is a **public, open-source repository**. Every file, commit message, and piece of code is visible to the world.

**NEVER include:**

- Internal infrastructure details (hostnames, IPs, account names)
- Secrets, tokens, API keys, or credentials
- References to private repositories or internal tools
- References to internal team processes or private services
- Personally identifiable information

**Before every commit, verify:**

- `grep -ri` for any internal references returns nothing
- No `.env` files or credential files are staged
- Commit messages contain no private information

---

## Development

```bash
pnpm install
pnpm check    # Type-check
pnpm lint     # ESLint
pnpm test     # Vitest
pnpm build    # Compile TypeScript
```

## Conventions

- **TypeScript** — strict mode, ES2023 target, NodeNext modules
- **Tests** — colocated `*.test.ts` files, Vitest, 80% coverage threshold
- **Commits** — Conventional Commits (enforced by commitlint)
- **Lint** — ESLint flat config + Prettier, auto-fixed on commit via lint-staged
- **CI** — 4 parallel jobs: lint, typecheck, test, build
