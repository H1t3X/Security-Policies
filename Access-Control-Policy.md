**Document Classification:** Public – Portfolio Demonstration  
**Version:** 1.0  
**Last Updated:** April 2026  
**ACCESS CONTROL POLICY**

**H1t3X Portfolio Website**

_hitesh114.github.io/h1t3x_

Owner: Hitesh | Role: GRC Analyst (Fresher) | Version: 1.0 | April 2026

**1\. Purpose**

This policy defines the access control requirements for the H1t3X portfolio website and all connected assets. It establishes who is permitted to access specific resources, under what conditions, and with what level of permission.

This policy is based on ISO 27001 controls A.9.2.1 and A.9.4.1 and is informed by the Risk Register maintained for this portfolio.

**2\. Scope**

This policy applies to:

- The H1t3X portfolio website hosted on GitHub Pages (hitesh114.github.io/h1t3x)
- The GitHub repository used to manage and publish the site
- Google Drive folders containing certification and document assets linked from the portfolio
- Any future admin panel, backend tool, or CMS connected to the portfolio
- All third-party services and libraries integrated into the site

This policy does not apply to employer infrastructure, unrelated personal accounts, or services with no connection to this portfolio.

**3\. Data Classification**

All assets and data associated with the H1t3X portfolio must be classified before access rules are applied. Classification determines the level of protection required.

| **Classification** | **Examples**                                                     | **Access Control Required**                                        |
| ------------------ | ---------------------------------------------------------------- | ------------------------------------------------------------------ |
| **PUBLIC**         | Portfolio pages, project write-ups, skills section, contact form | No authentication required. Read-only for all visitors.            |
| **INTERNAL**       | GitHub repository code, deployment configs, branch settings      | Authentication required. Access limited to site owner only.        |
| **CONFIDENTIAL**   | Certification files on Google Drive, personal identity details   | Restricted sharing only. No public indexing. No open access links. |

Any new asset or data added to the portfolio must be assigned a classification before it is published or shared.

**4\. Policy Rules**

<div class="joplin-table-wrapper"><table><tbody><tr><th><p><strong>🔐 4.1 Authentication - ISO A.9.2.1</strong></p></th></tr><tr><td><ul><li>Access to the GitHub repository must require a valid authenticated account at all times.</li></ul></td></tr><tr><td><ul><li>Two-factor authentication (2FA) must be enabled on the GitHub account used to manage this portfolio.</li></ul></td></tr><tr><td><ul><li>No write access to the repository is permitted without successful authentication.</li></ul></td></tr><tr><td><ul><li>Any future admin panel or backend login added to this portfolio must enforce authentication before granting access.</li></ul></td></tr><tr><td><ul><li>Shared or public devices must not be used to access authenticated areas without logging out immediately after use.</li></ul></td></tr></tbody></table></div>

<div class="joplin-table-wrapper"><table><tbody><tr><th><p><strong>⚖️ 4.2 Authorization - ISO A.9.4.1</strong></p></th></tr><tr><td><ul><li>Visitors to the portfolio website are authorized for read-only access to PUBLIC classified content only.</li></ul></td></tr><tr><td><ul><li>Write access to the GitHub repository is authorized for the site owner role only.</li></ul></td></tr><tr><td><ul><li>CONFIDENTIAL assets (certification files) must not be authorized for unrestricted public access under any circumstances.</li></ul></td></tr><tr><td><ul><li>Google Drive links to certification files must be set to 'Restricted' - accessible only to specific authorized accounts, not to anyone with the link.</li></ul></td></tr><tr><td><ul><li>If a file must be shared externally, it must be moved to INTERNAL classification and a time-limited, revocable link must be used.</li></ul></td></tr><tr><td><ul><li>Input submitted through any website form must be validated and sanitized before it is processed. Unvalidated input must be rejected.</li></ul></td></tr></tbody></table></div>

<div class="joplin-table-wrapper"><table><tbody><tr><th><p><strong>🛡️ 4.3 Least Privilege - ISO A.6.1.1 | A.9.4.1</strong></p></th></tr><tr><td><ul><li>No account, tool, or third-party service must be granted permissions beyond what is strictly required for its function.</li></ul></td></tr><tr><td><ul><li>GitHub Pages deployment must be scoped to the minimum required branch only. Full repository admin access must not be used for deployment.</li></ul></td></tr><tr><td><ul><li>Third-party JavaScript libraries must be loaded from verified, trusted CDN sources only. Libraries must not be granted access to resources beyond their stated function.</li></ul></td></tr><tr><td><ul><li>Subresource Integrity (SRI) attributes must be applied to all external scripts to detect unauthorized modifications.</li></ul></td></tr><tr><td><ul><li>All Google Drive sharing permissions must be reviewed every six months. Links that are no longer needed must be revoked.</li></ul></td></tr><tr><td><ul><li>No elevated or admin-level permissions must remain active on any connected service when not in active use.</li></ul></td></tr></tbody></table></div>

