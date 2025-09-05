
# SQL for Cloud Security Architects — Week 1

This repository contains **Week 1** labs focused on securing SQL in cloud environments (AWS RDS, Azure SQL Database, GCP Cloud SQL). Each lab is designed for **everyday security operations**—audits, monitoring, and patching—plus **offense‑informed defense**.

## Labs (Week 1)
- **Lab 1 – SQL Security Basics in the Cloud** (`labs/lab01_sql_security_basics/`)
- **Lab 2 – SQL Injection Simulation & Mitigation** (`labs/lab02_sql_injection_patch/`)
- **Lab 3 – Audit & Logging** (`labs/lab03_audit_logs/`)
- **Lab 4 – Encryption in Transit & At Rest** (`labs/lab04_sql_encryption/`)
- **Lab 5 – Security Patching & Compliance** (`labs/lab05_patching_compliance/`)

> Each lab ships with: `README.md` (context), `lab_guide.md` (step‑by‑step), `security_patch_notes.md`, `interview_qna.md`, `src/` (code), `diagrams/`.

## How to use
1. Open a new GitHub repo and upload these contents.
2. Fill in the placeholders as you complete each lab.
3. Commit often; push screenshots/outputs to `evidence/` folders in each lab.

## Cloud Targets
- AWS RDS (MySQL/PostgreSQL), Azure SQL Database, GCP Cloud SQL

## Badges
![Status](https://img.shields.io/badge/Week-1-blue)
![Focus](https://img.shields.io/badge/Focus-SQL%20Security-success)
![Cloud](https://img.shields.io/badge/Cloud-AWS%2FAzure%2FGCP-lightgrey)

## Structure
```
.
├── README.md
├── LICENSE
├── .gitignore
├── .github/
│   ├── ISSUE_TEMPLATE/bug_report.md
│   ├── ISSUE_TEMPLATE/feature_request.md
│   └── workflows/markdown.yml
└── labs/
    ├── lab01_sql_security_basics/
    ├── lab02_sql_injection_patch/
    ├── lab03_audit_logs/
    ├── lab04_sql_encryption/
    └── lab05_patching_compliance/
```

## Contribution Guide
- Use feature branches: `feat/lab02-mitigation`, `docs/readme-tweaks`.
- Pull Request template prompts you for lab evidence and security impact.
- Keep secrets out of the repo. Use `example.env` files when needed.

## License
MIT
