---
FrontmatterVersion: 1
DocumentType: Guide
Title: Fathym EaC API Runtime Guide
Summary: Playbook for developing and releasing the Fathym Everything-as-Code API runtime.
Created: 2025-11-20
Updated: 2025-11-20
Owners:
  - fathym
References:
  - Label: Project README
    Path: ./README.md
  - Label: Project AGENTS Guide
    Path: ./AGENTS.md
  - Label: EaC Apps Area README
    Path: ../README.md
  - Label: EaC Apps Area GUIDE
    Path: ../GUIDE.md
  - Label: Workspace GUIDE
    Path: ../../../WORKSPACE_GUIDE.md
---

# Fathym EaC API Runtime Guide

## Workflow

1. Align scope in `README.md`: note intended change (endpoint/contract update, feature/fix, release prep) and affected consumers.
2. Develop handlers/plugins/config with compatibility in mind; keep API docs current.
3. Validate with `deno task check`, `deno task test`, and `deno task build`; for Docker flows use `deno task build:docker`, `refresh:docker`, and `deploy:docker` as needed.
4. Update `.env*` samples when adding env vars; keep secrets out of the repo; note Docker network/volumes (`eac-runtimes`, KV mounts).
5. Record provenance and version pins in `UPSTREAM.md` when publishing (jsr/npm/Docker) and communicate breaking changes to consumers.

## Verification

- Tests/lint/fmt pass; links relative; single-line paragraphs maintained.
- API changes documented with migration notes; downstream impacts called out. EOF
