# Azure-AD-vs-On-Premises-AD

- Azure AD is different from AD DS.

# Key characterstics of Azure AD that make it different from an on premises AD

- <strong> <em> Identity solution. </strong> </em> Azure AD is primarily an identity solution, and it is designed for Internet-based applications by using HTTP and HTTPS communications.
- <strong> <em> REST API Querying. </strong> </em> Because Azure AD is HTTP/HTTPS based, it cannot be queried through LDAP. Instead, Azure AD uses the REST API over HTTP and HTTPS.
- <strong> <em> Communication Protocols. </strong> </em> Because Azure AD is HTTP/HTTPS based, it does not use Kerberos authentication. Instead, it uses HTTP and HTTPS protocols such as SAML, WS-Federation, and OpenID Connect for authentication (and OAuth for authorization).
- <strong> <em> Authentication Services. </strong> </em> Include SAML, WS-Federation, or OpenID.
- <strong> <em> Authorization Service. </strong> </em> Uses OAuth.
- <strong> <em> Federation Services. </strong> </em> Azure AD includes federation services, and many third-party services (such as Facebook).
- <strong> <em> Flat structure. </strong> </em> Azure AD users and groups are created in a flat structure, and there are no Organizational Units (OUs) or Group Policy Objects (GPOs).

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/168120404-e6beeb10-f5f7-44a6-b92e-9fcfc93c0a81.png" height="75%" width="75%" alt="Admin Units"/>
  
<p/>

# What is a Federation Service? 
- In a federated environment, a user from an external organization such as Facebook, can use its own credentials to log into resources in another organization.
- Each organization continues to manage its own identities(users, accounts, passwords), but they can securely accept identities from other organizations
- This is what allows Single-Sign On (SSO)
- Federation with Azure AD or 0365 enables users to authenticate using on-premises credentials and access all resources in the cloud.
- It becomes important to have a highly available AD FS infrastructure to ensure access to resources both on-premises and in the cloud.

# Why ADFS is used by organizations?
- Using Active Directory (AD) in the connected online world creates authentication challenges. AD cannot authenticate users who try to access integrated applications externally. In the modern workplace, users often need to access applications that are not owned or managed by their organization’s AD. ADFS is able to resolve and simplify these third-party authentication challenges.

- ADFS allows users from one organization to access applications of partner organizations using the standard credentials of their organization’s Active Directory (AD). ADFS also lets users access AD-integrated applications while working remotely using their standard organizational AD credentials via a web interface. When establishing a partnership to use another organization’s web applications, ADFS provides a central place to manage and audit the employee identity information that is shared with their organization’s partners.

- Over 90% of organizations use Active Directory, which means many use ADFS as well.

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/168121383-f86094b5-582b-4ec0-be6a-38208bfb7dfe.png" height="75%" width="75%" alt="Admin Units"/>
  
<p/>

# What are the components of ADFS?
- Active Directory: The Identity Information which is to be used by ADFS is stored on the Active Directory.
- Federation Server: It contains the tools needed to manage federated trusts between business partners. It processes authentication requests coming in from external users and hosts a security token service that issues tokens for claims based on verification of credentials from AD.
- Federation Server Proxy: The Proxy is deployed on the extranet of the organization, to which external clients connect when requesting a security token. It forwards these requests to the Federation Server. The Federation server is not exposed directly to the internet to prevent security risks.
- ADFS Web Server: It hosts the ADFS Web Agent which manages the security tokens and authentication cookies sent to it for authentication purposes.
 

