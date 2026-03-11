# AGENTS.md — Hospital Admission Records Analysis AI Agent Governance

This file defines the rules, constraints, and boundaries for AI agents (Claude, Copilot, Cursor, etc.)
working in this repository. Any agent reading this file must follow the rules below before taking action.

Last updated: 2026-03-11

---

## Scope

Agents may read any file in this repository to understand the project structure and environment setup.

Agents are allowed to:
- Modify documentation files such as `README.md` and `CHANGELOG.md`
- Modify environment verification scripts such as `setup.sh`
- Suggest improvements to project structure and configuration
- Read files in the `tests/` directory

Agents may **not** modify:
- `AGENTS.md` itself without explicit human instruction
- hidden configuration directories such as `.git/`

Agents should focus only on tasks related to environment setup, documentation, and reproducibility.

---

## Constraints

Agents must follow these rules when proposing or making changes:

- All code must remain compatible with **Python 3.11 or higher**
- Do not add new packages to `requirements.txt` without verification
- Never commit secrets, credentials, or `.env` files
- Follow the existing repository structure
- Do not modify files unrelated to the environment setup or documentation
- Follow clear and descriptive commit messages

---

## Testing Requirements

Before proposing any change as complete, an agent must verify:

1. Run:

```bash
bash setup.sh
```

This must exit successfully without errors.

2. Run:

```bash
python test_environment.py
```

This must print:

```
Environment OK
```

3. Ensure the following files are **not staged for commit**:

- `.venv/`
- `.env`
- `__pycache__/`

If any verification fails, the change should not be considered complete.

---

## Boundaries

The following actions are **strictly prohibited** for AI agents:

- Never read or modify `.env` files or credentials
- Never push commits directly to remote repositories
- Never open Pull Requests automatically
- Never modify grading rubrics, instructions, or evaluation files
- Never delete tracked project files without explicit human confirmation

If a task requires any of the above actions, the agent must stop and request human approval.