
# Lab 1 – SQL Security Basics in the Cloud — Lab Guide

## Prereqs
- Cloud account with free-tier managed SQL (RDS/Azure SQL/Cloud SQL)
- CLI installed (aws/az/gcloud) and authenticated
- psql or mysql client

## Steps (High Level)
1. **Provision**: Create a test DB instance (smallest free-tier option).
2. **Configure**: Network allowlist, auth, initial users/roles.
3. **Execute**: Run the SQL and CLI commands in this guide.
4. **Validate**: Capture evidence (screenshots/outputs) to `/evidence`.
5. **Tear down or retain**: Clean-up notes at bottom.

> Replace `{PLACEHOLDER}` values with your actual identifiers.

## Commands (Scaffold)
```bash
# example placeholders
# aws rds describe-db-instances --db-instance-identifier {PLACEHOLDER}
# psql "sslmode=require host={PLACEHOLDER} user={PLACEHOLDER} dbname={PLACEHOLDER}"
```

## Evidence Checklist
- [ ] Screenshot: DB instance details (engine/version, storage encryption)
- [ ] Output: Role/privileges list
- [ ] Log snippet: relevant events
- [ ] Diagram: data flow (client ↔ network ↔ DB)

## Cleanup
Document any resources to delete to avoid charges.
