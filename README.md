# FinControl

An offline-first personal + business finance tracker built as a Progressive Web App (PWA).

## Run it
A service worker requires HTTPS or localhost. For a quick local test, run a local web server in this folder:
- Python: `python -m http.server 8000`
- Open `http://localhost:8000`

To use on Android, host the folder on a trusted HTTPS static host, open the URL in Chrome, then choose **Install app** or **Add to Home screen**. The same app works in desktop browsers.

## Included
- Dashboard for card outstanding, manually entered bank balances, recorded personal/business spending and deal receivables.
- Credit card register (last four digits only).
- Bank account register (last four digits only).
- Transaction register with Personal / Business / Shared / Unclassified, Income / Expense / Transfer and Deal ID.
- Deal and commission tracker.
- In-app reminder list.
- CSV transaction import.
- JSON backup and restore.
- Dark and light themes.
- Local IndexedDB storage and offline service-worker cache.

## Important limitations in this first version
- No SMS reading, bank connection, cloud sync or server upload.
- CSV import only; PDF statements need conversion to CSV/XLSX first.
- CSV column detection is best-effort; review imported rows before relying on reports.
- Duplicate detection and statement reconciliation are not yet implemented.
- Browser reminders are an in-app list; push notifications / background scheduled alerts are not guaranteed when the app is closed. Use issuer apps or your calendar for critical due dates.
- No biometric lock in this version. Device screen lock and browser/device security still matter.
- This PWA is installable on Android but is not a signed native APK.

## Privacy
Records are stored in IndexedDB in the browser profile on the device. Clearing browser data, uninstalling or losing the device may delete records. Export JSON backups regularly and keep them in a secure location. Do not import or store full card numbers, CVV, PINs, OTPs, passwords or full bank account numbers.
