# Infrastructure

> Limelight IT Group — Core Infrastructure Repository

## Overview

This repository contains the infrastructure-as-code, documentation, scripts, and reusable modules that underpin Limelight IT's technical operations. It serves as the single source of truth for environment configuration, deployment standards, and operational tooling.

## Purpose

- Standardise infrastructure provisioning across all Limelight IT environments
- Provide reusable, version-controlled modules for common infrastructure patterns
- Document architecture decisions and operational runbooks
- Support repeatable, auditable deployments for client engagements

## Architecture

Limelight IT operates a lean, cloud-first architecture designed for SMB scale with enterprise-grade security principles:

- **Identity & Access** — Microsoft Entra ID (Azure AD) with Conditional Access and MFA enforced
- **Endpoint Management** — Microsoft Intune for device compliance and configuration
- **Productivity** — Microsoft 365 Business Premium (Exchange Online, SharePoint, Teams)
- **Security** — Defender for Business, Cyber Essentials alignment
- **Automation** — Python-based scripts and PowerShell modules for repeatable tasks
- **Monitoring** — Logging and alerting via Microsoft Sentinel (roadmap)

## Folder Structure

```
infrastructure/
├── docs/          # Architecture decision records, runbooks, standards
├── labs/          # Experimental configs, proof-of-concept work
├── modules/       # Reusable infrastructure modules (Terraform, Ansible, PS)
└── scripts/       # Operational scripts — deployment, maintenance, automation
```

## Standards

- All scripts must include a header comment block: purpose, author, date, version
- Secrets must never be committed — use `.env` files or a secrets manager
- All production changes require a pull request with at least one review
- Branch naming convention: `feature/`, `fix/`, `docs/`, `lab/`
- Commit messages follow Conventional Commits (`feat:`, `fix:`, `docs:`, `chore:`)
- Python: PEP 8 compliant, type hints encouraged, docstrings required on functions
- PowerShell: verb-noun naming, approved verbs only, comment-based help required

## License

MIT License — Copyright (c) 2026 Limelight IT Group

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files, to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, subject to the following conditions: The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED.