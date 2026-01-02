# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please email security@example.com with:

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Your recommended fix (if any)

Please do NOT open a public issue for security vulnerabilities.

## Security Best Practices

- Keep dependencies updated via Renovate
- Review security advisories regularly
- Use strong credentials and rotate regularly
- Follow OWASP guidelines for application security
- Run CodeQL security scans in CI/CD
- Implement proper authentication and authorization
- Never commit secrets to the repository

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Security Scanning

This project uses:
- GitHub CodeQL for code analysis
- Dependabot for dependency scanning
- npm audit for vulnerability checks
