# Security Policy

## Scope
Quoralinex People (Folio-lite) is a public-facing staff-directory/profile site backed by directory data and a Turnstile-protected contact flow.

## Required controls
- Do not commit employee credentials, private HR data, API keys, Turnstile secret keys or backend/webhook credentials.
- Treat staff-profile JSON/API data as publishable only when explicitly approved for public display.
- Validate Turnstile tokens server-side before processing contact submissions.
- Keep contact-form handling behind an approved Worker/backend; never place secret validation material in client-side code.
- Preserve HTTPS for directory API and form-backend communication.
- Static-profile routes must not expose unpublished or internal-only staff records.

## Reporting
Report suspected vulnerabilities or unintended personal-data exposure privately to repository maintainers. Do not publish sensitive staff data in a public issue.

## Supported code
Security fixes apply to the maintained `master` branch and current Cloudflare Pages deployment path.
