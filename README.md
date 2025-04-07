# CI Cheks PoC with TypeScript, MegaLinter, Commitlint, and Semantic Release

This is a super simple proof-of-concept repository to demonstrate a basic CI pipeline using:

- ✅ [TypeScript](https://www.typescriptlang.org/)
- ✅ [MegaLinter](https://github.com/oxsecurity/megalinter) (for code quality)
- ✅ [Commitlint](https://commitlint.js.org/#/) (for enforcing Conventional Commits)
- ✅ [Semantic Release](https://github.com/semantic-release/semantic-release) (for automated versioning and changelogs)
- ✅ [GitHub Actions](https://docs.github.com/en/actions) (for workflow automation)

---

## 📁 Project Structure

- `index.ts`: Minimal TypeScript entry point
- `.github/workflows/`: CI/CD automation
- `.commitlintrc.yml`: Commitlint config
- `.mega-linter.yml`: MegaLinter config
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

## 🧪 Linting & CI

MegaLinter and tsc --noEmit are used during CI to ensure code quality and type correctness.

```bash
# Run MegaLinter locally (optional)
npx mega-linter-runner
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