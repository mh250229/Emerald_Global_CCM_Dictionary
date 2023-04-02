## OpenID Connect (OIDC) Protocol - Emerald Global CCM 

The Emerald Global CCM supports Active Directory, Single Sign, and Azure Active Directory (Open ID connect protocol).

Users can log in to the CCM Office and be authenticated via OIDC (External) authentication, or via the Active Directory or Emerald internal credentials. This is determined by the Security Policy/Office Authentication configuration.

In the CCM Office/Security Policy/Office Authentication section, there are three Authentication options:

* OIDC (External)
* Active Directory
* Emerald

![Office Authentication Screen](/Images/officeauthenticationscreen.png)

**Example of Internal authentication:**

Prerequisite: In the CCM -> Security Policy -> Office authentication, the Authentication Method is set to Emerald (Internal).

1. Open the CCM and enter a valid INTERNAL username.
1. Enter the Password and click the LOG IN button  
The Authentication is done by the INTERNAL provider  
The Log in is successful

**Example of External authentication:**

Prerequisite: In the CCM -> Security Policy -> Office authentication, the Authentication Method is set to OIDC (External).

1. Open the CCM and enter a valid external username (such as test@Name.com).  
The Client recognizes that the username is a valid email (EXTERNAL IDP) and checks if the email domain prefix match, and is valid in the RETAILER_DOMAIN (domain prefix that was received from the OIDC (OpenID connect) configuration)  
**Note:**  
When it is External authentication, the Password field is hidden.  
![Login Password Field Hidden](/Images/loginpasswordfieldhidden.png)

1. Click the LOG IN button  
The Client starts the OIDC flow with the EXTERNAL IDP and the Authentication is done by the External provider  
The Client sends and sets the user’s email:
![Pick an account](/Images/pickanaccount.png)

1. Select the account. The Authentication process is continued after selecting the account.  
The EXTERNAL provider requires that the user enters their password (or any other authentication)
![Enter password](/Images/enterpassword.png)

1. Enter the user’s password and click Sign in.  
When the authentication flow is completed with the EXTERNAL IDP, the IDP will redirect the user back to the CCM.  
The Log in is successful.  
The CCM sends the TOKEN to the Emerald Global server once the authentication/authorization flow is completed with the EXTERNAL IDP.

1. Logout of the CCM. On logging out, the ‘Select Account’ screen is redisplayed.

1. Select the account from which you wish to sign out. The Login screen is redisplayed.

**Details**

**OIDC: OpenID Connect** is an identity layer built on top of the OAuth 2.0 framework. It allows third-party applications to verify the identity of the end-user and to obtain basic user profile information.

It defines the sign-in flow that enables the client application to authenticate the user, and to obtain information (or "claims") about that user, such as the user name, email, and so on. User identity information is encoded in a secure JSON Web Token (JWT), called ID token.

**Idmlogin API**

The idmlogin API supports the ‘USER_UNIQUE_IDENTIFIER’ and then returns the user session after the validation in the Emerald Global database.

**OpenID Connect (OIDC) Protocol:** Emerald Global exposes the GET openidConfiguration service. It retrieves the OIDC IDP (Identify Provider) configuration that was added to the ConfigurationEntry table.

The following parameters and values are returned to the client when it requests the OpenId configuration (GET Request to api/openid-configuration):
* CLIENT_ID 
* CLIENT_ROOT
* CLIENT_SCOPE
* RESPONSE_TYPE  
* AUTHORITY
* REDIRECT_URI
* API_ROOT
* IDP OPENID CONFIGURATION – Azure example:
“https://login.microsoftonline.com/{tenant-id-xxxx}/v2.0/well-know/openid-configuration”
* LOAD_USER_INFO | by default set it to true
* DEFAULT_TOKEN_EXPIRATION_RENEWAL_TIME | by default set it to 170
* AUTOMATIC_SILENT_RENEW = false | true (Emerald Global will authorize the user only once with the Emerald Global server, therefore, no refresh of the token is required).
* RETAILER_DOMAIN - "retailer.com the domain prefix".
* USER_UNIQUE_IDENTIFIER → EMAIL | UPN | OID ...
* IDP FORCE LOGOUT=FALSE | TRUE	by default set it to TRUE

**Example:**

![Open ID example](/Images/openidexample.png)

**Logout API:**

Create a new Logout API "/logout“ that is responsible for the update of the EXTERNAL provider and deletes the session when the user logs out from the CCM.

### Azure Account Setup 

This section describes how to register the CCM Application in Azure.

1. Create an account in azure using the following link.
https://azure.microsoft.com/en-us/get-started/azure-portal

1. Create a trial account by giving payment details.
Once you are successfully logged in, the Home page is displayed as follows:  
![Azure home page screen](/Images/azurehomepagescreen.png)

1. Host your React application in the above account.

1. Go to App Registration --> New Registration. The following page is displayed.
![New registration screen](/Images/newregistration.png)

1. Enter the details required, then click **Register**.  
Once registered, when you open the App registration Page the registered react app appears as follows:
![App registration screen](/Images/appregistrations.png)

1. On selecting the name provided under the **Display name**, the React OIDC_App page is displayed with all the relevant details:
![React OIDC_App screen](/Images/ReactOIDCAppscreen.png)

1. From the left-hand side column under the Overview, you can see the relevant details: Tenant ID, client ID etc, whose values need to be entered in our Configuration Entry Table.

1. Under the Authentication tab, enter the redirect Uri and the application hosted Url:
![Authentication tab](/Images/authenticationtab.png)
View the logout Url, as well as check the **ID token** checkbox
![Logout Url](/Images/logouturl.png)

1. In the Token Configuration screen, click the **+ Add Optional claim**. This required to decode the token we get for the optional claim and its corresponding values which we can further use to validate in Emerald Global.
![Add optional claim screen](/Images/addoptionalclaim.png)

1. From the left-hand side column, select Owners and click **+ Add owners**. The Owners tab is displayed. Only those who are owners can access the application.  
The following image show you how to find the owners. If you created an owner under the Users page (Home -> users-> create /invite users) the owners appear under the owner’s list.
![Owners screen](/Images/ownersscreen.png)

1. View the Roles and Administrators screen as follows:
![Roles and Administrators screen](/Images/RolesandAdministratorsscreen.png)

1. From the left-hand side column, select Overview > Endpoints.   
There are endpoints which are required in the development.
![Endpoints screen](/Images/endpointsscreen.png)
