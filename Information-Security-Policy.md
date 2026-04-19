**Document Classification:** Public – Portfolio Demonstration  
**Version:** 1.0  
**Last Updated:** April 2026  

**INFORMATION SECURITY POLICY**

**H1t3X Portfolio Website**

_hitesh114.github.io/h1t3x_

Prepared by: Hitesh | Role: GRC Analyst (Fresher) | Version: 1.0 | Date: April 2026

# 1\. Purpose

This policy was created to define the basic security rules for my personal portfolio website (H1t3X), hosted at hitesh114.github.io/h1t3x. The goal of this document is to make sure that the website and the information associated with it are protected from common threats such as data scraping, unauthorized access, and content misuse.

As a fresher GRC (Governance, Risk and Compliance) analyst, I created this policy as part of a real-world practice exercise. It is based on my own Risk Register and ISO 27001 Control Mapping Sheet, which I applied to the portfolio's actual assets and threats. This policy shows that I understand how to identify risks and translate them into simple, actionable security rules.

# 2\. Scope

This policy applies to all assets and activities directly related to the H1t3X portfolio website. Specifically, it covers:

- The portfolio website hosted on GitHub Pages (hitesh114.github.io/h1t3x)
- The GitHub repository used to manage and deploy the website code
- Contact information, certification links, and project details published on the site
- Social media accounts linked from or referenced by the portfolio
- Third-party tools and services used to run the website, such as CDNs, GitHub Pages, and any JavaScript libraries
- Visitors who access the website and any data their interaction may generate

This policy does not cover internal employer systems, other personal accounts not connected to this portfolio, or any offline activities.

# 3\. Policy Statements (Rules)

The following rules are based on the risks identified in my Risk Register and the control gaps found in my ISO 27001 Control Mapping. Each rule is written to address a specific threat or vulnerability found during the assessment.

## 3.1 Contact Information Protection

- My email address must not be displayed directly (as plain text) on any page of the portfolio website.
- A contact form must be used instead of a visible email address to reduce the risk of automated data scraping by bots.

## 3.2 GitHub Repository Security

- Branch protection must be enabled on the main branch of the portfolio GitHub repository.
- No direct commits should be pushed to the main branch without at least a basic review step, even as a solo developer.
- Repository settings must be reviewed periodically to confirm that only intended information is publicly visible.

## 3.3 Website Availability and Network Protection

- Cloudflare or an equivalent CDN service must be used to protect the website against DDoS attacks and improve availability.
- Any third-party JavaScript libraries or CDN-hosted scripts must come from trusted, well-known sources only (e.g., cdnjs, jsDelivr).
- Subresource Integrity (SRI) attributes should be added to third-party script tags where possible, to detect if an external file has been changed without permission.

## 3.4 Access Control and Sensitive Asset Exposure

- Certification files and sensitive documents must not be accessible through direct cloud links that are easily visible in the page source code.
- Google Drive sharing settings for certificates and documents must be set to 'restricted' or 'anyone with the link' only - not publicly indexed by search engines.
- Any admin tools or backend features added to the portfolio in the future must require authentication before access is granted.

## 3.5 Content Protection

- Images and project work displayed on the portfolio must include a visible watermark or copyright notice to reduce the risk of content being copied without credit.
- A copyright notice must be displayed in the footer section of the website.

## 3.6 Identity and Social Media

- Sensitive personal information such as phone numbers, home address, or government IDs must never be published on the portfolio or any linked social media accounts.
- Social media accounts linked from the portfolio should use the available privacy settings to limit unnecessary data exposure.
- Accounts should not be cross-linked in ways that make it easy to collect and combine personal information across multiple platforms.

## 3.7 Secure Development Practices

- All user-facing forms (such as a contact form) must sanitize and validate inputs to protect against script injection attacks.
- Before publishing any new feature or page update, a basic review of the code should be performed to check for obvious security issues.
- External libraries and packages should be checked for known vulnerabilities before being added to the project.

## 3.8 Logging and Monitoring

- A basic analytics or logging tool (such as Google Analytics or Cloudflare Analytics) must be configured to track visitor activity and detect unusual traffic.
- Any suspicious traffic patterns or unexpected spikes in visits should be reviewed and investigated.

## Appendix A: Risk Register Summary

The table below summarizes the 10 risks identified for the H1t3X portfolio. These risks directly informed the policy rules written in Section 3.

