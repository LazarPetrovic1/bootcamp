# User Management

You define user roles, security profiles, and user accounts to control who has access to IBM QRadar, which tasks they can perform, and which data they have access to.

### User roles

During installation, 2 roles are defined:
+ **Admin**
+ **All**

> Related CRUD tasks:
+ Creating a user role (pg. 13)
+ Editing a user role (pg. 16)
+ Deleting a user role (pg. 19)

### Security profiles

Security profiles define which networks, log sources, and domains that a user can access.

##### Domains

You must define domains on the **Domain Management** window before the **Domains** tab is shown on the **Security Profile Management** window. Domain-level restrictions are not applied until the security profiles are updated, and the changes are deployed.

Domain assignments take precedence over all settings on the **Permission Precedence, Networks**, and **Log Sources** tabs.

### Permission precedence

+ **No Restrictions** - This option does not place restrictions on which events are displayed in the Log Activity tab, and which flows are displayed in the Network Activity tab.
+ **Network Only** - This option restricts the user to view only events and flows that are associated with the networks that are specified in this security profile.
+ **Log Sources Only** - This option restricts the user to view only events that are associated with the log sources that are specified in this security profile.
+ **Networks AND Log Sources** - This option allows the user to view only events and flows that are associated with the log sources and networks that are specified in this security profile. For example, if the security profile allows access to events from a log source but the destination network is restricted, the event is not displayed in the Log Activity tab. The event must match both requirements.
+ **Networks OR Log Sources** - This option allows the user to view events and flows that are associated with either the log sources or networks that are specified in this security profile.

##### Permission precedence for offense data

Security profiles automatically use the **Networks OR Log Sources** permission when offense data is shown.

> Related CRUD tasks:
+ Creating a security profile (pg. 20)
+ Editing a security profile (pg. 21)
+ Duplicating a security profile (pg. 22)
+ Deleting a security profile (pg. 22)

### User accounts

The user account defines the unique user name that is used to log in to IBM QRadar, and specifies which user role, security profile, and tenant assignments the user is assigned to.

> Related tasks:
+ Viewing and editing information about the current user (pg. 23)
+ Viewing user login history (pg. 24)
+ Creating a user account (pg. 24)
+ Editing a user account (pg. 25)
+ Disabling a user account (pg. 26)
+ Deleting a user account (pg. 26)
+ Deleting saved searches of a deleted user (pg. 27)

### User authentication


IBM QRadar supports the following authentication types:

+ System authentication - Users are authenticated locally. System authentication is the default authentication type.
+ RADIUS authentication - Users are authenticated by a Remote Authentication Dial-in User Service (RADIUS) server. When a user attempts to log in, QRadar encrypts the password only, and forwards the user name and password to the RADIUS server for authentication.
+ TACACS authentication - Users are authenticated by a Terminal Access Controller Access Control System (TACACS) server. When a user attempts to log in, QRadar encrypts the user name and password, and forwards this information to the TACACS server for authentication. TACACS Authentication uses Cisco Secure ACS Express as a TACACS server. QRadar supports up to Cisco Secure ACS Express 4.3.
+ Microsoft Active Directory - Users are authenticated by a Lightweight Directory Access Protocol (LDAP) server that uses Kerberos.
+ LDAP - Users are authenticated by a Native LDAP server.
+ SAML single sign-on authentication - Users can easily integrate QRadar with your corporate identity server to provide single sign-on, and eliminate the need to maintain QRadar local users. Users who are authenticated to your identity server can automatically authenticate to QRadar. They don't need to remember separate passwords or type in credentials every time they access QRadar.

##### Prerequisite checklist for external authentication providers

Before you can configure RADIUS, TACACS, Active Directory, or LDAP as the authentication type, you must complete the following tasks:
+ Configure the authentication server before you configure authentication in QRadar. For more information, see your server documentation.
+ Ensure that the server has the appropriate user accounts and privilege levels to communicate with QRadar. For more information, see your server documentation.
+ Ensure that the time of the authentication server is synchronized with the time of the QRadar server.
+ Ensure that all users have appropriate user accounts and roles to allow authentication with the vendor servers.

> Related tasks
+ Changing QRadar user passwords (pg. 28)
+ External authentication guidelines for administrative users (pg. 28)
+ Configuring system authentication (pg. 29)
+ Configuring RADIUS authentication (pg. 30)
+ Configuring TACACS authentication (pg. 31)
+ Configuring Active Directory authentication(pg. 32)

### LDAP authentication

You can configure IBM QRadar to use supported Lightweight Directory Access Protocol (LDAP) providers for user authentication and authorization.

QRadar reads the user and role information from the LDAP server, based on the authorization criteria that you defined.

> Related tasks
+ Configuring LDAP authentication (pg. 33)
+ Synchronizing data with an LDAP server (pg. 37)
+ Configuring SSL or TLS certificates (pg. 37)
+ Displaying hover text for LDAP information(pg. 38)
+ Multiple LDAP repositories (pg. 39)
+ Example: Least privileged access configuration and set up (pg. 40)

### SAML single sign-on authentication

Security Assertion Markup Language (SAML) is a framework for authentication and authorization between a service provider (SP) and an identity provider (IDP) where authentication is exchanged using digitally signed XML documents. The service provider agrees to trust the identity provider to authenticate users. In return, the identity provider generates an authentication assertion, which indicates that a user has been authenticated.

> Related tasks
+ Configuring SAML authentication (pg. 40)
+ Import a new certificate for signing and decrypting (pg. 42)
+ Setting up SAML with Microsoft Active Directory Federation Services (pg. 42)
+ Installing unrestricted SDK JCE policy files (pg. 43)
+ Troubleshooting SAML authentication (pg. 44)
