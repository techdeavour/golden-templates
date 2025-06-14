# 🏆 Golden Templates

**Secure-by-default, reusable GitHub Actions and workflows — your team's golden path to scalable, production-grade CI/CD pipelines.**

## ✨ Overview

`golden-templates` is a curated collection of opinionated, composable, and secure GitHub workflows and actions. Built to reduce boilerplate and enforce best practices, these templates serve as the **paved road** for development teams looking to move fast **without compromising on quality, compliance, or security**.

Whether you're running CI on a Python project, scanning for secrets, deploying to cloud infrastructure, or building Docker containers — `golden-templates` has you covered.

## 🔧 Features

* ✅ Reusable workflows using `workflow_call`
* 🔁 Composite GitHub Actions to abstract repeated logic
* 🔒 Security-first: Includes license checks, secret scanning, SAST, and more
* 🌐 Language-agnostic: Works across Python, Node.js, Go, and containers
* 🧱 Composable building blocks for IDPs and internal platform teams
* 📦 Versioned, documented, and ready to plug-and-play

## 📁 Repository Structure

    golden-templates/
    ├── workflows/          → Reusable workflows (via `workflow_call`)
    │   ├── python-ci.yml
    │   ├── docker-build.yml
    │   └── secure-deploy.yml
    ├── actions/            → Composite GitHub Actions
    │   ├── setup-python/
    │   │   └── action.yml
    │   └── verify-license/
    │       └── action.yml
    ├── examples/           → Usage examples
    │   └── using-python-ci.yml
    ├── docs/               → Extended documentation
    │   ├── usage.md
    │   └── design-philosophy.md
    └── README.md

## 🚀 Quick Start

**Using a Reusable Workflow**

    jobs:
      ci:
        uses: org/golden-templates/.github/workflows/python-ci.yml@main
        with:
          python-version: '3.11'

**Using a Composite Action**

    steps:
      - uses: actions/checkout@v3
      - uses: org/golden-templates/actions/setup-python@main
        with:
          python-version: '3.11'

💡 Replace `org/` with your GitHub org or user namespace.

## 🔐 Security Best Practices

Workflows in this repo follow DevSecOps principles and include:

* 📦 Dependency scanning (pip-audit, npm audit, etc.)
* 🔑 Secret scanning (trufflehog, gitleaks)
* 📄 License compliance checks
* 🔒 Minimal permissions and scoped tokens

Optional integrations like `Scorecard`, `OSV Scanner`, or `Wiz CLI` can be added per environment.

## 📚 Documentation

* [usage.md](docs/usage.md)
* [design-philosophy.md](docs/design-philosophy.md)
* [contributing.md](docs/contributing.md)

## 🤝 Contributing

We welcome contributions to expand and improve the golden path. Please refer to the [contributing guide](docs/contributing.md) for setup, structure, and standards.

## 🛣️ Why "Golden Templates"?

This project is inspired by the **paved road** or **golden path** approach — where platform and security engineers provide opinionated, pre-approved CI/CD workflows so teams can innovate safely without reinventing infrastructure.

## 📜 License

This repository is licensed under the MIT License.

## 💬 Questions or Ideas?

Feel free to open an issue or start a discussion. Let's build secure, scalable CI/CD for everyone 🚀