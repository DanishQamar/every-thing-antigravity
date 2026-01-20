---
description: Conduct a deep-dive security analysis of the codebase.
---

# Security Review Workflow

1. **Vulnerability Detection**
   - Identify OWASP Top 10 issues
   - Check for hardcoded secrets
   - Validate input sanitization

2. **Review High-Risk Areas**
   - Authentication/Authorization
   - API endpoints
   - Database queries
   - File uploads

3. **Security Checklist**
   - [ ] No hardcoded secrets
   - [ ] All inputs validated
   - [ ] SQL injection prevention
   - [ ] XSS prevention
   - [ ] Rate limiting enabled

4. **Report Findings**
   - List Critical/High/Medium issues
   - Provide remediation steps
