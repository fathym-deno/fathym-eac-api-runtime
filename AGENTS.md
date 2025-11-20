---
FrontmatterVersion: 1
DocumentType: Guide
Title: Fathym EaC API Runtime Agents Guide
Summary: Guardrails for collaborating on the Fathym Everything-as-Code API runtime.
Created: 2025-11-20
Updated: 2025-11-20
Owners:
  - fathym
References:
  - Label: Project README
    Path: ./README.md
  - Label: Project GUIDE
    Path: ./GUIDE.md
  - Label: EaC Sub-Area README
    Path: ../README.md
  - Label: EaC Sub-Area AGENTS
    Path: ../AGENTS.md
  - Label: EaC Sub-Area GUIDE
    Path: ../GUIDE.md
  - Label: Projects AGENTS
    Path: ../../AGENTS.md
  - Label: Workspace AGENTS
    Path: ../../../AGENTS.md
---

# AGENTS: Fathym EaC API Runtime

Guardrails for humans and AI collaborating on the EaC API runtime.

## Core Guardrails

1. **Stay scoped.** Keep work under `projects/everything-as-code/fathym-eac-api-runtime/` unless coordinating with another pod; link cross-pod dependencies explicitly.
2. **Frontmatter required.** All docs include frontmatter and relative references back to parent guides.
3. **API stability.** Avoid breaking API contracts silently; document breaking changes and add migration notes for known consumers.
4. **Provenance.** Capture upstream sources, release channels, and version pins in `UPSTREAM.md` when publishing; prefer upstream-first fixes before diverging.
5. **Security & data handling.** Do not embed secrets or tenant data; document required env vars for Docker and local dev.

## Communication

- Declare intent before editing; summarize outcomes and next steps in the project README or a short log.
- Notify dependent runtimes (steward, applications, products) when behavior changes to keep dependencies aligned.
