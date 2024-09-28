---
title: "ACSC Information Security Manual"
description: "ISM controls in a form suitable for trace"
lead: "Web enabled ISM for automated security trace and validation."
draft: false
images: []
weight: 5
toc: true
---
## ISM Controls for Automated Security Trace and Validation

The following links provide the top-level [ISM](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/ism) control sets, which serve as input for automated security control allocation and automation.

- [ISM in Security Group Context](/context)
- [All the ISM Controls](/control/index)
- [Essential Eight Controls](/essential-eight)

## Overview

To obtain an Authority to Operate (ATO), systems must demonstrate reduced operational risks to an acceptable level. This is commonly achieved through the Australian Cyber Security Centre's ([ACSC](https://cyber.gov.au/)) Information Security Manual ([ISM](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/ism)). However, the traditional approach—using Excel spreadsheets and Word documents—complicates reliable control allocation and testing, making it challenging to maintain a verifiable security posture over time.

To address this, the U.S. standards body NIST has developed the Open Security Controls Assessment Language ([OSCAL](https://pages.nist.gov/OSCAL/)), which enables automated control allocation and testing. The ACSC has adapted this by publishing the ISM with an OSCAL schema.

Despite this advancement, additional tools are necessary for practical application. MentorMind has developed ISM OSCAL parsers in [Rust](https://www.rust-lang.org), complemented by a REST API for easy access.

Thus, the following `curl` request:

```bash
curl https://ism.mentormind.com.au/content/control/ism-0123
```

returns the following result:

Similarly, the following `curl` requests produce all the controls as a single document, as well as the different security control groups:

```bash
curl https://ism.mentormind.com.au/control
curl https://ism.mentormind.com.au/control/all
curl https://ism.mentormind.com.au/group
```

## Take Me to the Controls

[ISM in Group Context](/context) [All ISM Controls](/control/index) [Essential Eight Controls](/essential-eight)
