# 🧪 Repo Test - CI/CD & Integration Test Framework

[![Demo Workflow with Single Parameter](https://github.com/IntegrationtestThanhlv/repo-test/actions/workflows/demo-params.yml/badge.svg)](https://github.com/IntegrationtestThanhlv/repo-test/actions/workflows/demo-params.yml)
![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![GitHub repo size](https://img.shields.io/github/repo-size/IntegrationtestThanhlv/repo-test)

This repository serves as a standardized demo and template for **GitHub Actions CI/CD workflows** with parameter inputs and automated integration testing configuration.

---

## 📁 Repository Structure

```text
.
├── .github/
│   └── workflows/
│       └── demo-params.yml   # GitHub Actions workflow with single input parameter
├── .gitignore                # Git ignore rules for OS and IDE files
├── testfile.txt              # Standardized test suites, mock data & environment configs
└── README.md                 # Project documentation
```

---

## 🚀 GitHub Actions Workflow

The repository includes a production-ready GitHub Action workflow located at [`.github/workflows/demo-params.yml`](.github/workflows/demo-params.yml).

### Features
- **Manual Trigger (`workflow_dispatch`)**: Trigger the pipeline on-demand with custom input parameters.
- **Push Trigger (`push`)**: Automatically executes on pushes to the `main` branch with default fallback values.
- **Rich Step Summary**: Automatically produces a formatted Markdown execution summary in the GitHub Actions UI.

### Workflow Input Parameter

| Parameter | Type | Options | Default | Description |
|:---|:---|:---|:---|:---|
| `environment` | `choice` | `development`, `staging`, `production` | `staging` | Target deployment environment |

### How to Run the Workflow

#### Option 1: Via GitHub Web Interface
1. Go to the **[Actions](https://github.com/IntegrationtestThanhlv/repo-test/actions)** tab.
2. Select **Demo Workflow with Single Parameter** from the left sidebar.
3. Click the **Run workflow** dropdown on the right.
4. Select your desired **Target deployment environment** (`development`, `staging`, or `production`).
5. Click **Run workflow**.

#### Option 2: Via GitHub CLI (`gh`)
```bash
# Run with default environment (staging)
gh workflow run demo-params.yml

# Run with specific environment
gh workflow run demo-params.yml -f environment=production
```

---

## ⚙️ Configuration & Test Context

The repository includes [`testfile.txt`](testfile.txt), providing standardized context for integration tests, including:
- **Project Metadata**: Repository details, default timezone, and encoding.
- **Environment Matrix**: Specific endpoints, timeouts, and logging levels for `development`, `staging`, and `production`.
- **Test Suite Definitions**: Pre-defined test suites for smoke tests, authentication validation, data ingestion, and latency benchmarks.
- **Mock Data & Payloads**: Sample user profiles and JSON test payloads.

---

## 👤 Maintainer

- **Repository**: [IntegrationtestThanhlv/repo-test](https://github.com/IntegrationtestThanhlv/repo-test)
- **Author**: `IntegrationtestThanhlv`
