## Online Authorization Messages

Online Authorization Messages displays the error messages displayed on a POS that are returned from the external providers upon receiving errors during communication with 3rd party providers via the GSE.

**Reference Path:** *Rules & Policies/Online Authorization/Online Authorization Messages*

![Online Authorization Messages Screen](/Images/OnlineAuthorizationMessagesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Target Provider**|The name of the provider, e.g., CVV, Internal, etc.|
|**Return Code**|The return code associated with the target provider.|
|**Touchpoint group**|The touchpoint group to which the message is associated.|
|**Message**|The message that is prompted when an error is returned.|

**Reference Path:** *Rules & Policies/Online Authorization/Online Authorization Messages/New Online Authorization Messages*

![Online Authorization Messages Form](/Images/OnlineAuthorizationMessagesForm.png)

|**Field**|**Description**|
|---------|----------|
|**Target Provider**|The name of the provider, e.g., CVV, Internal, etc.<BR>If the Target Provider is configured to ‘Internal’, and the integrated provider settings is configured to Retalix, Emerald Global takes the corresponding message configured for the Target Provider=Internal.<BR>If the integrated provider is not configured to get the message from Retalix, i.e., may be configured as CVV (external provider), it takes the specific Target Provider’s message.<BR>In a case where both options do not exist:<BR>* If a message was passed by GSE, Emerald Global takes this formatted message<BR>* If a message was not passed by GSE, the POS prompts the default message (i.e., the message from the server database, or the POS client resource file).|
|**Return Code**|The return code associated to the Target Provider. This a free text field and can be alphanumeric.<BR>The following error codes are sent by the GSE for internal problems:<BR>#120 – Training Mode<BR>#121 – Timeout<BR>#103 – Communication error|
|**Touchpoint group**|The touchpoint groups to which the message is associated. This is only relevant to a primary touchpoint group. If a touchpoint group is not selected, all touchpoint groups are associated.|
|**Message**|The message that is prompted when an error is returned.<BR>The message is of type ‘Provider’.|