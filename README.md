<div align="center">

<img src="https://raw.githubusercontent.com/365businessdev/ALbuild/main/media/icon.png" alt="ALbuild" width="120" />

# ALbuild

### The easy toolchain for Microsoft Dynamics 365 Business Central AL development.

[![Issues](https://img.shields.io/github/issues/365businessdev/ALbuild)](https://github.com/365businessdev/ALbuild/issues)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Business Central](https://img.shields.io/badge/Dynamics%20365-Business%20Central-da3b8a.svg)](https://learn.microsoft.com/dynamics365/business-central/)

</div>

---

> **This repository is the community hub for ALbuild** — it is where you **report bugs**, **request
> features**, and **ask questions**. The product source code is maintained separately; this repo
> exists to collect and track your feedback across all ALbuild components.

## What is ALbuild?

ALbuild builds, tests and ships Business Central apps **without BcContainerHelper**, with a real
transitive dependency resolver, a built‑in AL test runner, cross‑platform AL Tool compilation, code
signing, NuGet/Universal/local dependency sources, runtime packages, on‑prem & Marketplace release,
and more.

It ships as **three components** — please note which one your issue is about:

| Component | What it is | Where to get it | Issue label |
| --- | --- | --- | --- |
| 🟦 **PowerShell module** | The engine (`businessdev.ALbuild`): containers, artifacts, dependency resolution, compile, sign, test, package, release. | PowerShell Gallery | `ALbuild.powershell` |
| 🟩 **Azure DevOps extension** | Granular pipeline tasks over the module (CI/CD). | Visual Studio Marketplace (Azure DevOps) | `ALbuild.pipeline` |
| 🟧 **VS Code extension** | Developer inner‑loop: pipeline status, BC container management, artifact browsing. | Visual Studio Marketplace (VS Code) | `ALbuild.vscode` |

## Reporting an issue

1. **Search first.** Please check [existing issues](https://github.com/365businessdev/ALbuild/issues?q=is%3Aissue)
   (open *and* closed) to avoid duplicates — add a 👍 or a comment to an existing one instead of
   opening a new report.
2. **Open a new issue** and pick a template:
   - 🐞 [**Bug report**](https://github.com/365businessdev/ALbuild/issues/new?template=bug_report.yml)
   - 💡 [**Feature request**](https://github.com/365businessdev/ALbuild/issues/new?template=feature_request.yml)
   - ❓ Questions & general discussion → [Discussions](https://github.com/365businessdev/ALbuild/discussions)
3. **Choose the component.** Every template asks which component the issue is about — pick
   **ALbuild.powershell**, **ALbuild.vscode** or **ALbuild.pipeline** (or *Not sure*). The matching
   label is applied automatically so issues can be triaged per component.

### What to include
A good report is fast to act on. Please provide:
- **Component & version** (module version, extension version, or pipeline task version).
- **What happened** vs. **what you expected**.
- **Exact, minimal steps to reproduce** (and a sample `albuild.json` / pipeline YAML if relevant).
- **Environment**: OS, PowerShell edition/version (5.1 / 7.x), Docker, and the BC artifact
  version/country in play.
- The **clean error message** ALbuild printed (it surfaces a readable one‑line reason; full detail
  is in the *ALbuild* output channel / pipeline log).

## Labels

Issues are organized with a small, consistent label set:

**Component** (one per issue, auto‑applied from the template):
- `ALbuild.powershell` — the PowerShell module
- `ALbuild.vscode` — the VS Code extension
- `ALbuild.pipeline` — the Azure DevOps extension / pipeline tasks

**Type:** `bug` · `enhancement` · `question` · `documentation`

**Triage/status:** `triage` (new, awaiting review) · `needs-info` (waiting on the reporter) ·
`good first issue` · `wontfix` · `duplicate`

## Roadmap & releases

Planned work is tracked through issues and [milestones](https://github.com/365businessdev/ALbuild/milestones).

## Security

**Please do not report security vulnerabilities in public issues.** Email
**info@365businessdev.com** instead — see [SECURITY.md](.github/SECURITY.md).

## License

The ALbuild components are released under the [MIT License](LICENSE).

<div align="center">

Maintained by **365 business development GmbH**

</div>
