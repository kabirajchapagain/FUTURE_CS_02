# Phishing Detection & Awareness System

Cyber Security Task 2 — Future Interns

## Overview

This repository contains a phishing email analysis exercise: four sample
emails (two phishing, one suspicious, one legitimate), a header/content
analysis of each, and a resulting awareness report with prevention
guidelines for employees.

## Contents

- `Phishing_Detection_Awareness_Report.pdf` — full report: methodology,
  risk classification framework, per-sample analysis, indicators
  checklist, and Do's/Don'ts.
- `Sample/` — sample email files (`.eml`) with headers, used as the
  evidence base for the report:
  - `sample1_account_verification.eml` — Phishing
  - `sample2_finance_invoice.eml` — Phishing
  - `sample3_suspicious_it_notice.eml` — Suspicious
  - `sample4_legitimate_password_reset.eml` — Safe (included for contrast)

- `Evidence/` — screenshots from the analysis (MXToolbox SuperTool,
  header analyzer, WHOIS, certificate lookup, search), each explained
  in section 6 of the report:
  - `sample1_google_search.png`, `sample1_whois.png`, `sample1_http_lookup_522.png`, `sample1_header_analysis.png`
  - `sample2_http_lookup_unresolved.png`, `sample2_header_analysis.png`
  - `sample3_http_lookup_unresolved.png`, `sample3_header_analysis.png`
  - `sample4_cert_lookup.png`, `sample4_header_analysis.png`

> Note: the sample emails are original, illustrative examples written
> for this exercise (not copied from any dataset). Their SPF/DKIM/DMARC
> values are written into the sample headers. Where an example domain
> turned out to be registered to a real party, it is treated neutrally
> and no claim is made about its owner.

## Tools Used

- [Google Admin Toolbox — Messageheader](https://toolbox.googleapps.com/apps/messageheader/)
- [MXToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)
- MXToolbox SuperTool: HTTP lookup, certificate lookup, WHOIS
- Google search for supporting context
- Links were checked only through lookup tools, never opened in a browser

## Analysis Approach

1. Compare the From, Reply-To, and Return-Path headers for mismatches.
2. Check SPF, DKIM, and DMARC authentication results.
3. Inspect linked URLs for lookalike, unrelated, or subdomain-confusion
   domains.
4. Assess the message body for urgency, threats, or fear-based pressure.
5. Check for generic greetings vs. genuine, expected correspondence.
6. Classify the email as **Safe**, **Suspicious**, or **Phishing** and
   document the reasoning in plain, non-technical language.

## Disclaimer

This work is for security education and awareness purposes only. No
phishing infrastructure was built or deployed, and no real individuals
or organizations were targeted.
