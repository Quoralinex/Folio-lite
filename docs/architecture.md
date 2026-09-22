# Quoralinex People (Folio-lite) Architecture

## Purpose
Folio-lite is the public Quoralinex staff/profile directory. The site renders staff profiles dynamically and supports direct employee URLs.

## Runtime flow
Browser -> static Folio-lite site -> Quoralinex portal directory API -> profile rendering.

The contact path adds Turnstile in the browser and requires server-side token validation in an approved Worker/backend before forwarding a message.

## Main components
- Static HTML/CSS/JS and brand imagery.
- Directory API at `https://portal.quoralinex.com/directory-api/employees`.
- Query/direct-path profile routing.
- Cloudflare Pages caching/hosting controls.
- Turnstile-protected contact UI with external Worker/backend validation.

## Boundaries
The public site is a presentation surface, not the system of record for staff information. Directory data should remain controlled upstream, and secrets must remain outside client-side code.
