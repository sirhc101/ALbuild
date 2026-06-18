# Pipeline templates

Ready-to-use Azure DevOps pipeline templates so a new Business Central repository can adopt
ALbuild by changing only a handful of parameters.

- **`yaml/`** — parameterised YAML pipeline templates (consumed via `extends`/`template`):
  - `ci-pipeline.yml` — **with container**: artifact → stamp version → create container → install
    test toolkit → resolve dependencies → check translations → compile → sign → publish/install →
    test → publish results → remove container → publish artifact. Versioning, dependency resolution
    and signing are toggled by parameters.
  - `altool-pipeline.yml` — **no container**: optionally stamp version and resolve dependencies, then
    compile with the cross-platform AL tool only (fast PR/compile validation on a hosted agent).
  - `runtimepackage-pipeline.yml` — batched/parallel/incremental runtime-package engine (one stage
    per platform version) via the `BuildRuntimePackages` task.
  - `release-pipeline.yml` — NuGet publish plus optional per-tenant-extension and on-prem release.
  - `marketplace-release.yml` — AppSource/Marketplace submission and promotion via `SubmitMarketplace`.
- **`release-json/`** — importable classic Release Definition JSON templates (AppSource), modelled
  on the granular flow: authenticate → find product → create submission → wait for validation →
  promote, calling `Submit-BcMarketplaceApp`.

> The container CI template requires the ALbuild Azure DevOps extension (granular tasks) and a
> DevOps agent with Docker.
