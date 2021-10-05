# Study guide to Exam [SC-300](https://docs.microsoft.com/en-us/learn/certifications/exams/sc-300)

This study guide contains various links to official documentation in order to get certified for the [SC-300](https://docs.microsoft.com/en-us/learn/certifications/exams/sc-300) exam

## [Part 1: Implement an identity management solution](https://docs.microsoft.com/en-us/learn/paths/implement-identity-management-solution/)

### [Implement initial configuration of Azure Active Directory](https://docs.microsoft.com/en-us/learn/modules/implement-initial-configuration-of-azure-active-directory)
- Azure Active Directory roles
    - [Understand roles ](https://docs.microsoft.com/en-us/azure/active-directory/roles/concept-understand-roles)  
    There are about 60 Azure Active Directory (Azure AD) built-in roles, which are roles with a fixed set of role permissions. To supplement the built-in roles, Azure AD also supports custom roles. Azure AD roles are different from other Microsoft 365 roles.  
    ![](/images/role-overlap-diagram.png)
    - [Compare Azure and Azure AD Roles](https://docs.microsoft.com/en-us/azure/role-based-access-control/rbac-and-directory-admin-roles)  
    Explain the difference between Azure roles, Azure Active Directory (Azure AD) roles and Classic subscription administrator roles  
    ![](/images/rbac-admin-roles.png)
    - [Roles for Microsoft 365 services in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/roles/m365-workload-docs)  
    All products in Microsoft 365 can be managed with administrative roles in Azure Active Directory (Azure AD). Some products also provide additional roles that are specific to that product
    - [Assign Azure AD roles to users](https://docs.microsoft.com/en-us/azure/active-directory/roles/manage-roles-portal)  
    To grant access to users in Azure Active Directory (Azure AD), you assign Azure AD roles. A role is a collection of permissions.
    - [Use Azure AD groups to manage role assignments](https://docs.microsoft.com/en-us/azure/active-directory/roles/groups-concept)  
    Azure Active Directory (Azure AD) lets you target Azure AD groups for role assignments. Assigning roles to groups can simplify the management of role assignments in Azure AD with minimal effort from your Global Administrators and Privileged Role Administrators.
    ![](/images/role-assignable-group.png)
    - [Azure AD built-in roles](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference)  
    This article lists the Azure AD built-in roles you can assign to allow management of Azure AD resources.
    - [Custom Roles](https://docs.microsoft.com/en-us/azure/active-directory/roles/custom-create)  
    This article describes how to create new custom roles in Azure Active Directory (Azure AD). For the basics of custom roles, see the [custom roles overview](https://docs.microsoft.com/en-us/azure/active-directory/roles/custom-overview). The role can be assigned either at the directory-level scope or an app registration resource scope only.  
    ![](/images/rbac-overview.png)
    - [Develop a security plan](https://docs.microsoft.com/en-us/azure/active-directory/roles/security-planning)  
    Microsoft recommends that you develop and follow a roadmap to secure privileged access against cyber attackers.
    - [Establish emergency accounts](https://docs.microsoft.com/en-us/azure/active-directory/roles/security-emergency-access)  
    It is important that you prevent being accidentally locked out of your Azure Active Directory (Azure AD) organization because you can't sign in or activate another user's account as an administrator. You can mitigate the impact of accidental lack of administrative access by creating two or more emergency access accounts in your organization.
- Custom domains
    - [Add your custom domain name](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/add-custom-domain)  
    Every new Azure AD tenant comes with an initial domain name, <domainname>.onmicrosoft.com. You can't change or delete the initial domain name, but you can add your organization's names. Adding custom domain names helps you to create user names that are familiar to your users, such as alain@contoso.com.
    - [Managing custom domain names](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/domains-manage)  
        - Set the primary domain name for your Azure AD organization
        - Add custom domain names to your Azure AD organization
        - Add subdomains of a custom domain
        - What to do if you change the DNS registrar for your custom domain name
        - Delete a custom domain name
    - [Verify a custom subdomain](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/domains-verify-custom-subdomain)  
    After a root domain is added to Azure Active Directory (Azure AD), all subsequent subdomains added to that root in your Azure AD organization automatically inherit the authentication setting from the root domain. However, if you want to manage domain authentication settings independently from the root domain settings, you can now with the Microsoft Graph API. For example, if you have a federated root domain such as contoso.com, this article can help you verify a subdomain such as child.contoso.com as managed instead of federated.
    - [Self-service sign-up for Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/directory-self-service-signup)  
    This article explains how to use self-service sign-up to populate an organization in Azure Active Directory (Azure AD). If you want to take over a domain name from an unmanaged Azure AD organization, see [Take over an unmanaged tenant as administrator](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/domains-admin-takeover).
- Device registration
    - [Azure AD registered devices](https://docs.microsoft.com/en-us/azure/active-directory/devices/concept-azure-ad-register)  
    The goal of Azure AD registered devices is to provide your users with support for the bring your own device (BYOD) or mobile device scenarios. In these scenarios, a user can access your organization’s resources using a personal device.  
    ![](/images/azure-ad-registered-device.png)
    - [Azure AD joined devices](https://docs.microsoft.com/en-us/azure/active-directory/devices/concept-azure-ad-join)  
    Azure AD join is primarily intended for organizations that do not have an on-premises Windows Server Active Directory infrastructure  
    ![](/images/azure-ad-joined-device.png)
    - [Hybrid Azure AD joined devices](https://docs.microsoft.com/en-us/azure/active-directory/devices/concept-azure-ad-join-hybrid)  
    These devices are joined to your on-premises Active Directory and registered with Azure Active Directory.  
    ![](/images/azure-ad-hybrid-joined-device.png)
    - [How SSO to on-premises resources works on Azure AD joined devices](https://docs.microsoft.com/en-us/azure/active-directory/devices/azuread-join-sso)  
    If your environment has an on-premises Active Directory (AD), you can also get SSO experience on Azure AD joined devices to resources and applications that rely on on-premises AD. This article explains how this works.
- Delegation by using administrative units
    - [Administrative units](https://docs.microsoft.com/en-us/azure/active-directory/roles/administrative-units)  
    An administrative unit is an Azure AD resource that can be a container for other Azure AD resources. An administrative unit can contain only users and groups. Administrative units restrict permissions in a role to any portion of your organization that you define. You could, for example, use administrative units to delegate the Helpdesk Administrator role to regional support specialists, so they can manage users only in the region that they support.
    - [Delegate app registration permissions](https://docs.microsoft.com/en-us/azure/active-directory/roles/delegate-app-roles)  
        - Restrict who can create applications
        - Assign application owners
        - Assign built-in application admin roles
        - Create and assign a custom role (preview)
- Tenant-wide settings
    - [Default user permissions (members and guests)](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/users-default-permissions)  
    In Azure Active Directory (Azure AD), all users are granted a set of default permissions. A user’s access consists of the type of user, their role assignments, and their ownership of individual objects. This article describes those default permissions and contains a comparison of the member and guest user defaults. The default user permissions can be changed only in user settings in Azure AD. The article also contains a comparison between member and guest default permissions.
    - [Sign in with LinkedIn](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/linkedin-integration)  
    You can allow users in your organization to access their LinkedIn connections within some Microsoft apps. No data is shared until users consent to connect their accounts. 
    - [Security defaults](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)  
    Managing security can be difficult with common identity-related attacks like password spray, replay, and phishing becoming more popular. Security defaults make it easier to help protect your organization from these attacks with preconfigured security settings
    - [Configure B2B external collaboration settings](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/delegate-invitations)  
    By default, all users and guests in your directory can invite guests even if they're not assigned to an admin role. External collaboration settings let you turn guest invitations on or off for different types of users in your organization. You can also delegate invitations to individual users by assigning roles that allow them to invite guests. Azure AD allows you to restrict what external guest users can see in your Azure AD directory. By default, guest users are set to a limited permission level that blocks them from enumerating users, groups, or other directory resources, but lets them see membership of non-hidden groups.
    - [Add your organization's privacy info](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-properties-area)  
    We strongly recommend you add both your global privacy contact and your organization's privacy statement, so your internal employees and external guests can review your policies. Because privacy statements are uniquely created and tailored for each business, we strongly recommend you contact a lawyer for assistance.  
    ![](/images/active-directory-no-privacy-statement-or-contact.png)

### [Create, configure, and manage identities](https://docs.microsoft.com/en-us/learn/modules/create-configure-manage-identities/)
- Manage users
    - [Add or delete users](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/add-users-azure-active-directory)
    - [Restore or remove a recently deleted user](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-users-restore)
- Manage groups
    - [Create a basic group and add members](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
    - [Add or remove a group from another group](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-groups-membership-azure-portal)
- Manage licenses
    - [Assign or remove licenses](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/license-users-groups)
    - [Assign or remove licenses to users](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/license-users-groups?context=/azure/active-directory/enterprise-users/context/ugr-context)
    - [Assign licenses to users by group membership](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/licensing-groups-assign)
    - [What is group-based licensing in Azure Active Directory?](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal)
    - [Identify and resolve license assignment problems for a group](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/licensing-groups-resolve-problems)
    - [How to migrate users with individual licenses to groups for licensing](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/licensing-groups-migrate-users)
    - [Scenarios, limitations, and known issues using groups to manage licensing](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/licensing-group-advanced)

### [Implement and manage external identities](https://docs.microsoft.com/en-us/learn/modules/implement-manage-external-identities/)
- Manage external collaboration
    - [What is guest user access?](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/what-is-b2b)
    - [Configure B2B external collaboration settings](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/delegate-invitations)
- Invite external users - individually and in bulk
    - [Add Azure Active Directory B2B collaboration users](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/add-users-administrator)
    - [Bulk invite Azure AD B2B collaboration users](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/tutorial-bulk-invite)
    - [Invitation email](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/invitation-email-elements)
    - [Invitation redemption experience](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/redemption-experience)
- Manage external user accounts in Azure Active Directory
    - [Properties of an Azure Active Directory B2B collaboration user](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/user-properties)
    - [Microsoft 365 external sharing and Azure Active Directory (Azure AD) B2B collaboration](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/o365-external-user)
- Dynamic groups
    - [Create or update a dynamic group](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/groups-create-rule)
    - [Dynamic membership rules for groups](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/groups-dynamic-membership)
- Configure identity providers
    - [Azure Active Directory (Azure AD) identity provider](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/azure-ad-account)
    - [Microsoft account (MSA) identity provider](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/microsoft-account)
    - [Add Google as an identity provider for B2B guest users](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/google-federation)
    - [Add Facebook as an identity provider for External Identities](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/facebook-federation)
    - [Federation with SAML/WS-Fed identity providers for guest users](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/direct-federation)

### [Implement and manage hybrid identity](https://docs.microsoft.com/en-us/learn/modules/implement-manage-hybrid-identity/)
- Azure AD Connect
    - [What is Seamless Single Sign-On/SSO?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sso)
    - [How does Seamless SSO work?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sso-how-it-works)
    - [What is Azure AD Connect?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-azure-ad-connect)
    - [Choose the right authentication method (decision tree)](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/choose-ad-authn)
    - [Azure AD Connect and Azure AD Connect Health installation roadmap](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-roadmap)
- Password hash synchronization (PHS)
    - [What is password hash synchronization?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-phs)
    - [How password hash synchronization works](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization)
    - [Troubleshoot password hash synchronization](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization)
    - [Getting started with Azure AD Connect using express settings (password hash synchronization)](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-express)
- Pass-through authentication (PTA)
    - [What is Pass-through Authentication?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta)
    - [How does Pass-through Authentication work?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-how-it-works)
    - [Current limitations](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-current-limitations)
    - [Security deep dive](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-security-deep-dive)
    - [Deploy Azure AD Pass-through Authentication](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-quick-start)
- Implement and manage federation
    - [What is federation?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-fed)
    - [How federation works](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-fed-whatis)
    - [Configuring federation with AD FS](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-custom#configuring-federation-with-ad-fs)
    - [Manage and customize ADFS by using Azure AD Connect](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-fed-management)
- Trouble-shoot synchronization errors
    - [Troubleshoot password hash synchronization](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization)
    - [Troubleshoot Pass-through Authentication](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-pass-through-authentication)
    - [Troubleshooting Errors during synchronization](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-sync-errors)
    - [Troubleshoot an object that is not synchronizing](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-object-not-syncing)
    - [Troubleshoot an attribute not synchronizing in Azure AD Connect](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-attribute-not-syncing)
- Azure AD Connect Health
    - [What is Azure AD Connect Health?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-azure-ad-connect#what-is-azure-ad-connect-health)
    - [Why use Azure AD Connect Health?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-azure-ad-connect#why-use-azure-ad-connect-health)
    - [Azure AD Connect Health agent installation](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-health-agent-install)
    - [Azure AD Connect Health operations](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-health-operations)
    - [Monitor Azure AD Connect sync with Azure AD Connect Health](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-health-sync)
    - [Diagnose and remediate duplicated attribute sync errors](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-health-diagnose-sync-errors)


## [Part 2: Implement an Authentication and Access Management solution](https://docs.microsoft.com/en-us/learn/paths/implement-authentication-access-management-solution/)

### [Secure Azure Active Directory users with Multi-Factor Authentication](https://docs.microsoft.com/en-us/learn/modules/secure-aad-users-with-mfa/)
- What is Azure AD Multi-Factor Authentication?
    - [How MFA works](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-howitworks)
    - [How to get MFA](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-licensing)
    - [Enable per-user MFA](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-mfa-userstates)
    - [Configure MFA settings](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-mfa-mfasettings)
- Plan your multi-factor authentication deployment
    - [Deployment guide](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-mfa-getstarted)
    - [What authentication and verification methods are available in Azure Active Directory?](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-authentication-methods)
    - [Plan a Conditional Access deployment](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/plan-conditional-access)
    - [Supported device compliance partners](https://docs.microsoft.com/en-us/mem/intune/protect/device-compliance-partners#supported-device-compliance-partners)
    - [Optimize reauthentication prompts and understand session lifetime for MFA](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concepts-azure-multi-factor-authentication-prompts-session-lifetime)
    - [Combined registration for SSPR and Azure AD MFA](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-registration-mfa-sspr-combined)
    - [Configure the Azure AD Multi-Factor Authentication registration policy](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-configure-mfa-policy)
    - [Communication templates](https://aka.ms/mfatemplates)
    - [End-user documentation](https://support.microsoft.com/en-us/account-billing/set-up-your-security-info-from-a-sign-in-prompt-28180870-c256-4ebf-8bd7-5335571bf9a8)
- Configure multi-factor authentication methods
    - [What authentication and verification methods are available in Azure Active Directory?](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-authentication-methods)

### [Manage user authentication](https://docs.microsoft.com/en-us/learn/modules/manage-user-authentication/)
- Administer FIDO2 and passwordless authentication methods
    - [What are FIDO2 security keys?](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-authentication-passwordless#fido2-security-keys)
    - [Enable passwordless security key sign-in](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-authentication-passwordless-security-key)
- Implement an authentication solution based on Windows Hello for Business
    - [How Windows Hello for Business works in Windows Devices](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-how-it-works)
    - [Why a PIN is better than a password](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-why-pin-is-better-than-password)
    - [Windows Hello for Business Deployment Overview](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-deployment-guide)
- Exercise configure and deploy self-service password reset
    - [How it works: Azure AD self-service password reset](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-sspr-howitworks)
    - [Enable users to unlock their account or reset passwords using Azure AD self-service password reset](https://docs.microsoft.com/en-us/azure/active-directory/authentication/tutorial-enable-sspr)
    - [How does self-service password reset writeback work in Azure Active Directory?](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-sspr-writeback)
    - [Plan an Azure Active Directory self-service password reset deployment](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-sspr-deployment)
- Deploy and manage password protection
    - [Eliminate weak passwords in the cloud](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-password-ban-bad)
    - [Eliminate weak passwords on-premises](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-password-ban-bad-on-premises)
    - [Plan and deploy on-premises Azure Active Directory Password Protection](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-password-ban-bad-on-premises-deploy)
    - [Enable on-premises Azure Active Directory Password Protection](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-password-ban-bad-on-premises-operations)
- Implement and manage tenant restrictions
    - [Use tenant restrictions to manage access to SaaS cloud applications](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/tenant-restrictions)

### [Plan, implement, and administer Conditional Access](https://docs.microsoft.com/en-us/learn/modules/plan-implement-administer-conditional-access/)
- Plan security defaults
    - [What are security defaults?](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)
    - [Introducing security defaults](https://techcommunity.microsoft.com/t5/azure-active-directory-identity/introducing-security-defaults/ba-p/1061414)
- Plan Conditional Access policies
    - [What is Conditional Access?](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/overview)
    - [Plan a Conditional Access deployment](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/plan-conditional-access)
    - [Manage external access with Conditional Access policies](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/7-secure-access-conditional-access)
    - [Emergency access or break-glass accounts](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-policy-block-access#user-exclusions)
    - [Require terms of use](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/terms-of-use)
- Implement Conditional Access policy controls and assignments
    - [Common Conditional Access policies](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-policy-common)
    - [Sign-in risk-based Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-policy-risk)
    - [User risk-based Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-policy-risk-user)
    - [Building a Conditional Access policy](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-policies)
    - [User and group assignment](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-users-groups)
- Test and troubleshoot Conditional Access policies
    - [Troubleshoot using the What If tool in Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/what-if-tool)
    - [Troubleshooting sign-in problems with Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/troubleshoot-conditional-access)
    - [Troubleshooting Conditional Access policy changes](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/troubleshoot-policy-changes-audit-log)
    - [Monitor and troubleshoot continuous access evaluation](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-continuous-access-evaluation-troubleshoot)
- Implement application controls
    - [Conditional Access: Cloud apps, actions, and authentication context](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-cloud-apps)
    - [Protect apps with Microsoft Cloud App Security Conditional Access App Control](https://docs.microsoft.com/en-us/cloud-app-security/proxy-intro-aad)
    - [Require app protection policy and an approved client app for cloud app access with Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/app-protection-based-conditional-access)
- Implement session management
    - [Conditional Access: Session](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-session)
    - [Deploy Conditional Access App Control for featured apps](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)
    - [Onboard and deploy Conditional Access App Control for any app](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-any-app)
- Configure smart lockout thresholds
    - [Protect user accounts from attacks with Azure Active Directory smart lockout](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-password-smart-lockout)

### [Manage Azure AD Identity Protection](https://docs.microsoft.com/en-us/learn/modules/manage-azure-active-directory-identity-protection/)
- Review identity protection basics
    - [What is Identity Protection?](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/overview-identity-protection)
    - [Security overview](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/concept-identity-protection-security-overview)
    - [What are risks?](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/concept-identity-protection-risks)
- Implement and manage user risk policy
    - [Identity Protection policies](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/concept-identity-protection-policies)
    - [Configure and enable risk policies](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-configure-risk-policies)
- Configure Azure Active Directory multi-factor authentication registration policy
    - [Configure the Azure AD Multi-Factor Authentication registration policy](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-configure-mfa-policy)
- Monitor, investigate, and remediate elevated risky users
    - [Configure notifications](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-configure-notifications)
    - [How To: Investigate risk](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-investigate-risk)
    - [Remediate risks and unblock users](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-remediate-unblock)

## [Part 3: Implement Access Management for Apps](https://docs.microsoft.com/en-us/learn/paths/implement-access-management-for-apps/)

### [Plan and design the integration of enterprise apps for SSO](https://docs.microsoft.com/en-us/learn/modules/plan-design-integration-of-enterprise-apps-for-sso/)
- Discover apps by using Microsoft Cloud App Security and Active Directory Federation Services app report
- Implement access management for apps
- Design and implement app management roles
- Create a custom role to manage app registration
- Configure pre-integrated gallery SaaS apps

### [Implement and monitor the integration of enterprise apps for SSO](https://docs.microsoft.com/en-us/learn/modules/implement-monitor-integration-of-enterprise-apps-for-sso/)
- Implement token customizations
- Implement and configure consent settings
- Integrate on-premises apps by using Azure Active Directory application proxy
- Integrate custom SaaS apps for single sign-on
- Implement application user provisioning
- Monitor and audit access to Azure Active Directory integrated applications

### [Implement app registration](https://docs.microsoft.com/en-us/learn/modules/implement-app-registration/)
- Plan your line of business application registration strategy
- Implement application registration
- Configure application permission
- Grant tenant-wide admin consent to an application
- Implement application authorization
- Add app roles to application and receive tokens

## [Part 4: Plan and implement an identity governance strategy](https://docs.microsoft.com/en-us/learn/paths/plan-implement-identity-governance-strategy/)

### [Plan and implement entitlement management](https://docs.microsoft.com/en-us/learn/modules/plan-implement-entitlement-management/)
- Define access packages
- Exercise create and manage a resource catalog with Azure AD entitlement
- Configure entitlement management
- Add terms of use acceptance report
- Manage the lifecycle of external users with Azure AD identity governance

### [Plan, implement, and manage access review](https://docs.microsoft.com/en-us/learn/modules/plan-implement-manage-access-review/)
- Plan for access reviews
- Create access reviews for groups and apps
- Monitor access review findings
- Manage licenses for access reviews
- Automate access review management tasks
- Configure recurring access reviews

### [Plan and implement privileged access](https://docs.microsoft.com/en-us/learn/modules/plan-implement-privileged-access/)
- Define a privileged access strategy for administrative users
- Configure Privileged Identity Management for Azure resources
- Configure Privileged Identity Management for Azure Active Directory roles
- Assign Azure Active Directory roles in Privileged Identity Management
- Assign Azure resource roles in Privileged Identity Management
- Analyze Privileged Identity Management audit history and reports
- Create and manage emergency access accounts

### [Monitor and maintain Azure Active Directory](https://docs.microsoft.com/en-us/learn/modules/monitor-maintain-azure-active-directory/)
- Analyze and investigate sign-in logs to troubleshoot access issues
- Review and monitor Azure Active Directory audit logs
- Connect data from Azure Active Directory to Azure Sentinel
- Export logs to third-party security information and event management system
- Analyze Azure Active Directory workbooks and reporting
- Configure notifications