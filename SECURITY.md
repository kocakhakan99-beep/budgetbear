# Security & Privacy

Policy summary
- BudgetBear has no application server or user account.
- Financial data is stored locally in browser `localStorage`.
- The app loads third-party libraries from CDNs; those requests do not include
  the application's saved state.

Recommendations for safe usage
- Regularly export JSON backups to a file you control.
- Treat exported XLSX, PDF, and JSON files as sensitive financial data.
- Do not share exported files without verifying contents.

Implementation guidelines
- Never hardcode secrets or keys in the source code.
- Never log user data or place exported files in the repository.
- Keep third-party library versions reviewed when updating CDN references.

Vulnerability disclosure
- Report vulnerabilities privately to the repository owner where possible. Do
  not include personal financial data in a public issue.