# Security & Privacy (offline-first)

Policy summary
- BudgetBear does not send user financial data to remote servers by default.
- All storage is local to the user’s machine and managed by their browser.

Recommendations for safe usage
- Regularly export backups to a file you control (XLSX or encrypted JSON).
- If you opt-in to encryption, choose a strong passphrase and store it safely (the app does not keep it).
- Do not share exported files without verifying contents.

Implementation guidelines
- Never hardcode secrets or keys in the source code.
- If using the File System Access API, ensure files are only accessed with explicit user consent.
- For encryption, use the browser Web Crypto API (AES-GCM).
- For any third-party libraries (SheetJS, Dexie), keep them updated and verify signatures where possible.

Vulnerability disclosure
- Report vulnerabilities to the repository owner (open an issue labeled security, or email the owner contact in README).