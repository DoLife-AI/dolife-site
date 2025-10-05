---
layout: page
title: Privacy Policy
permalink: /privacy/
include_in_header: true
---

_Last updated: {{ site.time | date: "%B %d, %Y" }}_

## Who we are
DoLife AI, LLC (“**DoLife**”, “we”, “us”)  
Georgia, United States  
Contact: [support@dolife-ai.com](mailto:support@dolife-ai.com)

## What this policy covers
This explains what we (and our processors) handle when you use:
- The DoLife iOS app
- Our website at app.dolife-ai.com (hosted via GitHub Pages)
- Optional email & calendar connectors you choose to turn on

We designed DoLife to be **on-device first**. By default, your mail content is fetched on your device; personally identifying details are **redacted on device** before any AI step.

## What we collect

### Account & sign-in
- Email address (for email/magic link sign-in)
- Apple/Google sign-in identifiers (identity only; no calendar/email access at sign-in)

### In-app data you create
- Tasks and related fields (title, notes, due date or priority, recurrence, steps, created by/date, notifications)
- Domains/tags and sharing relationships
- Optional child labels (e.g., first name badges you choose to enter)
- Preferences

### Optional connectors (you choose to connect)
- **Email**: Gmail (gmail.readonly), Microsoft 365 (Mail.Read), iCloud IMAP. Mail is fetched on your device.  
- **Calendar**: Apple (EventKit), Google (calendar.readonly/… as you authorize), Microsoft 365 (Calendars.Read).

### Website
- We do not add tracking pixels. GitHub Pages may set strictly-necessary cookies to serve the site.

### Diagnostics/analytics
- Not enabled at launch. If we add privacy-respecting analytics or crash reporting later, we will update this policy.

## How we use data (purposes)
- Provide core features (auth, sync, sharing, notifications)
- Optional email & calendar features you explicitly enable
- Security, fraud prevention, and support
- Optional AI summarization of **sanitized** email text into suggested tasks (“For Review”)

We do **not** sell personal data or share it for cross-context behavioral advertising.

## AI & PII-redaction
- On device, we detect likely personal info (names, emails, phone numbers, addresses, dates, URLs) and replace with tokens like `[PERSON]`, `[EMAIL]`, `[ADDRESS]`.
- Only the **sanitized text** is sent to our Supabase Edge Function.
- The Edge Function calls an LLM (planned: OpenAI GPT-4.1) with a strict JSON schema to return `{ tasks: [...] }`.
- We do **not** permit the LLM provider to use your data to train its models. If a provider requires that by default, we opt out.

## Third-party services (processors/controllers)
- **Supabase** (auth, database, storage; row-level security): operates our backend.
- **Postmark** (email) for magic-link sign-in and transactional mail.
- **Apple / Google / Microsoft**: OAuth for sign-in and for the optional calendar/email connectors you explicitly authorize.
- **OpenAI (planned)**: model inference for sanitized text only, via our Edge Function.
We only share the minimum necessary with these processors to provide the service.

## Data retention
- **Account & app data**: kept until you delete your account or content.  
- **LLM requests/responses**: not stored beyond transient processing; we log request metadata (timestamps, success/failure) for up to **30 days**.  
- **Server logs**: up to **30 days** for security/troubleshooting.  
- **Backups**: encrypted rolling backups retained for up to **35 days**.

## Deletion & your choices
- You can request account deletion via [support@dolife-ai.com](mailto:support@dolife-ai.com). We will delete account data and content subject to legal/backup constraints (backups roll off within 35 days).  
- You can disconnect any connector at any time (within the app and/or via Apple/Google/Microsoft account settings).  
- You may export or copy your data from within the app (where available) or by contacting support.

## Legal bases & rights
For U.S. users: we operate under applicable U.S. law.  
If we later serve EU/UK users, we will update this section to reflect GDPR/UK-GDPR rights and legal bases.

## Children
DoLife is intended for adults and individuals **13+**. Parents/caregivers may enter children’s first names to organize tasks; that entry is made by the adult user. We do not knowingly collect personal data directly from children under 13.

## Security
- Encryption in transit (TLS) and at rest (Supabase-managed).  
- Row-Level Security (RLS) and least-privilege access controls.  
- Access logging and periodic review.  
No method is perfectly secure; we work to protect your data and improve continually.

## International use
We primarily serve U.S. users and host data in U.S. regions. If we expand internationally, we will update this policy accordingly.

## Incident notification
If a security incident materially affects your data, we will notify you without undue delay and follow applicable laws.

## Changes to this policy
We may update this policy. We will post the new version here and update the “Last updated” date. For material changes, we may also notify you in-app or by email.

## Contact
Questions or requests: [support@dolife-ai.com](mailto:support@dolife-ai.com)
