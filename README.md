<p align="center">
  <img src="./assets/banner.svg" alt="Awesome Transactional Email Delivery Banner" width="100%" />
</p>

# 📨 Awesome Transactional Email Delivery

<p align="center">
  <a href="https://github.com/ishandutta2007/Awesome-Awesome-Awesome"><img src="https://img.shields.io/badge/Awesome-%E2%9C%94-blueviolet?style=flat-square&logo=github" alt="Awesome"/></a><a href="https://discord.gg/jc4xtF58Ve"><img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord" /></a>
  <a href="https://github.com/ishandutta2007/Awesome-Awesome-Awesome"><img src="https://awesome.re/badge.svg" alt="Awesome" /></a>
  <a href="https://github.com/ishandutta2007/Awesome-Transactional-Email-Delivery"><img src="https://img.shields.io/badge/Category-Email%20Infrastructure-blue.svg" alt="Email Infrastructure" /></a>
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT" /></a>
  <a href="https://github.com/ishandutta2007/Awesome-Transactional-Email-Delivery/pulls"><img src="https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat" alt="Contributions Welcome" /></a>
  <a href="https://github.com/ishandutta2007"><img alt="GitHub followers" src="https://img.shields.io/github/followers/ishandutta2007?label=Follow" /></a>
</p>

> 🚀 A curated list of top **Transactional Email Delivery** SaaS platforms, API providers, deliverability engines, and self-hosted open-source email infrastructure projects.

---

## 📑 Table of Contents