<div class="joplin-table-wrapper"><table><tbody><tr><th><p><strong>👥 4.4 Role-Based Access Control (RBAC) - ISO A.6.1.1</strong></p></th></tr><tr><td><ul><li>Two roles are defined for this portfolio: Public Visitor and Site Owner.</li></ul></td></tr><tr><td><ul><li>The Public Visitor role is permitted read-only access to PUBLIC classified content. No other access is authorized for this role.</li></ul></td></tr><tr><td><ul><li>The Site Owner role is the only role authorized to modify repository content, manage sharing permissions, and configure connected services.</li></ul></td></tr><tr><td><ul><li>No individual must be granted the Site Owner role unless explicitly required. Guest or collaborator access must use a separately defined, limited role.</li></ul></td></tr><tr><td><ul><li>Role assignments must be reviewed every six months. Any role that is no longer required must be revoked.</li></ul></td></tr></tbody></table></div>

<div class="joplin-table-wrapper"><table><tbody><tr><th><p><strong>⏱️ 4.5 Session Control - ISO A.9.2.1 | A.12.4.1</strong></p></th></tr><tr><td><ul><li>All active GitHub sessions must be reviewed monthly via GitHub Settings &gt; Security Log.</li></ul></td></tr><tr><td><ul><li>Any session originating from an unrecognized device or location must be terminated immediately.</li></ul></td></tr><tr><td><ul><li>Any future admin login added to this portfolio must enforce automatic session expiry after a maximum of 30 minutes of inactivity.</li></ul></td></tr><tr><td><ul><li>Upon detection of an unauthorized session, all active sessions must be revoked, credentials must be rotated, and the incident must be recorded.</li></ul></td></tr><tr><td><ul><li>Session tokens or credentials must not be stored in the GitHub repository, public files, or any client-side code.</li></ul></td></tr></tbody></table></div>

**5\. Responsibilities**

| **Role**                  | **Access Level**        | **Responsibility**                                                                                                |
| ------------------------- | ----------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Site Owner**            | Full (Site Owner role)  | Apply and maintain all access control rules. Review permissions, sessions, and role assignments every six months. |
| **GitHub Pages**          | Platform infrastructure | Platform-level hosting security. Repository access rules must be configured by the Site Owner.                    |
| **Google Drive**          | Document storage        | Storage of CONFIDENTIAL assets. Sharing permissions must be set and reviewed by the Site Owner.                   |
| **Third-Party Libraries** | Read-only / scoped      | External code used on the site. Vetting and updates are the responsibility of the Site Owner.                     |
| **Future Collaborators**  | Limited role only       | Must be assigned a defined limited role before access is granted. The Site Owner role must not be shared.         |

**6\. Enforcement**

**6.1 Six-Monthly Self-Audit**

- 2FA must be confirmed active on the GitHub account.
- All Google Drive sharing links must be reviewed and revoked if no longer required.
- All connected service permissions must be checked against the Least Privilege rule.
- Role assignments must be verified as accurate.
- GitHub Security Log must confirm no unauthorized session activity in the past six months.

**6.2 Incident Response**

- Any access control rule found to be violated must be remediated immediately and recorded in the Risk Register.
- Any unauthorized session or access event must result in immediate session revocation and credential rotation.

**6.3 Non-Compliance**

- Any rule not in place is treated as an open risk item in the Risk Register until resolved.
- Policy exceptions must be documented with a justification and reviewed at the next audit cycle.

**6.4 Policy Review Cycle**

- This policy must be reviewed every six months or following any significant change to the portfolio infrastructure.
- Version number and date must be updated in the Document Control section on each revision.

**Appendix: Control & Risk Reference**

| **Policy Rule**         | **ISO 27001 Control**                       | **Risk Register IDs**                                              |
| ----------------------- | ------------------------------------------- | ------------------------------------------------------------------ |
| **4.1 Authentication**  | A.9.2.1 - User Access Management            | Risk 2 (GitHub - Unauthorized Changes), Risk 8 (Projects)          |
| **4.2 Authorization**   | A.9.4.1 - Access Control                    | Risk 7 (Certifications - Data Scraping), Risk 4 (Script Injection) |
| **4.3 Least Privilege** | A.6.1.1 - Roles & Responsibilities, A.9.4.1 | Risk 10 (Supply Chain - Third-Party JS), Risk 7                    |
| **4.4 RBAC**            | A.6.1.1 - Roles & Responsibilities          | Risk 2, Risk 8 (Unauthorized Changes)                              |
| **4.5 Session Control** | A.9.2.1, A.12.4.1 - Logging & Monitoring    | Risk 3 (DDoS / No Monitoring), Risk 2                              |

**Document Control**

**Owner:** Hitesh | GRC Analyst (Fresher)

**Portfolio:** hitesh114.github.io/h1t3x

**Version:** 1.0 | April 2026

**Next Review:** October 2026

**Source Documents:** _Risk_Register_.xlsx | ISO*27001_Control_Mapping_Sheet.xlsx*
