# Study guide to Exam [SC-300](https://docs.microsoft.com/en-us/learn/certifications/exams/sc-300)

This study guide contains various links to official documentation in order to get certified for the [SC-300](https://docs.microsoft.com/en-us/learn/certifications/exams/sc-300) exam

## [Part 1: Implement an identity management solution](https://docs.microsoft.com/en-us/learn/paths/implement-identity-management-solution/)

### [Implement initial configuration of Azure Active Directory](https://docs.microsoft.com/en-us/learn/modules/implement-initial-configuration-of-azure-active-directory)

- Azure Active Directory roles
  - [Understand roles](https://docs.microsoft.com/en-us/azure/active-directory/roles/concept-understand-roles)  
    There are about 60 Azure Active Directory (Azure AD) built-in roles, which are roles with a fixed set of role permissions. To supplement the built-in roles, Azure AD also supports custom roles. Azure AD roles are different from other Microsoft 365 roles.  
    ![Understand roles](/images/role-overlap-diagram.png)
  - [Compare Azure and Azure AD Roles](https://docs.microsoft.com/en-us/azure/role-based-access-control/rbac-and-directory-admin-roles)  
    Explain the difference between Azure roles, Azure Active Directory (Azure AD) roles and Classic subscription administrator roles  
    ![RBAC Admin roles](/images/rbac-admin-roles.png)
  - [Roles for Microsoft 365 services in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/roles/m365-workload-docs)  
    All products in Microsoft 365 can be managed with administrative roles in Azure Active Directory (Azure AD). Some products also provide additional roles that are specific to that product
  - [Assign Azure AD roles to users](https://docs.microsoft.com/en-us/azure/active-directory/roles/manage-roles-portal)  
    To grant access to users in Azure Active Directory (Azure AD), you assign Azure AD roles. A role is a collection of permissions.
  - [Use Azure AD groups to manage role assignments](https://docs.microsoft.com/en-us/azure/active-directory/roles/groups-concept)  
    Azure Active Directory (Azure AD) lets you target Azure AD groups for role assignments. Assigning roles to groups can simplify the management of role assignments in Azure AD with minimal effort from your Global Administrators and Privileged Role Administrators.
    ![Role assignable groups](/images/role-assignable-group.png)
  - [Azure AD built-in roles](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference)  
    This article lists the Azure AD built-in roles you can assign to allow management of Azure AD resources.
  - [Custom Roles](https://docs.microsoft.com/en-us/azure/active-directory/roles/custom-create)  
    This article describes how to create new custom roles in Azure Active Directory (Azure AD). For the basics of custom roles, see the [custom roles overview](https://docs.microsoft.com/en-us/azure/active-directory/roles/custom-overview). The role can be assigned either at the directory-level scope or an app registration resource scope only.  
    ![RBAC Overview](/images/rbac-overview.png)
  - [Develop a security plan](https://docs.microsoft.com/en-us/azure/active-directory/roles/security-planning)  
    Microsoft recommends that you develop and follow a roadmap to secure privileged access against cyber attackers.
  - [Establish emergency accounts](https://docs.microsoft.com/en-us/azure/active-directory/roles/security-emergency-access)  
    It is important that you prevent being accidentally locked out of your Azure Active Directory (Azure AD) organization because you can't sign in or activate another user's account as an administrator. You can mitigate the impact of accidental lack of administrative access by creating two or more emergency access accounts in your organization.
- Custom domains
  - [Add your custom domain name](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/add-custom-domain)  
    Every new Azure AD tenant comes with an initial domain name, \<domainname>.onmicrosoft.com. You can't change or delete the initial domain name, but you can add your organization's names. Adding custom domain names helps you to create user names that are familiar to your users, such as alain@contoso.com.
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
    ![Azure AD registered device](/images/azure-ad-registered-device.png)
  - [Azure AD joined devices](https://docs.microsoft.com/en-us/azure/active-directory/devices/concept-azure-ad-join)  
    Azure AD join is primarily intended for organizations that do not have an on-premises Windows Server Active Directory infrastructure  
    ![Azure AD joined device](/images/azure-ad-joined-device.png)
  - [Hybrid Azure AD joined devices](https://docs.microsoft.com/en-us/azure/active-directory/devices/concept-azure-ad-join-hybrid)  
    These devices are joined to your on-premises Active Directory and registered with Azure Active Directory.  
    ![Azure AD Hybrid joined device](/images/azure-ad-hybrid-joined-device.png)
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
    ![Privacy statement](/images/active-directory-no-privacy-statement-or-contact.png)

### [Create, configure, and manage identities](https://docs.microsoft.com/en-us/learn/modules/create-configure-manage-identities/)

- Manage users
  - [Add or delete users](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/add-users-azure-active-directory)  
    Add new users or delete existing users from your Azure Active Directory (Azure AD) organization. To add or delete users you must be a User administrator or Global administrator.
  - [Restore or remove a recently deleted user](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-users-restore)  
    After you delete a user, the account remains in a suspended state for 30 days. During that 30-day window, the user account can be restored, along with all its properties. After that 30-day window passes, the permanent deletion process is automatically started. You can view your restorable users, restore a deleted user, or permanently delete a user using Azure Active Directory (Azure AD) in the Azure portal.
- Manage groups
  - [Create a basic group and add members](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)  
    There are several group and membership types. The article explains each group (security/Microsoft 365) and membership type (assigned/dynamic user/dynamic device) and why they are used, to help you decide which options to use when you create a group.
  - [Add or remove a group from another group](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-groups-membership-azure-portal)  
    You can add an existing Security group to another existing Security group (also known as nested groups), creating a member group (subgroup) and a parent group. The member group inherits the attributes and properties of the parent group, saving you configuration time.
- Manage licenses
  - [Assign or remove licenses](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/license-users-groups)  
    Many Azure Active Directory (Azure AD) services require you to license each of your users or groups (and associated members) for that service. Only users with active licenses will be able to access and use the licensed Azure AD services for which that's true. Licenses are applied per tenant and do not transfer to other tenants.
  - [Assign licenses to users by group membership](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/licensing-groups-assign)  
    This article walks you through assigning product licenses to a group of users and verifying that they're licensed correctly in Azure Active Directory (Azure AD).
  - [What is group-based licensing in Azure Active Directory?](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal)  
    Azure AD now includes group-based licensing. You can assign one or more product licenses to a group. Azure AD ensures that the licenses are assigned to all members of the group. Any new members who join the group are assigned the appropriate licenses. When they leave the group, those licenses are removed. This licensing management eliminates the need for automating license management via PowerShell to reflect changes in the organization and departmental structure on a per-user basis.
  - [Identify and resolve license assignment problems for a group](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/licensing-groups-resolve-problems)  
    Group-based licensing in Azure Active Directory (Azure AD) introduces the concept of users in a licensing error state. In this article, we explain the reasons why users might end up in this state.
  - [How to migrate users with individual licenses to groups for licensing](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/licensing-groups-migrate-users)  
    You may have existing licenses deployed to users in the organizations via direct assignment; that is, using PowerShell scripts or other tools to assign individual user licenses. Before you begin using group-based licensing to manage licenses in your organization, you can use this migration plan to seamlessly replace existing solutions with group-based licensing.
  - [Scenarios, limitations, and known issues using groups to manage licensing](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/licensing-group-advanced)  
    Use the following information and examples to gain a more advanced understanding of Azure Active Directory (Azure AD) group-based licensing.

### [Implement and manage external identities](https://docs.microsoft.com/en-us/learn/modules/implement-manage-external-identities/)

- Manage external collaboration
  - [What is guest user access?](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/what-is-b2b)  
    Azure Active Directory (Azure AD) business-to-business (B2B) collaboration is a feature within External Identities that lets you invite guest users to collaborate with your organization. With B2B collaboration, you can securely share your company's applications and services with guest users from any other organization, while maintaining control over your own corporate data.
  - [Configure B2B external collaboration settings](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/delegate-invitations)  
    By default, all users and guests in your directory can invite guests even if they're not assigned to an admin role. External collaboration settings let you turn guest invitations on or off for different types of users in your organization. You can also delegate invitations to individual users by assigning roles that allow them to invite guests.
- Invite external users - individually and in bulk
  - [Add Azure Active Directory B2B collaboration users](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/add-users-administrator)  
    As a user who is assigned any of the limited administrator directory roles, you can use the Azure portal to invite B2B collaboration users. You can invite guest users to the directory, to a group, or to an application. After you invite a user through any of these methods, the invited user's account is added to Azure Active Directory (Azure AD), with a user type of Guest. The guest user must then redeem their invitation to access resources. An invitation of a user does not expire.
  - [Bulk invite Azure AD B2B collaboration users](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/tutorial-bulk-invite)  
    If you use Azure Active Directory (Azure AD) B2B collaboration to work with external partners, you can invite multiple guest users to your organization at the same time.
  - [Invitation email](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/invitation-email-elements)  
    Invitation emails are a critical component to bring partners on board as B2B collaboration users in Azure AD. While it’s not required that you send an email to invite someone using B2B collaboration, doing so gives the user all the information they need to make a decision about whether to accept your invite. It also gives them a link they can always refer to in the future when they need to return to your resources.
  - [Invitation redemption experience](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/redemption-experience)  
    This article describes the ways guest users can access your resources and the consent process they'll encounter. If you send an invitation email to the guest, the invitation includes a link the guest can redeem to get access to your app or portal.
- Manage external user accounts in Azure Active Directory
  - [Properties of an Azure Active Directory B2B collaboration user](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/user-properties)  
    This article describes the properties and states of an invited Azure Active Directory B2B (Azure AD B2B) collaboration user object both before and after invitation redemption. An Azure AD B2B collaboration user is an external user, typically from a partner organization, that you invite to sign into your Azure AD organization using their own credentials. This B2B collaboration user (also generally referred to as a guest user) can then access the apps and resources you want to share with them. A user object is created for the B2B collaboration user in the same directory as your employees. B2B collaboration user objects have limited privileges in your directory by default, and they can be managed like employees, added to groups, and so on.  
    ![Redemption diagram](/images/redemption-diagram.png)
  - [Microsoft 365 external sharing and Azure Active Directory (Azure AD) B2B collaboration](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/o365-external-user)  
    This article explains how Azure AD B2B differs from external sharing in SharePoint Online
- Dynamic groups
  - [Create or update a dynamic group](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/groups-create-rule)  
    In Azure Active Directory (Azure AD), you can use rules to determine group membership based on user or device properties. This article tells how to set up a rule for a dynamic group in the Azure portal. Dynamic membership is supported for security groups or Microsoft 365 Groups. When a group membership rule is applied, user and device attributes are evaluated for matches with the membership rule. When an attribute changes for a user or device, all dynamic group rules in the organization are processed for membership changes.
  - [Dynamic membership rules for groups](https://docs.microsoft.com/en-us/azure/active-directory/enterprise-users/groups-dynamic-membership)  
    Dynamic group membership reduces the administrative overhead of adding and removing users. This article details the properties and syntax to create dynamic membership rules for users or devices.
- Configure identity providers
  - [Azure Active Directory (Azure AD) identity provider](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/azure-ad-account)  
    Azure Active Directory is available as an identity provider option for B2B collaboration by default. If an external guest user has an Azure AD account through work or school, they can redeem your B2B collaboration invitations or complete your sign-up user flows using their Azure AD account.
  - [Microsoft account (MSA) identity provider](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/microsoft-account)  
    Your B2B guest users can use their own personal Microsoft accounts for B2B collaboration without further configuration. Guest users can redeem your B2B collaboration invitations or complete your sign-up user flows using their personal Microsoft account.
  - [Add Google as an identity provider for B2B guest users](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/google-federation)  
    By setting up federation with Google, you can allow invited users to sign in to your shared apps and resources with their own Gmail accounts, without having to create Microsoft accounts.
  - [Add Facebook as an identity provider for External Identities](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/facebook-federation)  
    You can add Facebook to your self-service sign-up user flows so that users can sign in to your applications using their own Facebook accounts. To allow users to sign in using Facebook, you'll first need to enable self-service sign-up for your tenant. After you add Facebook as an identity provider, set up a user flow for the application and select Facebook as one of the sign-in options.
  - [Federation with SAML/WS-Fed identity providers for guest users](https://docs.microsoft.com/en-us/azure/active-directory/external-identities/direct-federation)  
    This article describes how to set up federation with any organization whose identity provider (IdP) supports the SAML 2.0 or WS-Fed protocol. When you set up federation with a partner's IdP, new guest users from that domain can use their own IdP-managed organizational account to sign in to your Azure AD tenant and start collaborating with you. There's no need for the guest user to create a separate Azure AD account.

### [Implement and manage hybrid identity](https://docs.microsoft.com/en-us/learn/modules/implement-manage-hybrid-identity/)

- Azure AD Connect
  - [What is Seamless Single Sign-On/SSO?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sso)  
    Azure Active Directory Seamless Single Sign-On (Azure AD Seamless SSO) automatically signs users in when they are on their corporate devices connected to your corporate network. When enabled, users don't need to type in their passwords to sign in to Azure AD, and usually, even type in their usernames. This feature provides your users easy access to your cloud-based applications without needing any additional on-premises components.
  - [How does Seamless SSO work?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sso-how-it-works)  
    This article gives you technical details into how the Azure Active Directory Seamless Single Sign-On (Seamless SSO) feature works.  
    ![SSO](/images/sso1.png)
  - [What is Azure AD Connect?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-azure-ad-connect)  
    Azure AD Connect is the Microsoft tool designed to do:
    - Password hash synchronization - A sign-in method that synchronizes a hash of a users on-premises AD password with Azure AD.
    - Pass-through authentication - A sign-in method that allows users to use the same password on-premises and in the cloud, but doesn't require the additional infrastructure of a federated environment.
    - Federation integration - Federation is an optional part of Azure AD Connect and can be used to configure a hybrid environment using an on-premises AD FS infrastructure. It also provides AD FS management capabilities such as certificate renewal and additional AD FS server deployments.
    - Synchronization - Responsible for creating users, groups, and other objects. As well as, making sure identity information for your on-premises users and groups is matching the cloud. This synchronization also includes password hashes.
    - Health Monitoring - Azure AD Connect Health can provide robust monitoring and provide a central location in the Azure portal to view this activity.
  - [Choose the right authentication method (decision tree)](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/choose-ad-authn)  
    Choosing the correct authentication method is the first concern for organizations wanting to move their apps to the cloud.  
    ![Authentication methods](/images/azure-ad-authn-image1.png)
  - [Azure AD Connect and Azure AD Connect Health installation roadmap](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-roadmap)
- Password hash synchronization (PHS)
  - [What is password hash synchronization?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-phs)  
    Azure AD Connect synchronizes a hash, of the hash, of a user's password from an on-premises Active Directory instance to a cloud-based Azure AD instance.  
    ![Password hash synchronization](/images/arch1.png)
  - [How password hash synchronization works](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization)  
    This article provides information that you need to synchronize your user passwords from an on-premises Active Directory instance to a cloud-based Azure Active Directory (Azure AD) instance.  
    ![How does it work](/images/arch3d.png)
  - [Troubleshoot password hash synchronization](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization)  
    This topic provides steps for how to troubleshoot issues with password hash synchronization. If passwords are not synchronizing as expected, it can be either for a subset of users or for all users.
  - [Getting started with Azure AD Connect using express settings (password hash synchronization)](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-express)  
    Azure AD Connect Express Settings is used when you have a single-forest topology and password hash synchronization for authentication. Express Settings is the default option and is used for the most commonly deployed scenario.
- Pass-through authentication (PTA)
  - [What is Pass-through Authentication?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta)  
    A sign-in method that allows users to use the same password on-premises and in the cloud, but doesn't require the additional infrastructure of a federated environment.  
    ![Pass-through authentication](/images/pta1.png)
  - [How does Pass-through Authentication work?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-how-it-works)  
    This article is an overview of how Azure Active directory (Azure AD) Pass-through Authentication works.
  - [Current limitations](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-current-limitations)  
    This article details the supported and un-supported scenarios
  - [Security deep dive](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-security-deep-dive)  
    This article provides a more detailed description of how Azure Active Directory (Azure AD) Pass-through Authentication works. It focuses on the security aspects of the feature.
    - Detailed technical information about how to install and register the Authentication Agents.
    - Detailed technical information about the encryption of passwords during user sign-in.
    - The security of the channels between on-premises Authentication Agents and Azure AD.
    - Detailed technical information about how to keep the Authentication Agents operationally secure.
    - Other security-related topics.
  - [Deploy Azure AD Pass-through Authentication](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-pta-quick-start)  
    This is a quickstart tutorial
- Implement and manage federation
  - [What is federation?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-fed)  
    You can federate your on-premises environment with Azure AD and use this federation for authentication and authorization. This sign-in method ensures that all user authentication occurs on-premises. This method allows administrators to implement more rigorous levels of access control. Federation with AD FS and PingFederate is available.  
    ![Federated identity](/images/federated-identity.png)
  - [How federation works](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-fed-whatis)  
    With federation sign-in, you can enable users to sign in to Azure AD-based services with their on-premises passwords and, while on the corporate network, without having to enter their passwords again.
  - [Configuring federation with AD FS](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-install-custom#configuring-federation-with-ad-fs)
  - [Manage and customize ADFS by using Azure AD Connect](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-fed-management)  
    This article describes how to manage and customize Active Directory Federation Services (AD FS) by using Azure Active Directory (Azure AD) Connect. It also includes other common AD FS tasks that you might need to do for a complete configuration of an AD FS farm.
- Trouble-shoot synchronization errors
  - [Troubleshoot password hash synchronization](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-password-hash-synchronization)  
    This topic provides steps for how to troubleshoot issues with password hash synchronization. If passwords are not synchronizing as expected, it can be either for a subset of users or for all users.
  - [Troubleshoot Pass-through Authentication](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-pass-through-authentication)  
    This article helps you find troubleshooting information about common issues regarding Azure AD Pass-through Authentication
  - [Troubleshooting Errors during synchronization](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-sync-errors)  
    Errors could occur when identity data is synchronized from Windows Server Active Directory (AD DS) to Azure Active Directory (Azure AD). This article provides an overview of different types of sync errors, some of the possible scenarios that cause those errors and potential ways to fix the errors. This article includes the common error types and may not cover all the possible errors.
  - [Troubleshoot an object that is not synchronizing](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-object-not-syncing)  
    If an object is not syncing as expected with Microsoft Azure Active Directory (Azure AD), it can be because of several reasons. If you are troubleshooting a problem where the object is not in Azure AD, this article is for you. It describes how to find errors in the on-premises component Azure AD Connect synchronization.
  - [Troubleshoot an attribute not synchronizing in Azure AD Connect](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-attribute-not-syncing)
- Azure AD Connect Health
  - [What is Azure AD Connect Health?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-azure-ad-connect#what-is-azure-ad-connect-health)  
    Azure Active Directory (Azure AD) Connect Health provides robust monitoring of your on-premises identity infrastructure. It enables you to maintain a reliable connection to Microsoft 365 and Microsoft Online Services. This reliability is achieved by providing monitoring capabilities for your key identity components. Also, it makes the key data points about these components easily accessible.  
    ![Azure Active Directory Connect Health](/images/aadconnecthealth2.png)
  - [Why use Azure AD Connect Health?](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-azure-ad-connect#why-use-azure-ad-connect-health)  
    Azure AD Connect Health helps monitor and gain insights into your on-premises identity infrastructure thus ensuring the reliability of this environment. It is as simple as installing an agent on each of your on-premises identity servers.
  - [Azure AD Connect Health agent installation](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-health-agent-install)  
    In this article, you'll learn how to install and configure the Azure Active Directory (Azure AD) Connect Health agents.
  - [Azure AD Connect Health operations](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-health-operations)  
    This topic describes the various operations you can perform by using Azure Active Directory (Azure AD) Connect Healt (Enable email notifications, Delete a server or service instance, Manage access with Azure RBAC)
  - [Monitor Azure AD Connect sync with Azure AD Connect Health](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-health-sync)
    - Alerts for Azure AD Connect Health for sync
    - Limited Evaluation of Alerts
    - Sync Insight (latency, object changes)
    - Object Level Synchronization Error Report  
  - [Diagnose and remediate duplicated attribute sync errors](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-health-diagnose-sync-errors)  
    Taking one step farther to highlight sync errors, Azure Active Directory (Azure AD) Connect Health introduces self-service remediation. It troubleshoots duplicated attribute sync errors and fixes objects that are orphaned from Azure AD.

## [Part 2: Implement an Authentication and Access Management solution](https://docs.microsoft.com/en-us/learn/paths/implement-authentication-access-management-solution/)

### [Secure Azure Active Directory users with Multi-Factor Authentication](https://docs.microsoft.com/en-us/learn/modules/secure-aad-users-with-mfa/)

- What is Azure AD Multi-Factor Authentication?
  - [How MFA works](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-howitworks)  
    Multi-factor authentication is a process where a user is prompted during the sign-in process for an additional form of identification, such as to enter a code on their cellphone or to provide a fingerprint scan.  
    ![Conditional access overview](/images/conditional-access-overview.png)
  - [How to get MFA](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-licensing)  
     Basic multi-factor authentication features are available to Microsoft 365 and Azure Active Directory (Azure AD) global administrators for no extra cost. If you want to upgrade the features for your admins or extend multi-factor authentication to the rest of your users, you can purchase Azure AD Multi-Factor Authentication in several ways.
  - [Enable per-user MFA](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-mfa-userstates)  
    To secure user sign-in events in Azure AD, you can require multi-factor authentication (MFA). Enabling Azure AD Multi-Factor Authentication using Conditional Access policies is the recommended approach to protect users. Conditional Access is an Azure AD Premium P1 or P2 feature that lets you apply rules to require MFA as needed in certain scenarios.
    If needed, you can instead enable each account for per-user Azure AD Multi-Factor Authentication. When users are enabled individually, they perform multi-factor authentication each time they sign in (with some exceptions, such as when they sign in from trusted IP addresses or when the remember MFA on trusted devices feature is turned on).  
    Changing user states isn't recommended unless your Azure AD licenses don't include Conditional Access and you don't want to use security defaults
  - [Configure MFA settings](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-mfa-mfasettings)  
    To customize the end-user experience for Azure AD Multi-Factor Authentication, you can configure options for settings like the account lockout thresholds or fraud alerts and notifications. Some settings are directly in the Azure portal for Azure Active Directory (Azure AD), and some in a separate Azure AD Multi-Factor Authentication portal.
- Plan your multi-factor authentication deployment
  - [Deployment guide](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-mfa-getstarted)  
    This deployment guide shows you how to plan and implement an Azure AD MFA roll-out.
  - [What authentication and verification methods are available in Azure Active Directory?](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-authentication-methods)  
    Microsoft recommends passwordless authentication methods such as Windows Hello, FIDO2 security keys, and the Microsoft Authenticator app because they provide the most secure sign-in experience. Although a user can sign-in using other common methods such as a username and password, passwords should be replaced with more secure authentication methods.  
    ![Authentication methods](/images/authentication-methods.png)
  - [Plan a Conditional Access deployment](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/plan-conditional-access)  
    Microsoft provides standard conditional policies called security defaults that ensure a basic level of security. However, your organization may need more flexibility than security defaults offer. You can use Conditional Access to customize security defaults with more granularity and to configure new policies that meet your requirements.
  - [Supported device compliance partners](https://docs.microsoft.com/en-us/mem/intune/protect/device-compliance-partners#supported-device-compliance-partners)  
    The compliance state is evaluated by conditional access policies, the same as compliance state data for devices managed by Intune. By default, Intune is a registered compliance partner for iOS and Android. When you add additional partners, you can set the priority order to ensure the correct partner manages device to fit your business needs.
  - [Optimize reauthentication prompts and understand session lifetime for MFA](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concepts-azure-multi-factor-authentication-prompts-session-lifetime)  
    Azure Active Directory (Azure AD) has multiple settings that determine how often users need to reauthenticate. This reauthentication could be with a first factor such as password, FIDO, or passwordless Microsoft Authenticator, or to perform multi-factor authentication (MFA). You can configure these reauthentication settings as needed for your own environment and the user experience you want.
  - [Combined registration for SSPR and Azure AD MFA](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-registration-mfa-sspr-combined)  
    Before combined registration, users registered authentication methods for Azure AD Multi-Factor Authentication and self-service password reset (SSPR) separately. People were confused that similar methods were used for Azure AD Multi-Factor Authentication and SSPR but they had to register for both features. Now, with combined registration, users can register once and get the benefits of both Azure AD Multi-Factor Authentication and SSPR.
  - [Configure the Azure AD Multi-Factor Authentication registration policy](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-configure-mfa-policy)
  - [Communication templates](https://aka.ms/mfatemplates)  
    Use this customizable posters and email templates to roll out multi-factor authentication to your organization
  - [End-user documentation](https://support.microsoft.com/en-us/account-billing/set-up-your-security-info-from-a-sign-in-prompt-28180870-c256-4ebf-8bd7-5335571bf9a8)  
    You can follow these steps if you're prompted to set up your security info immediately after you sign-in to your work or school account.
- Configure multi-factor authentication methods
  - [What authentication and verification methods are available in Azure Active Directory?](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-authentication-methods)  
    This article outlines the security considerations for the available authentication methods.

### [Manage user authentication](https://docs.microsoft.com/en-us/learn/modules/manage-user-authentication/)

- Administer FIDO2 and passwordless authentication methods
  - [What are FIDO2 security keys?](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-authentication-passwordless#fido2-security-keys)  
    FIDO2 security keys are an unphishable standards-based passwordless authentication method that can come in any form factor.  
    ![FIDO2 Security key flow](/images/fido2-security-key-flow.png)
  - [Enable passwordless security key sign-in](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-authentication-passwordless-security-key)  
    This document focuses on enabling security key based passwordless authentication.
- Implement an authentication solution based on Windows Hello for Business
  - [How Windows Hello for Business works in Windows Devices](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-how-it-works)  
    Windows Hello for Business is a modern, two-factor credential that is the more secure alternative to passwords.
  - [Why a PIN is better than a password](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-why-pin-is-better-than-password)
  - [Windows Hello for Business Deployment Overview](https://docs.microsoft.com/en-us/windows/security/identity-protection/hello-for-business/hello-deployment-guide)  
    This deployment overview is to guide you through deploying Windows Hello for Business.
- Exercise configure and deploy self-service password reset
  - [How it works: Azure AD self-service password reset](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-sspr-howitworks)  
    Azure Active Directory (Azure AD) self-service password reset (SSPR) gives users the ability to change or reset their password, with no administrator or help desk involvement. If a user's account is locked or they forget their password, they can follow prompts to unblock themselves and get back to work. This ability reduces help desk calls and loss of productivity when a user can't sign in to their device or an application.
  - [Enable users to unlock their account or reset passwords using Azure AD self-service password reset](https://docs.microsoft.com/en-us/azure/active-directory/authentication/tutorial-enable-sspr)
  - [How does self-service password reset writeback work in Azure Active Directory?](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-sspr-writeback)  
    Password writeback is a feature enabled with Azure AD Connect that allows password changes in the cloud to be written back to an existing on-premises directory in real time. In this configuration, as users change or reset their passwords using SSPR in the cloud, the updated passwords also written back to the on-premises AD DS environment
  - [Plan an Azure Active Directory self-service password reset deployment](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-sspr-deployment)  
    This deployment guide shows you how to plan and then test an SSPR roll-out.
- Deploy and manage password protection
  - [Eliminate weak passwords in the cloud](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-password-ban-bad)  
    A lot of security guidance recommends that you don't use the same password in multiple places, to make it complex, and to avoid simple passwords like Password123. You can provide your users with guidance on how to choose passwords, but weak or insecure passwords are often still used. Azure AD Password Protection detects and blocks known weak passwords and their variants, and can also block additional weak terms that are specific to your organization. With Azure AD Password Protection, default global banned password lists are automatically applied to all users in an Azure AD tenant. To support your own business and security needs, you can define entries in a custom banned password list. When users change or reset their passwords, these banned password lists are checked to enforce the use of strong passwords.
  - [Eliminate weak passwords on-premises](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-password-ban-bad-on-premises)  
    Azure AD Password Protection detects and blocks known weak passwords and their variants, and can also block additional weak terms that are specific to your organization. On-premises deployment of Azure AD Password Protection uses the same global and custom banned password lists that are stored in Azure AD, and does the same checks for on-premises password changes as Azure AD does for cloud-based changes. These checks are performed during password changes and password reset events against on-premises Active Directory Domain Services (AD DS) domain controllers.
  - [Plan and deploy on-premises Azure Active Directory Password Protection](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-password-ban-bad-on-premises-deploy)  
    This article shows how the basic components of Azure AD Password Protection work together in an on-premises Active Directory environment
    ![Azure AD Password protection](/images/azure-ad-password-protection.png)
  - [Enable on-premises Azure Active Directory Password Protection](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-password-ban-bad-on-premises-operations)  
    This article shows you how to enable Azure AD Password Protection for your on-premises environment.
- Implement and manage tenant restrictions
  - [Use tenant restrictions to manage access to SaaS cloud applications](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/tenant-restrictions)  
    With tenant restrictions, organizations can control access to SaaS cloud applications, based on the Azure AD tenant the applications use for single sign-on. For example, you may want to allow access to your organization's Microsoft 365 applications, while preventing access to other organizations' instances of these same applications.

### [Plan, implement, and administer Conditional Access](https://docs.microsoft.com/en-us/learn/modules/plan-implement-administer-conditional-access/)

- Plan security defaults
  - [What are security defaults?](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)  
    Managing security can be difficult with common identity-related attacks like password spray, replay, and phishing becoming more popular. Security defaults make it easier to help protect your organization from these attacks with preconfigured security settings
  - [Introducing security defaults](https://techcommunity.microsoft.com/t5/azure-active-directory-identity/introducing-security-defaults/ba-p/1061414)
- Plan Conditional Access policies
  - [What is Conditional Access?](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/overview)  
    Conditional Access is the tool used by Azure Active Directory to bring signals together, to make decisions, and enforce organizational policies. Conditional Access is at the heart of the new identity driven control plane.  
    ![Conditional access signal decision enforcement](/images/conditional-access-signal-decision-enforcement.png)
  - [Plan a Conditional Access deployment](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/plan-conditional-access)
  - [Manage external access with Conditional Access policies](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/7-secure-access-conditional-access)  
    This article discusses applying Conditional Access policies to external users and assumes you don't have access to Entitlement Management functionality. Conditional Access policies can be and are used alongside Entitlement Management.
  - [Emergency access or break-glass accounts](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-policy-block-access#user-exclusions)  
    Emergency access or break-glass accounts to prevent tenant-wide account lockout. In the unlikely scenario all administrators are locked out of your tenant, your emergency-access administrative account can be used to log into the tenant take steps to recover access.
  - [Require terms of use](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/terms-of-use)  
    Azure AD terms of use policies provide a simple method that organizations can use to present information to end users. This presentation ensures users see relevant disclaimers for legal or compliance requirements. This article describes how to get started with terms of use (ToU) policies.
- Implement Conditional Access policy controls and assignments
  - [Common Conditional Access policies](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-policy-common)
  - [Sign-in risk-based Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-policy-risk)  
    Most users have a normal behavior that can be tracked, when they fall outside of this norm it could be risky to allow them to just sign in. You may want to block that user or maybe just ask them to perform multi-factor authentication to prove that they are really who they say they are. A sign-in risk represents the probability that a given authentication request isn't authorized by the identity owner. Organizations with Azure AD Premium P2 licenses can create Conditional Access policies incorporating Azure AD Identity Protection sign-in risk detections.
  - [User risk-based Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-policy-risk-user)  
    Microsoft works with researchers, law enforcement, various security teams at Microsoft, and other trusted sources to find leaked username and password pairs. Organizations with Azure AD Premium P2 licenses can create Conditional Access policies incorporating Azure AD Identity Protection user risk detections.
  - [Building a Conditional Access policy](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-policies)
  - [User and group assignment](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-users-groups)  
    A Conditional Access policy must include a user assignment as one of the signals in the decision process. Users can be included or excluded from Conditional Access policies. Azure Active Directory evaluates all policies and ensures that all requirements are met before granting access to the user
- Test and troubleshoot Conditional Access policies
  - [Troubleshoot using the What If tool in Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/what-if-tool)  
    How do you know what to expect from the Conditional Access policies in your environment? To answer this question, you can use the Conditional Access What If tool.
  - [Troubleshooting sign-in problems with Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/troubleshoot-conditional-access)  
    The information in this article can be used to troubleshoot unexpected sign-in outcomes related to Conditional Access using error messages and Azure AD sign-ins log.
  - [Troubleshooting Conditional Access policy changes](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/troubleshoot-policy-changes-audit-log)  
    The Azure Active Directory (Azure AD) audit log is a valuable source of information when troubleshooting why and how Conditional Access policy changes happened in your environment. Audit log data is only kept for 30 days by default, which may not be long enough for every organization. Organizations can store data for longer periods by changing diagnostic settings in Azure AD
  - [Monitor and troubleshoot continuous access evaluation](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-continuous-access-evaluation-troubleshoot)  
    Administrators can monitor and troubleshoot sign in events where continuous access evaluation (CAE) is applied in multiple ways.
- Implement application controls
  - [Conditional Access: Cloud apps, actions, and authentication context](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-cloud-apps)  
    Cloud apps, actions, and authentication context are key signals in a Conditional Access policy. Conditional Access policies allow administrators to assign controls to specific applications, actions, or authentication context.
  - [Protect apps with Microsoft Cloud App Security Conditional Access App Control](https://docs.microsoft.com/en-us/cloud-app-security/proxy-intro-aad)  
    Conditional Access App Control enables user app access and sessions to be monitored and controlled in real time based on access and session policies.
  - [Require app protection policy and an approved client app for cloud app access with Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/app-protection-based-conditional-access)  
    This article presents three scenarios to configure Conditional Access policies for resources like Microsoft 365, Exchange Online, and SharePoint.
- Implement session management
  - [Configure authentication session management with Conditional Access](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime#persistence-of-browsing-sessions)  
    A persistent browser session allows users to remain signed in after closing and reopening their browser window.
  - [Conditional Access: Session](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/concept-conditional-access-session)  
    Within a Conditional Access policy, an administrator can make use of session controls to enable limited experiences within specific cloud applications.
  - [Deploy Conditional Access App Control for featured apps](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)  
    Featured apps are already onboarded with both access and session controls (for example Salesforce, ServiceNow, ...)
  - [Onboard and deploy Conditional Access App Control for any app](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-any-app)  
    This article describes how to onboard and deploy custom line-of-business apps, non-featured SaaS apps, and on-premise apps hosted via the Azure Active Directory (Azure AD) Application Proxy with session controls.
- Configure smart lockout thresholds
  - [Protect user accounts from attacks with Azure Active Directory smart lockout](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-password-smart-lockout)  
    Smart lockout helps lock out bad actors that try to guess your users' passwords or use brute-force methods to get in. Smart lockout can recognize sign-ins that come from valid users and treat them differently than ones of attackers and other unknown sources. Attackers get locked out, while your users continue to access their accounts and be productive.

### [Manage Azure AD Identity Protection](https://docs.microsoft.com/en-us/learn/modules/manage-azure-active-directory-identity-protection/)

- Review identity protection basics
  - [What is Identity Protection?](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/overview-identity-protection)  
    Identity Protection is a tool that allows organizations to accomplish three key tasks: 1) Automate the detection and remediation of identity-based risks. 2) Investigate risks using data in the porta and 3) export risk detection data to your SIEM.
  - [Security overview](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/concept-identity-protection-security-overview)  
    The Security overview in the Azure portal gives you an insight into your organization’s security posture. It helps identify potential attacks and understand the effectiveness of your policies.
  - [What are risks?](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/concept-identity-protection-risks)  
    Risk detections in Azure AD Identity Protection include any identified suspicious actions related to user accounts in the directory. Risk detections (both user and sign-in linked) contribute to the overall user risk score that is found in the Risky Users report. Risk can be detected at the User and Sign-in level and two types of detection or calculation Real-time and Offline.
- Implement and manage user risk policy
  - [Identity Protection policies](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/concept-identity-protection-policies)  
    Azure Active Directory Identity Protection includes three default policies that administrators can choose to enable:  
    - Azure AD MFA registration policy
    - Sign-in risk policy
    - User risk policy
  - [Configure and enable risk policies](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-configure-risk-policies)  
    This article gives recommendations on choosing acceptable risk
- Configure Azure Active Directory multi-factor authentication registration policy
  - [Configure the Azure AD Multi-Factor Authentication registration policy](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-configure-mfa-policy)  
    Azure AD Identity Protection helps you manage the roll-out of Azure AD Multi-Factor Authentication (MFA) registration by configuring a Conditional Access policy to require MFA registration no matter what modern authentication app you are signing in to.
- Monitor, investigate, and remediate elevated risky users
  - [Configure notifications](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-configure-notifications)  
    Azure AD Identity Protection sends two types of automated notification emails to help you manage user risk and risk detections: users at risk detected email and a weekly digest email
  - [How To: Investigate risk](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-investigate-risk)  
    Identity Protection provides organizations with three reports they can use to investigate identity risks in their environment. These reports are the risky users, risky sign-ins, and risk detections. Investigation of events is key to better understanding and identifying any weak points in your security strategy.
  - [Remediate risks and unblock users](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/howto-identity-protection-remediate-unblock)  
    After completing your investigation, you will want to take action to remediate the risk or unblock users. Organizations also have the option to enable automated remediation using their risk policies. Organizations should try to close all risk detections that they are presented with in a time period your organization is comfortable with. Microsoft recommends closing events as soon as possible because time matters when working with risk.

## [Part 3: Implement Access Management for Apps](https://docs.microsoft.com/en-us/learn/paths/implement-access-management-for-apps/)

### [Plan and design the integration of enterprise apps for SSO](https://docs.microsoft.com/en-us/learn/modules/plan-design-integration-of-enterprise-apps-for-sso/)

- Discover apps by using Microsoft Cloud App Security (MCAS) and Active Directory Federation Services app report
  - [Set up Cloud Discovery](https://docs.microsoft.com/en-us/cloud-app-security/set-up-cloud-discovery)  
    Cloud Discovery analyzes your traffic logs against Microsoft Cloud App Security's cloud app catalog of over 22,000 cloud apps. The apps are ranked and scored based on more than 90 risk factors to provide you with ongoing visibility into cloud use, Shadow IT, and the risk Shadow IT poses into your organization.
  - [Working with discovered apps](https://docs.microsoft.com/en-us/cloud-app-security/discovered-apps)  
    The Cloud Discovery dashboard is designed to give you more insight into how cloud apps are being used in your organization. It provides an at-a-glance overview of what kinds of apps are being used, your open alerts, and the risk levels of apps in your organization.
  - [Use the AD FS application activity report to migrate applications to Azure AD](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/migrate-adfs-application-activity)  
    The AD FS application activity report in the Azure portal lets you quickly identify which of your applications are capable of being migrated to Azure AD. It assesses all AD FS applications for compatibility with Azure AD, checks for any issues, and gives guidance on preparing individual applications for migration.
- Implement access management for apps
  - [Assign users and groups to an application in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/add-application-portal-assign-users)  
    This article shows you how to assign users and groups to an enterprise application in Azure Active Directory (Azure AD)
- Design and implement app management roles
  - [Delegate app registration permissions in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/roles/delegate-app-roles)  
    This article describes how to use permissions granted by custom roles in Azure Active Directory (Azure AD) to address your application management needs
- Create a custom role to manage app registration
  - [Create and assign a custom role (preview)](https://docs.microsoft.com/en-us/azure/active-directory/roles/delegate-app-roles#create-and-assign-a-custom-role-preview)  
     A custom role can be assigned at organization-wide scope, or it can be assigned at the scope if a single Azure AD object. An example of an object scope is a single app registration.
- Configure pre-integrated gallery SaaS apps
  - [Configure enterprise application properties in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/add-application-portal-configure)  
    You can configure the following common attributes of an enterprise application:
    - Enabled for users to sign in? - Determines whether users assigned to the application can sign in.
    - User assignment required? - Determines whether users who aren't assigned to the application can sign in.
    - Visible to users? - Determines whether users assigned to an application can see it in My Apps and Microsoft 365 app launcher.
    - Logo - Determines the logo that represents the application.
    - Notes - Provides a place to add notes that apply to the application.

### [Implement and monitor the integration of enterprise apps for SSO](https://docs.microsoft.com/en-us/learn/modules/implement-monitor-integration-of-enterprise-apps-for-sso/)

- Implement token customizations
  - [Configurable token lifetimes in the Microsoft identity platform](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-configurable-token-lifetimes)  
    You can specify the lifetime of a access, ID, or SAML token issued by the Microsoft identity platform. You can set token lifetimes for all apps in your organization, for a multi-tenant (multi-organization) application, or for a specific service principal in your organization.
  - [Provide optional claims to your app](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-optional-claims)
- Implement and configure consent settings
  - [Configure how end-users consent to applications](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/configure-user-consent?tabs=azure-portal)  
    Before an application can access your organization's data, a user must grant the application permissions to do so. Different permissions allow different levels of access. By default, all users are allowed to consent to applications for permissions that don't require administrator consent.
  - [Risk-based step-up consent](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/configure-user-consent?tabs=azure-portal#risk-based-step-up-consent)  
    Risk-based step-up consent helps reduce user exposure to malicious apps that make illicit consent requests. For example, consent requests for newly registered multi-tenant apps that are not publisher verified and require non-basic permissions are considered risky. If Microsoft detects a risky end-user consent request, the request will require a "step-up" to admin consent instead. This capability is enabled by default, but it will only result in a behavior change when end-user consent is enabled.
  - [Configure the admin consent workflow](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/configure-admin-consent-workflow)  
    This article describes how to enable the admin consent workflow feature, which gives end users a way to request access to applications that require admin consent.
  - [Grant tenant-wide admin consent to an application](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/grant-admin-consent)
- Integrate on-premises apps by using Azure Active Directory application proxy
  - [What is Application Proxy?](https://docs.microsoft.com/en-us/azure/active-directory/app-proxy/what-is-application-proxy)  
    Azure AD Application Proxy  can be implemented by IT professionals who want to publish on-premises web applications externally. Remote users who need access to internal apps can then access them in a secure manner.  
    ![Azure Active Directory Application Proxy architecture](/images/azure-ad-application-proxy-architecture.png)
  - [Remote access to on-premises applications through Azure AD Application Proxy](https://docs.microsoft.com/en-us/azure/active-directory/app-proxy/application-proxy)  
    After a single sign-on to Azure AD, users can access both cloud and on-premises applications through an external URL or an internal application portal. For example, Application Proxy can provide remote access and single sign-on to Remote Desktop, SharePoint, Teams, Tableau, Qlik, and line of business (LOB) applications.
- Integrate custom SaaS apps for single sign-on
  - [What is the Microsoft identity platform?](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-overview)
  - [ClaimsXRay in AzureAD with Directory Extension](https://techcommunity.microsoft.com/t5/core-infrastructure-and-security/claimsxray-in-azuread-with-directory-extension/ba-p/1505737)
- Implement application user provisioning
  - [How Application Provisioning works in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/app-provisioning/how-provisioning-works)  
    Automatic provisioning refers to creating user identities and roles in the cloud applications that users need access to. In addition to creating user identities, automatic provisioning includes the maintenance and removal of user identities as status or roles change. Before you start a deployment, you can review this article to learn how Azure AD provision works and get configuration recommendations.
  - [SCIM synchronization with Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/sync-scim)
- Monitor and audit access to Azure Active Directory integrated applications
  - [Usage and insights report in the Azure Active Directory portal](https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/concept-usage-insights-report)  
    With the usage and insights report, you can get an application-centric view of your sign-in data.
  - [Audit logs in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/concept-audit-logs)  
    With the audit logs in Azure AD, you get access to records of system activities for compliance. The most common views of this log are based on the following categories: user/group/application management

### [Implement app registration](https://docs.microsoft.com/en-us/learn/modules/implement-app-registration/)

- Plan your line of business application registration strategy
  - [How and why applications are added to Azure AD](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-how-applications-are-added)  
    - What are application objects and where do they come from
    - What are service principals and where do they come from?
    - How are application objects and service principals related to each other?
    - Why do applications integrate with Azure AD?
    - Who has permission to add applications to my Azure AD instance?
  - [Tenancy in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/develop/single-and-multi-tenant-apps)  
    Single-tenant versus Multi-tenant apps
- Implement application registration
  - [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)  
    In this quickstart, you register an app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for your application and its users.
  - [Application and service principal objects in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/develop/app-objects-and-service-principals)  
    This article describes application registration, application objects, and service principals in Azure Active Directory (Azure AD): what they are, how they're used, and how they are related to each other. A multi-tenant example scenario is also presented to illustrate the relationship between an application's application object and corresponding service principal objects.
  - [App sign-in flow with the Microsoft identity platform](https://docs.microsoft.com/en-us/azure/active-directory/develop/app-sign-in-flow)  
    This topic discusses the basic sign-in flow for web, desktop, and mobile apps using Microsoft identity platform.
- Configure application permission
  - [Permissions and consent in the Microsoft identity platform](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-permissions-and-consent)  
    This article covers the basic concepts of this authorization model, including scopes, permissions, and consent.
  - [Understanding Azure AD application consent experiences](https://docs.microsoft.com/en-us/azure/active-directory/develop/application-consent-experience)  
    Learn more about the Azure Active Directory (Azure AD) application consent user experience. So you can intelligently manage applications for your organization and/or develop applications with a more seamless consent experience.
  - [Configure a client application to access a web API](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis)
- Grant tenant-wide admin consent to an application
  - [Admin consent on the Microsoft identity platform](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-admin-consent)  
    Some permissions require consent from an administrator before they can be granted within a tenant. You can also use the admin consent endpoint to grant permissions to an entire tenant.
- Implement application authorization
  - [Application roles](https://docs.microsoft.com/en-us/azure/architecture/multitenant-identity/app-roles)  
    - Roles using Azure AD App Roles
    - Roles using Azure AD security groups
    - Roles using an application role manager
- Add app roles to application and receive tokens
  - [Add app roles to your application and receive them in the token](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-add-app-roles-in-azure-ad-apps)  
    Using RBAC with Application Roles and Role Claims, developers can securely enforce authorization in their apps with less effort.

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
