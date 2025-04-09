# CI Cheks PoC with TypeScript, Commitlint, and Semantic Release

This is a super simple proof-of-concept repository to demonstrate a basic CI pipeline using:

- [TypeScript](https://www.typescriptlang.org/)
- [Commitlint](https://commitlint.js.org/#/) (for enforcing Conventional Commits)
- [Semantic Release](https://github.com/semantic-release/semantic-release) (for automated versioning and changelogs)
- [GitHub Actions](https://docs.github.com/en/actions) (for workflow automation)

---

## 📁 Project Structure

- `index.ts`: Minimal TypeScript entry point
- `.github/workflows/`: CI/CD automation
- `.commitlintrc.yml`: Commitlint config
- `tsconfig.json`: TypeScript settings

---

## 🚀 Getting Started

This project uses [**fnm**](https://github.com/Schniz/fnm) for Node.js version management via the `.node-version` file.

```bash
# Make sure you're using right node version
fnm use

# Install dependencies
npm install

# Run the app
npm start

```

## 📦 Commit Message Format

This repo uses Conventional Commits, enforced by Commitlint and Husky.

### ✅ Valid Examples

```bash
git commit -m "feat: add login support"
git commit -m "fix(auth): correct token expiration"
```

### ❌ Invalid Example

```bash
git commit -m "foo: this will fail"
```

## 📝 Why PR Titles Matter

GitHub now uses **pull request titles** as the default commit message when using **Squash and Merge**:

> “When squash merging a pull request, the default commit message is now the pull request title.”  
> 🔗 [GitHub Changelog – Default to PR titles for squash merge commit messages](https://github.blog/changelog/2022-05-11-default-to-pr-titles-for-squash-merge-commit-messages/)

This is why this project:

- Enforces [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) for PR titles
- Uses a GitHub Action to auto-format PR titles if needed
- Uses [`semantic-release`](https://github.com/semantic-release/semantic-release) to automate changelogs and versioning

✅ Having properly formatted PR titles = clean git history + automated releases!
