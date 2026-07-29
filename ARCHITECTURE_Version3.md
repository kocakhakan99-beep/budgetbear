# Architecture (offline-first)

Principles
- The app runs entirely client-side.
- Data is stored in the user's browser (IndexedDB).
- Data portability is achieved through explicit exports (XLSX + JSON).
- Optional client-side encryption protects backup files at user choice.

Core components
- UI (vanilla JS or framework): present & edit transactions, categories, budgets, reports.
- Persistence layer: Dexie.js wrapper over IndexedDB.
- Export/Import layer: SheetJS (xlsx) for Excel, JSON fallback, validators.
- Recurrence engine: generates projected future transactions for planning.
- PWA layer: manifest + Service Worker for offline app shell.

Data model (high-level)
- transactions: id, date, amount, type [expense/income], account, category_id, description, tags, recurring_rule_id (nullable)
- categories: id, name, budget_amount
- settings: id (singleton), currency, preferred_backup_format, encryption_enabled (local flag only)
- recurring_rules: id, frequency (daily/weekly/monthly/yearly/custom), amount, next_date, end_date

Persistence details
- Use Dexie.js; schema versioning for migrations.
- Store attachments (if any) in IndexedDB as Blobs.

Backup, export & restore
- Export options:
  - XLSX (human-friendly): SheetJS workbook with sheets: Transactions, Categories, Settings
  - JSON (lossless): full DB dump
- Import:
  - Validate schema and data integrity; run migrations as needed.
  - Provide preview before overwrite; support merging.
- Encryption:
  - Optional client-side AES-GCM encryption of the JSON backup file using a passphrase.
  - Use Web Crypto API; do not persist passphrase.

Advanced UX (optional)
- Use File System Access API (when available) to let users pick a file and allow updates without downloading each time.
- Provide recurring backup reminders and a "last exported" status.