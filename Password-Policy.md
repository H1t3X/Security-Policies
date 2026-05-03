# Password Policy

**Document Owner:** Hitesh (GRC Analyst — Portfolio Project)
**Version:** 1.0
**Date:** May 2026
**Reference Controls:** ISO 27001:2013 — A.9.2.1, A.9.4.1, A.5.1.1

---

## 1. Purpose

The purpose of this policy is to establish basic rules for creating and managing passwords across systems and accounts associated with this portfolio project. Passwords are one of the most fundamental controls in information security, and weak or poorly managed passwords remain a leading cause of unauthorized access incidents.

This policy was developed as part of a GRC (Governance, Risk, and Compliance) portfolio exercise. It is aligned to ISO 27001:2013 controls A.9.2.1 (User Access Management) and A.9.4.1 (Access Control), both of which were identified as **not implemented** in the accompanying ISO 27001 Control Mapping Sheet. It also supports A.5.1.1, which requires a written information security policy to exist.

By defining these rules, the goal is to reduce the risk of unauthorized access to accounts and systems — a risk that appears multiple times in the associated Risk Register (e.g., Risk ID 2: GitHub unauthorized changes, Risk ID 4: Script injection, Risk ID 5: Identity phishing).

---

## 2. Scope

This policy applies to all accounts and platforms used in connection with this portfolio project, including but not limited to:

- **GitHub** — source code repository and version control (hitesh114.github.io)
- **Google Drive** — storage for certifications and shared documents referenced in the portfolio
- **Social media accounts** — any profiles publicly linked from the portfolio website
- **Email accounts** — used for contact or professional communication associated with this project
- **Any third-party tools or services** connected to the above (e.g., Cloudflare, CDN providers)

This policy applies to the portfolio owner (Hitesh) as the sole user and administrator of these systems. If collaborators are added to any of the above platforms in the future, this policy will apply to them as well.

---

## 3. Policy Rules

### 3.1 Password Strength
- All passwords must be at least **12 characters** in length.
- Passwords must include a mix of uppercase letters, lowercase letters, numbers, and at least one special character (e.g., `!`, `@`, `#`, `$`).
- Passwords must not contain the account holder's name, username, or obvious sequences (e.g., `123456`, `password`, `qwerty`).

### 3.2 Password Uniqueness
- Each account or platform must have a **unique password**. Reusing passwords across accounts is not permitted.
- This is especially important for high-value accounts such as GitHub and Google Drive, which are directly referenced in the Risk Register as assets exposed to unauthorized access.

### 3.3 Multi-Factor Authentication (MFA)
- Where the platform supports it, **MFA must be enabled**. This applies to GitHub, Google accounts, and social media accounts.
- MFA adds a second layer of verification beyond the password, significantly reducing the risk of account compromise even if a password is leaked (relevant to Risk ID 5: Phishing).

### 3.4 Password Storage
- Passwords must not be stored in plain text (e.g., in a notes app, spreadsheet, or text file).
- A reputable password manager (e.g., Bitwarden, 1Password) should be used to store and manage passwords securely.

### 3.5 Password Sharing
- Passwords must not be shared with anyone unless operationally required.
- If a password must be temporarily shared, it should be changed immediately afterward.

### 3.6 Password Rotation
- Passwords for critical accounts (GitHub, email, Google Drive) should be reviewed and updated at least **once every 12 months**, or immediately if a breach or compromise is suspected.

### 3.7 Default and Temporary Passwords
- Any default passwords provided by a new service or platform must be changed upon first login.
- Temporary passwords (e.g., received via email reset) must be changed immediately after use.

---

## 4. Responsibilities

Since this is a personal portfolio project with a single owner, the responsibility structure is straightforward. This maps to ISO 27001 control A.6.1.1, which requires that security responsibilities be defined.

| Role | Responsibility |
|---|---|
| **Portfolio Owner (Hitesh)** | Ensuring all accounts comply with this policy; enabling MFA; using a password manager; reviewing and rotating passwords annually |
| **Future Collaborators (if any)** | Following this policy for any accounts or repositories they are granted access to; reporting any suspected password compromise immediately |

In a real organizational context, these responsibilities would typically be distributed across an IT team, a security team, and end users. For the purposes of this portfolio project, all responsibilities are held by the owner.

---

## 5. Enforcement

In an organizational setting, enforcement of a password policy would typically involve technical controls (such as Active Directory group policies, automated password expiry, or Identity and Access Management tools) combined with HR and disciplinary procedures.

For this portfolio project, enforcement is self-managed. The following practical measures are used in place of automated enforcement:

- **Self-audit:** The portfolio owner will conduct a review of all in-scope accounts at least once a year to verify compliance with this policy (e.g., confirming MFA is enabled, passwords are stored in a password manager, no accounts use default credentials).
- **Incident response trigger:** If any account shows signs of compromise (e.g., unusual login notifications, unexpected changes to the GitHub repository), passwords will be changed immediately and MFA tokens reset.
- **Documentation:** Compliance with this policy will be noted in the accompanying ISO 27001 Control Mapping Sheet under controls A.9.2.1 and A.9.4.1 as evidence of implementation.

> **Note for reviewers:** In a production environment, this section would reference specific technical enforcement mechanisms, HR policy consequences, and audit logging. The approach described here reflects the scope and resources of a personal portfolio project.

---

## 6. Exceptions

There may be situations where following this policy in full is not immediately possible — for example, a third-party platform that does not support MFA, or a legacy tool with a maximum password length below 12 characters.

In such cases:
- The exception must be **documented**, including the reason why full compliance is not possible and what compensating controls are in place (e.g., using a longer passphrase if length is limited, or disabling the platform entirely if MFA is unavailable and the account holds sensitive data).
- Exceptions must be **reviewed** as part of the annual self-audit to determine whether the platform has since added support for the required controls.
- Exceptions are not a permanent bypass — they should be resolved as soon as the platform or circumstances allow.

**Current known exceptions:**

| Platform | Exception | Compensating Control | Review Date |
|---|---|---|---|
| None identified at this time | — | — | May 2027 |

---

*This policy will be reviewed annually or following any significant change to the systems in scope.*