- [📊 Sector Overview & Market Dynamics](#-sector-overview--market-dynamics)
- [☁️ SaaS & Hosted Email Platforms](#️-saas--hosted-email-platforms)
- [📦 Open-Source GitHub Projects](#-open-source-github-projects)
- [🎯 Key Selection Criteria](#-key-selection-criteria)
- [🤝 Support](#-support)
- [⭐ Star History](#-star-history)
- [📝 How to Contribute](#-how-to-contribute)
- [⚖️ Disclaimer](#️-disclaimer)

---

## 📊 Sector Overview & Market Dynamics

The global transactional email and enterprise messaging infrastructure market is estimated at **$3.8 billion to $4.5 billion**, expanding at a 13–15% CAGR fueled by cloud-native microservices, multi-factor authentication (MFA/OTPs), real-time alerts, and product-led growth communications. The industry exhibits **moderate fragmentation with high concentration at the tier-1 infrastructure layer**—a few dominant cloud and communications behemoths (Amazon Web Services, Twilio/SendGrid, Sinch/Mailgun, Intuit/Mailchimp) capture majority outbound enterprise volume, while modern developer-experience platforms (Resend, Postmark) and self-hosted open-source solutions aggressively capture mid-market developers seeking lower latency, React/code-first email development, and sovereignty over deliverability infrastructure.

---

## ☁️ SaaS & Hosted Email Platforms

The following hosted transactional email providers and APIs are sorted in descending order by **company scale (annual revenue / market valuation)**:

| Platform | Company Scale (Revenue / Valuation) | Starting Paid Tier Pricing | Free Tier / Trial Limit | Key Highlights & Architecture |
| :--- | :--- | :--- | :--- | :--- |
| **[Amazon SES](https://aws.amazon.com/ses/)** | 🏢 **~$105B+ AWS Annual Run-Rate** (Amazon ~$2.3T Market Cap) | 💳 **$0.10 per 1,000 emails** ($10/month for 100,000 emails; $0.12/GB attachments) | 🎁 **62,000 emails/month free forever** when called from EC2/Lambda (or 3,000 emails/month free for 12 months on AWS Free Tier) | ⚡ Industry price floor leader; ultra-reliable global AWS backbone; deeply integrates with SNS, SQS, CloudWatch, and IAM policies. |
| **[Mandrill](https://mandrill.com/)** | 🏢 **~$1B+ Intuit Mailchimp Revenue** (Intuit ~$180B Market Cap) | 💳 **$20/month per block of 25,000 emails** (requires Mailchimp Standard plan starting at $20/month, total min ~$40/month) | 🎁 **500 free transactional trial emails** to any email address on your verified domain | ⚡ Transactional email add-on strictly tied to Mailchimp; synchronizes contact events and leverages Mailchimp template engines. |
| **[HubSpot Transactional Email](https://www.hubspot.com/)** | 🏢 **~$2.6B+ Annual Revenue** (~$28B Market Cap) | 💳 **$300/month flat fee for dedicated IP & unlimited transactional sends** (requires Marketing Hub Pro starting at $890/month) | 🎁 **14-day free trial** of Marketing Hub with full platform feature access (no free-forever transactional tier) | ⚡ Unified customer journey tracking directly connected to HubSpot CRM, pipelines, and attribution reporting. |
| **[SendGrid](https://sendgrid.com/)** | 🏢 **~$4.4B+ Twilio Annual Revenue** (~$15B Market Cap) | 💳 **$19.95/month for up to 50,000 emails/month** (Essentials plan) | 🎁 **100 emails/day free forever** (~3,000 emails/month) | ⚡ Ubiquitous industry standard; robust SMTP/REST API relay, dynamic templating, suppression list management, and deliverability insights. |
| **[Mailgun](https://www.mailgun.com/)** | 🏢 **~$2.7B+ Sinch Annual Revenue** (Acquired for $1.9B) | 💳 **$15/month for up to 10,000 emails/month** (Basic plan, $1.50 per 1,000 overage) | 🎁 **30-day free trial with 5,000 free emails total** | ⚡ Renowned for developer-first REST APIs, advanced inbound MIME parsing, SPF/DKIM verification, and isolated EU/US GDPR regions. |
| **[SparkPost](https://www.sparkpost.com/)** | 🏢 **~$600M+ Bird/MessageBird Group Valuation** | 💳 **$20/month for up to 50,000 emails/month** (Starter plan) | 🎁 **30-day free trial with 500 emails/month free limit** | ⚡ Enterprise high-volume sending engine powered by Momentum MTA; industry-leading deliverability analytics and predictive mailbox placement. |
| **[Postmark](https://postmarkapp.com/)** | 🏢 **~$500M+ ActiveCampaign Valuation** | 💳 **$15/month for up to 10,000 emails/month** ($1.80 per 1,000 overage; 45-day log retention) | 🎁 **100 emails/month free forever** with complete API and dashboard access | ⚡ Ultra-fast delivery latency (sub-10s); strictly enforces architectural isolation between transactional and broadcast streams. |
| **[Brevo](https://www.brevo.com/)** | 🏢 **~$120M+ Annual Revenue** (Valued at ~$500M+) | 💳 **$9/month for up to 5,000 emails/month** (Starter tier; no daily send limits) | 🎁 **300 emails/day free forever** (~9,000 emails/month total) | ⚡ Multi-channel communication suite uniting transactional email, SMS, WhatsApp API, and CRM on European-hosted infrastructure. |
| **[Resend](https://resend.com/)** | 🏢 **~$100M+ Valuation** ($13M+ Seed/Series A from Y Combinator & Craft) | 💳 **$20/month for up to 50,000 emails/month** (Pro plan) | 🎁 **3,000 emails/month free forever** (100 emails/day limit, 1 custom domain) | ⚡ Built specifically for frontend/full-stack developers; first-class React Email component integration, modern REST API, and webhooks. |
| **[MailerSend](https://www.mailersend.com/)** | 🏢 **~$35M+ MailerGroup Annual Revenue** | 💳 **$30/month for up to 50,000 emails/month** (Premium plan, $0.90 per 1,000 overage) | 🎁 **3,000 emails/month free forever** (100 emails/day limit, full API/SMTP access) | ⚡ Developer-friendly transactional email & SMS platform from the creators of MailerLite; visual drag-and-drop template builder & inbound routing. |

---

## 📦 Open-Source GitHub Projects

Self-hosted and provider-agnostic transactional email systems, notification routers, and mail servers. Projects are listed in descending order by **GitHub Star Count**:

| Project | Stars | Language | Primary Category | Description & Capabilities |
| :--- | :--- | :--- | :--- | :--- |
| **[Novu](https://github.com/novuhq/novu)** | [![Stars](https://img.shields.io/github/stars/novuhq/novu?style=social&color=white)](https://github.com/novuhq/novu/stargazers) | TypeScript | 🔔 Notification & Email Infrastructure | Unified communications engine coordinating transactional email, SMS, push, in-app feeds, and chat with built-in provider routing and digest algorithms. |
| **[Listmonk](https://github.com/knadh/listmonk)** | [![Stars](https://img.shields.io/github/stars/knadh/listmonk?style=social&color=white)](https://github.com/knadh/listmonk/stargazers) | Go | 📬 Newsletter & Transactional API | High-performance single-binary mail orchestrator backed by PostgreSQL; supports transactional API triggers with custom templates over upstream SMTP relays. |
| **[docker-mailserver](https://github.com/docker-mailserver/docker-mailserver)** | [![Stars](https://img.shields.io/github/stars/docker-mailserver/docker-mailserver?style=social&color=white)](https://github.com/docker-mailserver/docker-mailserver/stargazers) | Shell / Python | 🐳 Fullstack SMTP Server | Production-ready, containerized mail server image equipped with Postfix, Dovecot, OpenDKIM, OpenDMARC, Fail2ban, and SpamAssassin. |
| **[React Email](https://github.com/resend/react-email)** | [![Stars](https://img.shields.io/github/stars/resend/react-email?style=social&color=white)](https://github.com/resend/react-email/stargazers) | TypeScript | ⚛️ Email Templating & Components | Modern standard collection of high-quality, unstyled React components for crafting responsive transactional emails that render reliably across all clients. |
| **[Postal](https://github.com/postalserver/postal)** | [![Stars](https://img.shields.io/github/stars/postalserver/postal?style=social&color=white)](https://github.com/postalserver/postal/stargazers) | Ruby | 📮 Complete Delivery Platform | Battle-tested full-featured alternative to SendGrid and Mailgun; supports incoming/outgoing mail, webhooks, click/open tracking, and multi-organization routing. |
| **[Stalwart Mail Server](https://github.com/stalwartlabs/stalwart)** | [![Stars](https://img.shields.io/github/stars/stalwartlabs/stalwart?style=social&color=white)](https://github.com/stalwartlabs/stalwart/stargazers) | Rust | 🦀 Next-Gen Mail Server | Modern, all-in-one secure mail platform built entirely in Rust supporting JMAP, IMAP, SMTP, ACME TLS, DMARC, DKIM, and SPF validation. |
| **[Transactional Email Templates](https://github.com/mailgun/transactional-email-templates)** | [![Stars](https://img.shields.io/github/stars/mailgun/transactional-email-templates?style=social&color=white)](https://github.com/mailgun/transactional-email-templates/stargazers) | HTML / CSS | 🎨 Production Email Templates | Open-source responsive HTML email templates for transactional use cases (password resets, order receipts, activation alerts) curated by Mailgun. |
| **[Postmark Transactional Templates](https://github.com/ActiveCampaign/postmark-templates)** | [![Stars](https://img.shields.io/github/stars/ActiveCampaign/postmark-templates?style=social&color=white)](https://github.com/ActiveCampaign/postmark-templates/stargazers) | CSS / HTML | 📝 Production Email Templates | Rock-solid responsive transactional email templates crafted by Postmark, thoroughly tested across major desktop, web, and mobile email clients. |
| **[Hermes](https://github.com/matcornic/hermes)** | [![Stars](https://img.shields.io/github/stars/matcornic/hermes?style=social&color=white)](https://github.com/matcornic/hermes/stargazers) | Go | ✉️ Programmatic Email Generator | Golang engine that programmatically creates clean, responsive, localized HTML and plain-text emails for transactional workflows. |
| **[Dittofeed](https://github.com/dittofeed/dittofeed)** | [![Stars](https://img.shields.io/github/stars/dittofeed/dittofeed?style=social&color=white)](https://github.com/dittofeed/dittofeed/stargazers) | TypeScript | 🤖 Automated Messaging Engine | Modern open-source customer communication platform to orchestrate transactional and behavioral message sequences across email, SMS, and webhooks. |
| **[Forward Email](https://github.com/forwardemail/free-email-forwarding)** | [![Stars](https://img.shields.io/github/stars/forwardemail/free-email-forwarding?style=social&color=white)](https://github.com/forwardemail/free-email-forwarding/stargazers) | JavaScript | 🔒 Privacy SMTP & Forwarding | Privacy-focused encrypted email service and transactional SMTP API with full support for DNS-based routing, spam filtering, and custom domains. |
| **[Notifuse](https://github.com/Notifuse/notifuse)** | [![Stars](https://img.shields.io/github/stars/Notifuse/notifuse?style=social&color=white)](https://github.com/Notifuse/notifuse/stargazers) | TypeScript | 🎛️ Multi-Provider Email Platform | Self-hosted visual transactional and marketing platform featuring MJML drag-and-drop authoring and multi-provider relay switching (SES, Postmark, Mailgun). |
| **[Cuttlefish](https://github.com/mlandauer/cuttlefish)** | [![Stars](https://img.shields.io/github/stars/mlandauer/cuttlefish?style=social&color=white)](https://github.com/mlandauer/cuttlefish/stargazers) | Ruby | 🦑 Transactional Mail Server | Transactional mail server featuring web dashboard observability, quota controls, automated retry mechanisms, and delivery status logging. |
| **[Apache James](https://github.com/apache/james-project)** | [![Stars](https://img.shields.io/github/stars/apache/james-project?style=social&color=white)](https://github.com/apache/james-project/stargazers) | Java | ☕ Modular Enterprise Mail Server | Enterprise-grade modular messaging server supporting SMTP, LMTP, IMAP, and JMAP protocols with pluggable spool processing and custom matchers. |
| **[Posta](https://github.com/goposta/posta)** | [![Stars](https://img.shields.io/github/stars/goposta/posta?style=social&color=white)](https://github.com/goposta/posta/stargazers) | Go | 📬 Self-Hosted Delivery API | Developer-first Go email delivery platform providing unified HTTP sending APIs, SMTP relay, dynamic templates, analytics, and tenant management. |
| **[Larasend](https://github.com/savvyagents/larasend)** | [![Stars](https://img.shields.io/github/stars/savvyagents/larasend?style=social&color=white)](https://github.com/savvyagents/larasend/stargazers) | PHP / Laravel | 📮 Self-Hosted SES Dashboard | Self-hosted transactional management layer on top of Amazon SES; provides dedicated API keys, sending logs, bounce handlers, and webhook events. |
| **[Senlo](https://github.com/IgorFilippov3/senlo)** | [![Stars](https://img.shields.io/github/stars/IgorFilippov3/senlo)](https://github.com/IgorFilippov3/senlo/stargazers) | TypeScript | 🔌 Provider-Agnostic Infrastructure | Decoupled email orchestration layer allowing developers to trigger transactional templates over any SMTP relay or provider (SES, Postmark, Resend). |

---

## 🎯 Key Selection Criteria

When evaluating transactional email platforms and infrastructure:

1. 🛡️ **Deliverability & Reputation Isolation**: High deliverability requires strict separation of transactional notifications (receipts, 2FA codes, password resets) from bulk marketing campaigns. Platforms like Postmark enforce stream isolation by default.
2. 💰 **Infrastructure Ownership vs. Total Cost**: Amazon SES offers unmatched unit economics ($0.10/1,000 emails), but places operational burdens (IP warming, DNS validation, bounce management) on engineering teams. Modern APIs like Resend and Postmark trade margin for rapid developer onboarding.
3. ⚙️ **Self-Hosting Realities**: Self-hosting mail software (e.g., Postal, Stalwart, Posta) solves data sovereignty and infrastructure costs. However, operational deliverability (warmup schedules, feedback loops, ASN reputation, blacklists) requires ongoing engineering stewardship.

---

## 🤝 Support

Thank you for exploring this curated repository! If you find this directory valuable for your projects or infrastructure planning, please consider showing your support:

- ⭐ **Star this repository** to help others discover it across GitHub.
- 🍴 **Fork and contribute** your favorite transactional mail engines and tools.
- 📢 **Share with fellow developers**, DevOps, and platform engineers.
- ☕ **Buy a coffee or sponsor ongoing maintenance**: [Sponsor Ishan Dutta on GitHub](https://github.com/sponsors/ishandutta2007)

---

##  Star History
[![Star History Chart](https://star-history.dera.page/svg?repos=ishandutta2007/Awesome-Transactional-Email-Delivery&type=date&legend=top-left)](https://star-history.dera.page/#ishandutta2007/Awesome-Transactional-Email-Delivery&type=date&legend=top-left)

---

## 📝 How to Contribute

1. 🍴 Fork this repository on GitHub.
2. ✏️ Add or update items in [`README.md`](file:///C:/Users/hp/Documents/Projects/Awesome-Transactional-Email-Delivery/README.md) while maintaining the existing table structure and sorted order.
3. 🏷️ Ensure all SaaS entries include explicit starting tier pricing and accurate free tier or trial conditions.
4. 🌟 Ensure open-source additions include appropriate GitHub Star badges formatted with `style=social&color=white` linked to the repository stargazers page.
5. 🚀 Submit a pull request with a clear description of your additions.

---

## ⚖️ Disclaimer

- 📖 This list is a **community-curated resource** for technical evaluation and educational reference.
- 🛡️ Sending transactional email requires strict compliance with international privacy and anti-spam statutes (e.g., CAN-SPAM, GDPR, CASL). Always verify DNS SPF, DKIM, and DMARC enforcement before sending production traffic.
- 📜 Check third-party software licensing terms (e.g., AGPL, Apache 2.0, MIT) before embedding open-source engines into commercial architectures.
