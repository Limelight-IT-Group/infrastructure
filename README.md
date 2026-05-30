# Infrastructure

## Overview
Core infrastructure-as-code, scripts, documentation and lab configurations for Limelight IT Group.

## Purpose
This repository is the single source of truth for Limelight IT Group infrastructure. It holds everything needed to build, document, automate and replicate the technical environment — from lab setups to production-grade scripts and module libraries.

## Architecture
The repository is structured around four core disciplines:

- **docs/** — Architecture decisions, runbooks, standards and reference documentation
- **labs/** — Experimental configurations, homelab setups and proof-of-concept work
- **scripts/** — Operational scripts for deployment, maintenance, monitoring and automation
- **modules/** — Reusable infrastructure modules (Terraform, Ansible, PowerShell, Python)

## Folder Structure
```
infrastructure/
├── docs/          # Architecture decisions, runbooks, standards
├── labs/          # Lab configs, homelab, proof-of-concept
├── scripts/       # Operational and automation scripts
├── modules/       # Reusable infrastructure modules
├── .gitignore     # Python + general project ignores
└── README.md      # This file
```

## Standards
- All scripts must include a header comment describing purpose, author and date
- Secrets must never be committed — use environment variables or a secrets manager
- All modules must include inline documentation
- Branch protection is enforced on `main` — all changes via pull request
- Commit messages follow Conventional Commits: `feat:`, `fix:`, `chore:`, `docs:`

## License
MIT License — Copyright (c) 2026 Limelight IT Group
See [LICENSE](LICENSE) for full terms.
