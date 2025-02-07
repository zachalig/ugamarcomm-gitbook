---
description: >-
  How to set up transactional (system) emails on WordPress sites when hosted on Pantheon
---

# WordPress Transactional Email Setup on Pantheon Hosting

Some WordPress features require that it be able to send emails. For example, when a user requests a password reset, WordPress will send them an email with a link and instructions. Emails sent by an app, website, or other system, are called _transactional emails_.

As of January 2025, all of our WordPress sites are hosted on Pantheon.io, which [recommends against using WordPress' default email system by default](https://docs.pantheon.io/email). Every WordPress site we launch must be configured with a REST API based transactional email system.

## Step-by-step Instructions

### Step 1: Familiarize yourself with the process

If you've never done this before, take a minute and at least skim Pantheon's documentation: [CMS Email Service on Pantheon](https://docs.pantheon.io/email).

### Step 2: Log into SendGrid and create an API Key

MARCOMM has an account on [SendGrid](https://app.sendgrid.com), a top transactional email service. Head over to [sendgrid.com](https://www.sendgrid.com) and log in.

-  The login information for SendGrid is stored in our LastPass shared vault. If you don't already have access to LastPass, contact your supervisor.
- As of January 2025, SendGrid also requires a 2FA TOTP (ramdomly generated time code PIN). If you do not have a configured authenticator, contact the department's head of IT.
- This account was created and is administrated by MARCOMM's IT team (mcit@uga.edu)

Once logged in, create an API key by following these steps: 
