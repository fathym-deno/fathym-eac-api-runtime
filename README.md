---
FrontmatterVersion: 1
DocumentType: Guide
Title: Fathym EaC API Runtime
Summary: API runtime for Fathym Everything-as-Code services and integrations.
Created: 2025-11-20
Updated: 2025-11-20
Owners:
  - fathym
References:
  - Label: EaC Sub-Area README
    Path: ../README.md
  - Label: EaC Sub-Area AGENTS
    Path: ../AGENTS.md
  - Label: EaC Sub-Area GUIDE
    Path: ../GUIDE.md
  - Label: Projects README
    Path: ../../README.md
  - Label: Projects AGENTS
    Path: ../../AGENTS.md
  - Label: Projects GUIDE
    Path: ../../GUIDE.md
  - Label: Workspace README
    Path: ../../../README.md
  - Label: Workspace AGENTS
    Path: ../../../AGENTS.md
  - Label: Workspace GUIDE
    Path: ../../../WORKSPACE_GUIDE.md
  - Label: Project AGENTS Guide
    Path: ./AGENTS.md
  - Label: Project GUIDE
    Path: ./GUIDE.md
---

# Fathym EaC API Runtime

API runtime for Everything-as-Code services and integrations, built on Deno with EaC libraries and runtime plugins.

- **Goal:** expose stable EaC APIs for applications, steward flows, and downstream runtimes.
- **Outputs:** API routes/handlers, runtime plugins/configs, and deployment assets (incl. Docker).
- **Code location:** this folder hosts the source.

## Current Status

- Tasks: `deno task dev`, `check`, `test`, `build`, `build:docker`, `refresh:docker`, `deploy`, `publish:check`, `version`.
- Dependencies: `@fathym/eac`, `@fathym/eac-applications`, `@fathym/common`, `@fathym/ioc`, Preact.
- Docker networking: `eac-runtimes`; uses `.env.docker` and KV volume mounts in sample tasks.

## How to Work in This Pod

1. Read parent EaC docs and this project’s `AGENTS` and `GUIDE`.
2. Declare intent before editing; summarize outcomes and open questions in a short log or this README.
3. Update `.env*` samples for new configuration; keep secrets out of the repo.
4. Capture provenance/release channels in `UPSTREAM.md` when publishing (jsr/npm/Docker).
5. Note downstream impacts to steward runtimes or consumers when API contracts change.