| **ID** | **Asset**          | **Threat**           | **Vulnerability**              | **Risk Level** | **Mitigation**                         |
| ------ | ------------------ | -------------------- | ------------------------------ | -------------- | -------------------------------------- |
| 1      | Contact Info       | Data Scraping        | Email publicly visible         | Medium         | Use contact form                       |
| 2      | GitHub Repo        | Unauthorized Changes | No branch protection           | Medium         | Enable branch protection               |
| 3      | Portfolio Website  | DDoS                 | No CDN protection              | Medium         | Use Cloudflare CDN                     |
| 4      | Portfolio Visitors | Script Injection     | No input validation            | Low            | Sanitize inputs                        |
| 5      | Identity           | Phishing             | Public info exposure           | Medium         | Limit sensitive info                   |
| 6      | Social Media       | Data Scraping        | Accounts publicly visible      | Medium         | Use privacy settings                   |
| 7      | Certifications     | Data Scraping        | Drive links visible on inspect | Medium         | Restrict sharing permissions           |
| 8      | Projects           | Unauthorized Changes | Exposed GitHub repos           | Medium         | Enable branch protection               |
| 9      | Visitors           | Content Misuse       | Easy image download            | Medium         | Add watermark / copyright notice       |
| 10     | Portfolio Website  | Supply Chain Attack  | Third-party JS/CDN dependency  | Medium         | Use trusted sources + integrity checks |

Refer to:  
\- Risk Register ([link](../GRC-Risk-Assessment/Risk_Register%20.xlsx))

## Appendix B: ISO 27001 Control Mapping Summary

The table below shows which ISO 27001 controls were reviewed against the portfolio, whether they are currently implemented, and what action is required.

| **Control ID** | **Control Name**            | **Implemented** | **Action Required**            |
| -------------- | --------------------------- | --------------- | ------------------------------ |
| A.5.1.1        | Information Security Policy | No              | Create basic security policy   |
| A.6.1.1        | Roles & Responsibilities    | Partially       | Define security responsibility |
| A.8.1.1        | Asset Management            | No              | Create asset list              |
| A.9.2.1        | User Access Management      | No              | Add login system               |
| A.9.4.1        | Access Control              | No              | Restrict sensitive areas       |
| A.12.2.1       | Malware Protection          | No              | Use secure hosting/scanning    |
| A.12.4.1       | Logging & Monitoring        | No              | Add analytics / logging        |
| A.13.1.1       | Network Security            | Partially       | Use Cloudflare / CDN           |
| A.14.2.5       | Secure Development          | Partially       | Add code review & validation   |
| A.15.1.1       | Supplier Security           | Partially       | Use trusted providers          |
|                |                             |                 |                                |

Refer to:  
\- ISO Control Mapping ([link](../ISO-27001_Control_Mapping/ISO%2027001%20Control%20Mapping%20Sheet.xlsx))

# 4\. Responsibilities

Since this is a personal portfolio project, I am the primary person responsible for maintaining and following this policy. The table below outlines how responsibilities are split by role, even though the same person (me) fills all of them for now.

| **Role**                        | **Responsibility**                                                                                                                |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Self (Developer / Site Owner)   | Maintain the website, apply and review security controls, keep the Risk Register updated, and ensure this policy stays current.   |
| Hosting Provider (GitHub Pages) | Responsible for platform uptime and infrastructure-level security. Branch protection rules must be configured by the site owner.  |
| CDN Provider (Cloudflare)       | Responsible for network-level protection and DDoS mitigation. Configuration and updates are the responsibility of the site owner. |
| Third-Party Library Authors     | Responsible for the security of their own code. The site owner is responsible for vetting and keeping libraries up to date.       |

This policy and the associated Risk Register will be reviewed at least once every six months, or whenever a significant change is made to the website such as adding a new feature, changing the hosting provider, or linking new external accounts.

# 5\. Enforcement

Because this is a personal portfolio and not a corporate environment, enforcement is self-managed. The following steps will be taken to ensure the rules in this policy are actually followed in practice.

## 5.1 Self-Auditing

- The policy will be reviewed each rule in Section 3 against the actual state of the website at least once every six months.
- I will use a basic checklist to confirm that each control is in place before publishing major updates to the website.

## 5.2 Incident Response

- If I notice any security issue - such as unauthorized changes to the GitHub repository, suspicious traffic, or a broken security control - I will document what happened, fix the issue as quickly as possible, and update the Risk Register if needed.
- Any credentials or access tokens that may have been exposed will be rotated immediately.

## 5.3 Consequences of Non-Compliance

- If a rule in this policy is not followed, whether intentionally or by mistake, the gap will be documented and treated as an open risk in the Risk Register until it is resolved.
- Since this policy is part of my GRC portfolio submission, keeping it accurate and followed is important for the credibility of my overall work.

## 5.4 Policy Review and Updates

- This policy is version-controlled and will be updated whenever the risk environment changes or new controls are added.
- The version number and date will be updated at the top of the document with each revision.

# 6\. Exceptions

Any exceptions to this policy must be documented and justified. All exceptions must be reviewed and approved by the Security Owner.

**Document Control**

**Author:** Hitesh | GRC Analyst (Fresher)

**Portfolio:** hitesh114.github.io/h1t3x

**Version:** 1.0 | April 2026 

**Next Review Date:** October 2026

**Source Documents:** _Risk_Register_.xlsx | ISO*27001_Control_Mapping_Sheet.xlsx*
