# Contributing to Tutera

Thanks for your interest in contributing to Tutera! This document provides **organization-wide contributing guidelines** that apply across repositories in the Tutera GitHub organization, including (but not limited to) `tutera-frontend` and `tutera-backend`.

Each repository may extend or override these guidelines with additional project-specific instructions. Always check the repository’s own `README.md` and `CONTRIBUTING.md` first.

---

## Ways to contribute

There are many ways to help:

- **Bug reports** – help us improve quality by reporting problems
- **Feature requests** – suggest new capabilities or enhancements
- **Documentation** – fix typos, clarify instructions, or add missing docs
- **Code contributions** – fix bugs, implement features, or improve tests
- **Feedback** – share your experience using Tutera and where it can improve

---

## Getting started

1. **Find or open an issue**
   - Search the repository’s issue tracker to see if your bug or feature request already exists.
   - If not, open a new issue using the appropriate template (bug report, feature request, etc.).
2. **Discuss and align**
   - For non-trivial changes, discuss your proposal in the issue before starting significant work. This reduces the risk of spending time on an approach that may not be accepted.
3. **Fork and clone**
   - Fork the repository on GitHub, then clone your fork locally.
4. **Create a branch**
   - Use a descriptive branch name such as `feature/improve-onboarding`, `fix/login-timeout`, or `chore/update-deps`.

---

## Development workflow (general)

> Refer to each repository’s `README.md` for exact commands. The following is a common pattern.

1. Install dependencies as described in the repository’s documentation.
2. Make your changes in small, logically coherent commits.
3. Run tests, linters, and any formatting tools locally before opening a pull request.
4. Update or add documentation and tests as needed.
5. Push your branch to your fork.
6. Open a pull request against the appropriate branch (typically `main`) of the upstream repository.

---

## Pull request guidelines

- **Keep PRs focused**
  - A PR should address a single issue or a closely related set of changes.
  - Avoid mixing refactors, new features, and unrelated fixes in the same PR.

- **Describe your changes clearly**
  - Fill out the pull request template, including:
    - What problem the PR addresses
    - How it solves the problem
    - Any trade-offs or notable design decisions
    - Testing performed and how to reproduce

- **Stay up to date**
  - Rebase or merge from the target branch (often `main`) regularly to minimize conflicts.

- **Add tests where appropriate**
  - For bug fixes, add regression tests where possible.
  - For new features, add unit and/or integration tests that verify expected behavior.

- **Follow style guidelines**
  - Respect the repository’s existing style, formatting, and conventions.
  - Run linters and formatters before pushing.

---

## Code of Conduct

By participating in this project, you agree to abide by the [Tutera Code of Conduct](./CODE_OF_CONDUCT.md). Please report unacceptable behavior to the maintainers as described there.

---

## Commit messages

Readable history is important. Aim for commit messages that:

- Use the imperative mood (e.g. "Fix login timeout" instead of "Fixed login timeout")
- Briefly explain **what** changed and, when helpful, **why**
- Reference related issues, e.g. `Fixes #123` or `Refs #456`

---

## Review process

1. A maintainer or reviewer will be assigned to your PR.
2. They may ask clarifying questions or request changes.
3. Address feedback by pushing additional commits to the same branch.
4. Once the PR is approved and all required checks pass, a maintainer will merge it using the repository’s preferred strategy (e.g. squash merge or rebase).

Reviews are a collaboration, not an exam—ask questions and propose alternatives if you disagree with a suggestion.

---

## License

By contributing to a Tutera repository, you agree that your contributions will be licensed under that repository’s license as specified in its `LICENSE` file.

If you have questions about licensing or how your contribution will be used, please open an issue before submitting a pull request.