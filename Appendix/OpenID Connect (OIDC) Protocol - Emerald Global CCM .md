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

### Logging in to the CCM

1. Set the Authentication Mode = OIDC (External) in the Security Policy screen.
1. Perform an IIS Reset if the UI is not updated.
![CCM Authentication Mode screen](/Images/ccmauthenticationmodescreen.png)
Once the **Authentication Mode** is set to **OIDC**, the Log in page is displayed as follows. Only the User Name field is available.
![CCM log in screen](/Images/ccmlogin.png)
![CCM enter password screen](/Images/ccmenterpasswordscreen.png)
Once you enter the User Name, the following parameters are checked and only when they pass validation, you can login.
* The configuration Entry table should have data related to OIDC
* The Domain Name of the User Name should match the Retailer’s Domain Name value in the Configuration Entry table

Once you have logged in from the External IDP, the Emerald Global server validates the token which is passed in the header, and performs the following:
* Checks if the **Creation Time (Issued at "iat") is not more than 60 secs and if "nbf" is valid**.
* Checks if the ‘Token’ is valid and if we can decode and use the ‘USER_UNIQUE_IDENTIFIER’ (Each EXTERNAL IDP provider can have a different option for the identifier value → UPN/EMAIL/OID/ etc.), then check that this identifier value from the decoded token exists in the database (IN ‘AppUser’ table → ‘DomainUserName’ column).

ONLY if the ‘USER_UNIQUE_IDENTIFIER’ (UPN/EMAIL/OID ) is found on our side, an Emerald Global session is created. A user must be added to the App_Users table with the Domain Name that matches the USER_UNIQUE_IDENTIFIER.

Only when the above two conditions are satisfied, the Emerald Global session is created and you are successfully logged into the CCM.

### Logout Mechanism

Once you select CCM Logout, it checks if the IDPForceLogout is set to true and if you are an external user, and then redirects you to log out from both the CCM and the external Authenticator.

The following screen is displayed, and when you select your account, you are logged out of both.

![Sign out Pick an account screen](/Images/signoutpickanaccountscreen.png)

### RTIs

The following RTI is used to enter the data in the Configuration Entry Table.

```json
<?xml version="1.0" encoding="utf-8"?>
<ConfigurationMaintenanceRequest MajorVersion="1" xmlns="http://retalix.com/R10/services" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://retalix.com/R10/services file:///D:/Development/R10/Contracts/Src/Retalix.Contract.Schemas/Schema/Services/Configuration/ConfigurationV1.0.0.xsd">
  <RequestHeader />
  <Configuration Name="OIDC">
    <ConfigurationEntry>
      <Entry>Authority</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.String</ValueType>
      <DefualtValue />
      <Value>https://login.microsoftonline.com/8ee2cc4f-c54d-4001-b8bc-96627668a305</Value>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>AutomaticSilentRenew</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.Boolean</ValueType>
      <DefualtValue>false</DefualtValue>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>ClientID</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.String</ValueType>
      <DefualtValue />
      <Value>3eecee8a-32ec-4994-8af2-eda6897e5f10</Value>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>ClientRoot</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.String</ValueType>
      <DefualtValue />
      <Value>http://localhost:3002/</Value>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>ClientScope</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.String</ValueType>
      <DefualtValue />
      <Value>openid profile email</Value>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>DefaultTokenExpirationRenewalTime</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.Int32</ValueType>
      <DefualtValue>170</DefualtValue>
      <Value>170</Value>
    </ConfigurationEntry>   
    <ConfigurationEntry>
      <Entry>IdpForceLogout</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.Boolean</ValueType>
      <DefualtValue>true</DefualtValue>
      <Value>true</Value>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>IdpOpenIdConfiguration</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.String</ValueType>
      <DefualtValue />
      <Value>https://login.microsoftonline.com/8ee2cc4f-c54d-4001-b8bc-96627668a305/v2.0/.well-known/openid-configuration</Value>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>LoadUserInfo</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.Boolean</ValueType>
      <DefualtValue>true</DefualtValue>
      <Value>true</Value>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>RedirectURI</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.String</ValueType>
      <DefualtValue />
      <Value>http://localhost:3002/signin-callback</Value>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>ResponseType</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.String</ValueType>
      <DefualtValue />
      <Value>code</Value>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>RetailerDomain</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.String</ValueType>
      <DefualtValue />
      <Value>asda.com</Value>
    </ConfigurationEntry>
    <ConfigurationEntry>
      <Entry>UserUniqueIdentifier</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.String</ValueType>
      <DefualtValue />
      <Value>upn</Value>
    </ConfigurationEntry>
     <ConfigurationEntry>
      <Entry>MaxTokenIatAgeActiveTimeInSeconds</Entry>
      <Description TypeCode="Long" />
      <ValueType>System.Int32</ValueType>
      <DefualtValue />
      <Value>360</Value>
    </ConfigurationEntry>
  </Configuration>
</ConfigurationMaintenanceRequest>
```

OIDCConfigurationLookupRequest RTI example:

```rti
<OIDCConfigurationLookupRequest xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" MajorVersion="1" xmlns="http://retalix.com/R10/services">
  <Header>
    <MessageId Name="R10 Client" Timestamp="2023-03-16T14:25:22.8965127Z">424</MessageId>
  </Header>
</OIDCConfigurationLookupRequest>
```

**Note:**

On logging in to Spooky, the POS continues with the internal users using the user name and password, even if the system is configured to OIDC.