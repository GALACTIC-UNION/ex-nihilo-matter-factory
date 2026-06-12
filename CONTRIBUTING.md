# Contributing to ex-nihilo-matter-factory

Thank you for contributing to the **OMNISCIENT CIVILIZATION NEXUS (OCN)** — SINGULARITY-CATALYST domain.

## Code of Conduct

All contributors must follow the [OCN Code of Conduct](https://github.com/GALACTIC-UNION/.github/blob/main/CODE_OF_CONDUCT.md). In summary: be respectful, collaborative, and safety-conscious.

## Reporting Issues

- Use GitHub Issues with a clear title and description
- Include steps to reproduce, expected vs. actual behavior, and environment details
- Tag safety-critical issues with the **`[SAFETY]`** label — these receive priority review

## Submitting Changes

1. **Fork** the repository and clone your fork
2. **Branch** from `main`: `git checkout -b feat/your-feature-name`
3. **Write tests** covering all new logic
4. **Verify** all tests pass: `pytest tests/`
5. **Commit** using [Conventional Commits](https://www.conventionalcommits.org/):
   - `feat:` new feature
   - `fix:` bug fix
   - `docs:` documentation only
   - `test:` test additions/changes
   - `chore:` tooling/config

6. **Open a Pull Request** against `main` with a clear description

## Pull Request Checklist

- [ ] Tests added or updated for all changes
- [ ] Documentation updated to reflect changes
- [ ] CI checks passing (green)
- [ ] At least **1 approval** for general changes
- [ ] At least **2 approvals** for any `[SAFETY]`-tagged change
- [ ] No regression in test coverage

## Development Setup

```bash
git clone https://github.com/GALACTIC-UNION/ex-nihilo-matter-factory.git
cd ex-nihilo-matter-factory
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements-dev.txt
pytest tests/ -v
```

## Branch Strategy

| Branch | Purpose |
|--------|---------|
| `main` | Stable, protected, CI-gated |
| `develop` | Integration staging |
| `feat/*` | Feature development |
| `fix/*` | Bug fixes |
| `docs/*` | Documentation-only changes |

## Security Disclosures

**Do not open public GitHub Issues for security vulnerabilities.** Email `security@galactic-union.org` with full details. You will receive acknowledgment within 48 hours.

---
*OMNISCIENT CIVILIZATION NEXUS (OCN) · SINGULARITY-CATALYST domain · [GALACTIC-UNION](https://github.com/GALACTIC-UNION)*
