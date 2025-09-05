# Lab 01 – SQL Injection: Exploit to Defense (AWS/Azure)

## Goal
Experience the full lifecycle: detect a SQLi, block with WAF, fix in code, harden IAM/network, and wire logs to SIEM with automated response.

## Prereqs
- Cloud free tier (AWS or Azure), CLI configured
- Sample vulnerable app (DVWA/Mutillidae or simple Node/Flask app with a vulnerable query)
- Test client (curl / Postman / Burp Community)

## Steps
1. **Deploy VPC/VNet skeleton**: public subnet for ALB, private for App/DB. Security Groups/NSGs deny-all by default.
2. **Launch App Tier**: EC2/VMSS container or serverless function. Intentionally include a dynamic SQL route (`/search?q=`) for the test phase.
3. **Exploit Phase**: Prove SQLi with payloads (`' OR 1=1 --`, time-based `SLEEP(5)`, boolean-based). Record responses.
4. **WAF Controls**: Enable managed SQLi rules + add custom rule for your known payload. Re-test; confirm `403` or challenge.
5. **Code Fix**: Replace dynamic SQL with prepared statements/ORM. Add server-side validation. Re-test; verify blocked at code layer.
6. **IAM & Secrets**: Rotate DB credentials; move to Secrets Manager/KMS. Switch DB auth to IAM (where supported). Enforce least privilege.
7. **Network Hardening**: Restrict DB SG/NSG to App SG only; ensure DB is private-only.
8. **Logging → SIEM**: Ship WAF, App, and DB audit logs to SIEM (CloudWatch→Kinesis→Splunk/Sentinel or native pipelines). Create a correlation rule.
9. **SOAR Playbook**: On SQLi alert, automatically block source IP, rotate app secret, and notify channel.
10. **Validation**: Run payloads again; confirm SIEM alert & SOAR actions. Capture screenshots for your portfolio.

## Deliverables
- Before/after screenshots, WAF rule IDs, code diff for prepared statements, SIEM alert + SOAR action log.
- Update README “Controls Checklist” with actual ✅ items implemented.
