# My commit & branch rules | Common Patterns 🚀🔥

Using Git effectively is essential for maintaining a clear and organized project history. This document covers commit patterns based on "Conventional Commits," along with some personal preferences and best practices.

---

## ✨ Commit Format

The standard format for commits is:

```bash
!type(?scope): !message
<?body>
<?footer>
```

- `!type` (mandatory): Defines the category of change.
- `?scope` (optional): Provides context for the commit, which can also be the task number (e.g., `feat(112): add login endpoint`).
- `!message` (mandatory): A brief, imperative description of the change.

✅ **Example commits:**

```bash
feat(auth): add support for Google login
feat(112): implement password recovery endpoint
fix(ui): resolve modal bug
```

---

## 📌 Commit Types & Examples

### **🧪 test** - Creating or modifying tests

```bash
test(api): add tests for login endpoint
test(TASK-210): refactor formatting function tests
test(db): mock database connection in test setup
test: increase test coverage for authentication flow
test(routes): validate protected routes without JWT
```

### **✨ feat** - New feature development

```bash
feat(api): create password recovery endpoint
feat: add dark mode toggle
feat(db): implement new indexing for performance
feat(APP-84): enable OAuth login
feat(logging): add structured logs with Winston
```

### **♻️ refactor** - Code refactoring without changing logic

```bash
refactor(utils): optimize parsing function
refactor(db): simplify database schema
refactor(auth): extract JWT validation function
refactor(ui): remove unnecessary components
refactor(api): standardize error responses
```

### **🎨 style** - Code style changes (no functionality impact)

```bash
style(lint): fix indentation and spacing
style(css): apply new global theme
style(prettier): reformat source code
style(FRONT-03): remove unused comments
style(html): adjust indentation in main template
```

### **🐛 fix** - Bug fixes

```bash
fix(BUG-93): resolve JSON parsing issue
fix(ui): fix modal overlapping bug
fix(auth): fix session expiration handling
fix(db): fix intermittent connection error
fix: prevent duplicate log entries
```

### **🛠️ chore** - Project maintenance (no functional impact)

```bash
chore(deps): update project dependencies
chore(lint): configure ESLint rules
chore(docs): add contribution guide
chore: create local startup script
chore(ci): update GitHub Actions workflow
```

### **📚 docs** - Documentation updates

```bash
docs(readme): add API usage example
docs(changelog): document recent changes
docs(api): update OpenAPI specification
docs(contributing): refine PR guidelines
docs(roadmap): add upcoming project goals
```

### **🏗️ build** - Changes affecting the build process

```bash
build(npm): update core dependencies
build(docker): optimize Dockerfile for smaller image
build(ci): adjust pipeline caching
build(webpack): reduce bundle size
build(package): add monitoring package
```

### **⚡ perf** - Performance improvements

```bash
perf(query): optimize SQL query performance
perf(api): reduce response time for endpoints
perf(render): improve rendering efficiency
perf(caching): add caching to heavy routes
perf(loop): replace inefficient loop
```

### **🔁 revert** - Reverting previous commits

```bash
revert(TASK-932): undo change that broke the system
revert: revert incorrect PR merge
revert(black-friday): restore previous Dockerfile version
```

### **🚧 temp** - Temporary commits (debugging, quick tests)

```bash
temp: test new logging configuration
temp: debug caching behavior
temp: validate package version before merging
temp: troubleshoot intermittent API failure
temp: run test with debug flag
```

### **🧪 exp** - Experimental changes

```bash
exp: test alternative authentication system
exp: evaluate new folder structure
exp: analyze GraphQL migration feasibility
exp: experiment with caching API
exp: test alternative PDF library
```

---

## 🚀 Branch Naming Conventions

Companies often use structured branch names integrated with tools like Jira, such as:

```bash
feat/BACK-112-add-authentication
bugfix/FRONT-84-fix-header-bug
fix/FRONT-84
feat/BACK-84
```

💡 I personally prefer using only the task number, making checkouts faster:

```bash
feat/112
chore/TASK-84
feat/BACK-93
```

This allows for quick switching between branches without needing to look up full branch names. ⚡

---

## 🎭 Emoji Commits (Personal Preference)

This is something I use only in personal projects for aesthetics:

| Type                  | Emoji                     |
| --------------------- | ------------------------- |
| Initial commit        | 🎉 "\:tada\:"             |
| Version tag           | 🔖 "\:bookmark\:"         |
| New feature           | ✨ "\:sparkles\:"         |
| Task list             | 🔜 "\:soon\:"             |
| Bugfix                | 🐛 "\:bug\:"              |
| Documentation         | 📚 "\:books\:"            |
| Testing               | 🧪 "\:test_tube\:"        |
| Adding a test         | ✅ "\:white_check_mark\:" |
| Test approval         | ✔️ "\:heavy_check_mark\:" |
| Accessibility         | ♿ "\:wheelchair\:"       |
| Text changes          | 📝 "\:pencil\:"           |
| Package.json updates  | 📦 "\:package\:"          |
| In progress           | 🚧 "\:construction\:"     |
| Config files          | 🔧 "\:wrench\:"           |
| Removing a dependency | ➖ "\:heavy_minus_sign\:  |
| Adding a dependency   | ➕ "\:heavy_plus_sign\:"  |
| Reverting changes     | 💥 "\:boom\:"             |
| Code review changes   | 👌 "\:ok_hand\:"          |
| Refactoring           | ♻️ "\:recycle\:"          |
| Moving/Renaming       | 🚚 "\:truck\:"            |

📌 Full reference: [Gitmoji](https://gitmoji.dev/) 🎭

## Preferred Main Branch Name

I always prefer using `main` instead of `master` as the primary branch name in my repositories.
