# Awesome-Transactional-Email-Delivery

# Top Transactional Email Delivery Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on API-Driven Sending, Deliverability Infrastructure & Self-Hosted Mail Platforms*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Transactional Email Delivery**. These tools enable applications to send time-sensitive, user-triggered emails—password resets, receipts, verification codes, and notifications—reliably and at scale, with the deliverability infrastructure and observability that mission-critical messaging demands.

**Examples** include HubSpot Transactional Email, SendGrid, Mailgun, Amazon SES, Postmark, Brevo, SparkPost, Resend, Mandrill, and MailerSend (the category leaders).

**Open-source emphasis**: Transactional Email Delivery is a domain where open-source tooling is **genuinely viable for self-hosted sending infrastructure but requires operational maturity**. **Posta** stands out as the most complete self-hosted alternative to SendGrid, Mailgun, and Postmark—a single-binary Go platform with outbound API, inbound parsing, SMTP relay, templates, campaigns, bounce handling, and multi-tenant workspaces . **Postal** provides a mature, full-featured mail delivery platform with HTTP APIs, SMTP relay, click/open tracking, and multi-organization support, deployable via Docker . **Senlo** offers a developer-first, provider-agnostic email infrastructure where you bring your own sending provider (Resend, Postmark, SES, or SMTP) while Senlo handles templates, automations, and analytics . The critical caveat: **deliverability is the hard part, not the software**—self-hosting means you own IP reputation, SPF/DKIM/DMARC configuration, and bounce processing, which managed providers handle for you .

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[HubSpot Transactional Email](https://www.hubspot.com/)**  
  Transactional email add-on within HubSpot's Marketing Hub; keeps transactional and marketing streams separate while providing a unified view of customer interactions. **Expensive as a standalone option**—requires a paid Marketing Hub Professional or Enterprise plan (starting at $1,490/month) before the add-on, though it then includes unlimited transactional sends . Best for organizations already standardized on HubSpot CRM.

- **[SendGrid](https://sendgrid.com/)**  
  Industry-standard email delivery platform for high-volume senders; provides SMTP relay and API, dynamic templates, and deliverability tools. Widely adopted for enterprise-scale transactional and marketing email.

- **[Mailgun](https://www.mailgun.com/)**  
  The most **API-first** of the major providers; excels at inbound routing and email parsing for reply-to-app workflows, with pre-send email validation and EU/US data regions for GDPR compliance . Pricing from $15/month for 10,000 emails .

- **[Amazon SES](https://aws.amazon.com/ses/)**  
  The **cheapest option by a wide margin** at $0.10 per 1,000 emails (~$10 for 100,000/month) . AWS-native integration with SNS, CloudWatch, and Lambda. **Trade-off**: you own IAM configuration, domain verification, IP warmup, and analytics wiring—no beginner-friendly path .

- **[Postmark](https://postmarkapp.com/)**  
  Optimized for **delivery speed** on time-sensitive messages (magic links, OTPs, receipts); Message Streams isolate transactional from broadcast traffic by default . Manual account review before sending is enabled. Pricing from $15/month for 10,000 emails; 45-day log retention .

- **[Brevo](https://www.brevo.com/)**  
  All-in-one platform with transactional email alongside marketing, SMS, and CRM; robust infrastructure for high-volume order confirmations with GDPR compliance built in .

- **[SparkPost](https://www.sparkpost.com/)**  
  High-volume email delivery platform with analytics and deliverability tools; positioned for enterprises sending billions of messages.

- **[Resend](https://resend.com/)**  
  Developer-focused transactional email API with modern SDKs and React Email support; positioned for developer-controlled infrastructure .

- **[Mandrill](https://mandrill.com/)**  
  Transactional email add-on for Mailchimp; provides API-based sending with analytics and templates, integrated with Mailchimp audiences.

- **[MailerSend](https://www.mailersend.com/)**  
  Transactional email API and SMTP service from the makers of MailerLite; features templates, analytics, and inbound routing.

## Open-Source GitHub Projects

### Self-Hosted Email Delivery Platforms

- **[Posta](https://github.com/jkaninda/posta)**  
  The most comprehensive self-hosted **SendGrid/Mailgun/Postmark alternative** available; a developer-first email platform handling **outbound, inbound, and relayed email** via a single HTTP API with SMTP available for legacy paths . Features: **Outbound** (transactional/batch/templated emails with attachments, scheduled sending, preview mode, address verification, automatic retries with priority queues) ; **Inbound** (built-in SMTP receiver with TLS, webhook ingest with HMAC verification, spam scoring, attachment storage, forwarding) ; **Relay** (point existing SMTP clients at Posta without code changes) ; **Templates** (versioned, multi-language, variable substitution) ; **Campaigns** (bulk email with A/B testing) ; **Security** (API keys with IP allowlisting, JWT/RBAC, TOTP 2FA, OAuth/SSO) ; and **Workspaces** (multi-tenant with isolated roles) . Docker-deployable with a single container. **The strongest open-source foundation for replacing a managed transactional email provider**.

- **[Postal](https://github.com/postalserver/postal)**  
  Mature open-source **mail delivery platform** for outbound and transactional email; provides HTTP APIs, SMTP relay, click and open tracking, bounce handling, webhooks, and multi-organization/multi-mail-server support . Deployment via Docker Compose (web, SMTP, worker, MariaDB) requires **4GB RAM and 2 CPU cores minimum** . Requires careful DNS configuration (SPF, DKIM, MX records for bounce handling and tracking domains) . **The most battle-tested open-source Postal alternative to SendGrid/Mailgun**—but you own deliverability, IP reputation, and infrastructure maintenance.

### Provider-Agnostic Email Infrastructure

- **[Senlo](https://github.com/IgorFilippov3/senlo)**  
  Open-source, **provider-agnostic** email infrastructure for transactional and lifecycle emails (MVP stage) . Key differentiator: **bring your own delivery provider**—configure Resend, Postmark, or any SMTP server (including SES, Mailgun, or self-hosted) without changing your code . Features: visual drag-and-drop template editor, API-first triggering (`POST /api/triggered`), dynamic personalization with merge tags and conditional logic, template versioning, multi-project isolation (staging/production), and automations that branch on your own API data . **Best for teams wanting to self-host the template/automation layer while still using a managed delivery provider**—reduces lock-in and lets you swap providers without rewrites.

### Mailing List & Campaign Managers (Adjacent)

- **[Listmonk](https://github.com/knadh/listmonk)**  
  Open-source newsletter and mailing list manager (AGPLv3, Go + Vue); ships as a single binary with PostgreSQL as the only dependency . **Not a transactional-first platform**—it is designed for campaigns and newsletters—but supports transactional mail via its API, with templates, subscriber management, and analytics. **Critical caveat**: Listmonk **only sends over SMTP**, so you must pair it with an external SMTP provider (SES, Postmark, SendGrid) for actual delivery . Best for teams wanting self-hosted newsletter management, not primary transactional infrastructure.

### Additional Strong Open-Source Options

- **Apache James** — Enterprise mail server (Java) supporting SMTP, IMAP, POP3, and JMAP with modular architecture; **infrastructure-level**—provides the mail server itself, not a transactional email API with templates and analytics .
- **No open-source project matches the deliverability infrastructure of managed providers** — IP warmup, reputation monitoring, and inbox placement are operational services, not software features. Self-hosting means you own these responsibilities .

**Frameworks for building custom systems**: For a **full self-hosted transactional email platform** (API + inbound + relay + templates), Posta is the most complete option . For a **mature, battle-tested mail delivery platform** with a track record, Postal . For **provider-agnostic infrastructure** that lets you keep using a managed sender while self-hosting templates and automations, Senlo . For **newsletter/campaign management**, Listmonk (paired with an SMTP provider) . No open-source project replaces the **deliverability engineering** that managed providers like Postmark and SES handle—expect to own IP reputation, authentication, and bounce processing.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Transactional email platforms handling recipient data and message content must comply with applicable privacy regulations (GDPR, CCPA) and anti-spam laws (CAN-SPAM); **transactional emails are typically exempt from marketing consent requirements, but misclassification can create legal risk**.
- **Open-source transactional email is viable for software but not for deliverability**—Posta and Postal provide production-grade sending platforms , and Senlo offers provider-agnostic infrastructure . However, **deliverability (IP reputation, warmup, inbox placement) is an operational service that managed providers handle and self-hosters must own** . Organizations without email infrastructure expertise should evaluate Postmark, SES, or Mailgun rather than self-hosting.
- Verify license terms for commercial use; Posta is open-source (check repository) , Postal is open-source , and Senlo is open-source (MVP stage) .

---

**Made for application developers, platform engineers, and teams building reliable email delivery infrastructure.**  
Let's make transactional email more open, but with clear eyes about the deliverability engineering that software alone cannot replace.
