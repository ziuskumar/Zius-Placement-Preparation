# CI/CD

## 📖 Introduction

CI/CD is a modern DevOps practice that automates the process of building, testing, and deploying applications. It helps developers release software faster, more reliably, and with fewer manual errors.

---

# Definition

### Continuous Integration (CI)

Continuous Integration is the practice of automatically building and testing code whenever developers push changes to a shared repository.

### Continuous Delivery (CD)

Continuous Delivery automatically prepares the application for deployment, but deployment to production requires manual approval.

### Continuous Deployment

Continuous Deployment automatically deploys every successful change to production without manual intervention.

---

# Why it Exists

- 🚀 Faster software releases
- 🐞 Detect bugs early
- 🤝 Better collaboration among developers
- 🔄 Consistent deployments
- ⚡ Reduce manual work
- 📈 Improve software quality

---

# Working

1. Developer writes code.
2. Pushes code to GitHub.
3. CI pipeline starts automatically.
4. Code is built.
5. Automated tests run.
6. If tests pass, CD pipeline starts.
7. Application is deployed.

---

# Examples

## Git Push

```bash
git add .
git commit -m "Add login feature"
git push origin main
```

Example GitHub Actions workflow:

```yaml
name: CI Pipeline

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4

      - name: Install Dependencies
        run: npm install

      - name: Run Tests
        run: npm test
```

---

# Output

```
✔ Repository Checked Out

✔ Dependencies Installed

✔ Tests Passed

✔ Build Successful

✔ Deployment Successful
```

---

# Explanation

Whenever code is pushed:

- GitHub detects the push.
- CI server builds the project.
- Tests are executed.
- If all tests pass, deployment begins.
- Users receive the latest version.

---

# Diagram (ASCII)

```
Developer
    │
    ▼
Git Push
    │
    ▼
GitHub Repository
    │
    ▼
CI Pipeline
(Build + Test)
    │
    ▼
CD Pipeline
(Deploy)
    │
    ▼
Production
```

---

# Real-world Example

Netflix developers push code hundreds of times every day.

Every push automatically:

- Builds the application
- Runs thousands of automated tests
- Deploys new versions safely

No manual deployment is required.

---

# CI vs CD

| CI | CD |
|----|----|
| Continuous Integration | Continuous Delivery / Deployment |
| Builds code | Deploys code |
| Runs tests | Releases application |
| Finds bugs early | Makes releases faster |

---

# Popular CI/CD Tools

- GitHub Actions
- Jenkins
- GitLab CI/CD
- CircleCI
- Azure DevOps
- Travis CI

---

# Interview Keywords

- CI
- CD
- Pipeline
- Build Automation
- Deployment
- GitHub Actions
- Jenkins
- Docker
- Kubernetes
- Automated Testing

---

# Common Mistakes

❌ Skipping automated tests

❌ Deploying manually every time

❌ Large commits instead of small frequent commits

❌ Ignoring failed pipelines

---

# Interview Traps

### Q1. Difference between Continuous Delivery and Continuous Deployment?

Continuous Delivery requires manual approval before deployment.

Continuous Deployment deploys automatically after successful testing.

---

### Q2. Why is CI important?

Because it catches bugs early and ensures new code doesn't break existing functionality.

---

### Q3. Name popular CI/CD tools.

- GitHub Actions
- Jenkins
- GitLab CI/CD
- CircleCI
- Azure DevOps

---

# Quick Revision

✅ CI = Build + Test

✅ CD = Deliver / Deploy

✅ Every Git Push triggers the pipeline

✅ Build → Test → Deploy

✅ Faster releases

✅ Less manual work

✅ Popular Tools:
- GitHub Actions
- Jenkins
- GitLab CI/CD
- CircleCI

---

# 🧠 Memory Trick

```
CI = Code In

CD = Code Delivered
```

Remember the flow:

```
Code
 ↓
Build
 ↓
Test
 ↓
Deploy
```