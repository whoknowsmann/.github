# Contributing to whoknowsmann Projects

Conventions and standards for all repositories in this org.

---

## Repository Naming

- **Use `lowercase-kebab-case`** — e.g., `gba-engine`, `molt-tamagotchi`
- **Be descriptive** — the name should hint at what the project does
- **Avoid generic names** — `utils`, `misc`, `stuff` tell you nothing

---

## README Structure

Every repo should have a `README.md` with the following sections (in order):

```markdown
# Project Name

One-line description of what this project does.

## Features
- Key feature 1
- Key feature 2

## Requirements
List dependencies, toolchains, or system requirements.

## Quick Start
Step-by-step to get running as fast as possible.

## Usage
More detailed usage examples and options.

## Project Structure (optional)
Brief overview of folder layout, or link to docs/ARCHITECTURE.md.

## Contributing
Link to this file or inline contribution notes.

## License
State the license (e.g., MIT, Apache 2.0, proprietary).
```

### Section Guidelines

| Section | Required | Notes |
|---------|----------|-------|
| Title + one-liner | ✅ | First thing people see |
| Features | ✅ | Bullet list, keep it scannable |
| Requirements | ✅ | What do I need before I start? |
| Quick Start | ✅ | 3-5 steps max to get running |
| Usage | ✅ | Examples, CLI flags, API overview |
| Project Structure | Optional | For larger projects |
| Contributing | ✅ | Link here or brief inline |
| License | ✅ | State it explicitly |

### Optional Additions

- **Badges** — build status, version, license (top of README)
- **Screenshots/GIFs** — for visual projects
- **Troubleshooting** — common issues and fixes
- **Acknowledgments** — credits for dependencies or inspiration

---

## Folder Structure

Adapt based on project type, but prefer this general layout:

```
├── src/              # Source code
├── tests/            # Test files
├── docs/             # Documentation (ARCHITECTURE.md, API.md, etc.)
├── scripts/          # Build/utility scripts
├── assets/           # Images, data files, etc.
├── .github/          # GitHub-specific (workflows, issue templates)
│   └── workflows/    # CI/CD actions
├── README.md
├── LICENSE
├── CHANGELOG.md      # For versioned projects
└── .gitignore
```

### Language-Specific Conventions

**Python:**
```
├── src/project_name/  # or just project_name/
├── tests/
├── requirements.txt   # or pyproject.toml
└── setup.py          # if distributing
```

**C/C++ (GBA/embedded):**
```
├── src/
├── include/          # Headers
├── third_party/      # External dependencies
├── tools/            # Build tools, converters
├── Makefile
└── DEPENDENCIES.md   # Document external deps
```

**Node.js:**
```
├── src/
├── tests/
├── package.json
└── tsconfig.json     # if TypeScript
```

---

## Branch Naming

| Branch | Purpose |
|--------|---------|
| `main` | Production-ready code |
| `develop` | Integration branch (optional) |
| `feature/<name>` | New features — e.g., `feature/add-multiplayer` |
| `fix/<name>` | Bug fixes — e.g., `fix/memory-leak` |
| `hotfix/<name>` | Urgent production fixes |
| `docs/<name>` | Documentation updates |
| `refactor/<name>` | Code cleanup, no behavior change |

---

## Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

### Types

| Type | When to use |
|------|-------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `style` | Formatting, no logic change |
| `refactor` | Code change, no feature/fix |
| `test` | Adding or updating tests |
| `chore` | Build, tooling, dependencies |

### Examples

```
feat(map): add fog of war system
fix(render): prevent crash on empty tileset
docs(readme): add troubleshooting section
chore(deps): bump butano to v18.5.0
refactor(ai): simplify pathfinding logic
```

### Rules

- **Use imperative mood** — "add feature" not "added feature"
- **Keep first line under 72 characters**
- **Reference issues** — `fix(auth): handle null token (closes #42)`

---

## Pull Requests

1. **Branch from `main`** (or `develop` if the repo uses it)
2. **One PR = one concern** — don't mix unrelated changes
3. **Write a clear description** — what changed and why
4. **Link related issues** — `Closes #123` or `Related to #456`
5. **Keep it reviewable** — under 400 lines if possible

### PR Title Format

Follow the same convention as commits:
```
feat(scope): add new thing
fix(scope): resolve bug
```

---

## Code Style

- **Follow existing patterns** — match the style of the codebase
- **Use formatters** — prettier, black, clang-format, etc.
- **No trailing whitespace**
- **End files with a newline**

Language-specific linters/formatters are noted in each repo's README or config files.

---

## Documentation

- **Update docs with code** — if you change behavior, update the README
- **Use Markdown** — consistent formatting across all docs
- **Link, don't duplicate** — reference other docs instead of copying

---

## Issues

When opening an issue:

- **Bug reports**: Include steps to reproduce, expected vs actual behavior, environment details
- **Feature requests**: Describe the use case, not just the solution
- **Questions**: Check existing issues/docs first

---

## License

Unless otherwise specified, projects are released under the license stated in their `LICENSE` file. Contributions are assumed to be under the same license.

---

## Questions?

Open an issue.
