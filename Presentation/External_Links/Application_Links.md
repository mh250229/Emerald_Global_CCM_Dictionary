## Application Links

Application Links displays the name of the external application that can be accessed from the CCM.

The application URLs are added via the ApplicationLinkMaintenance RTI. In addition, the external application ID is configured to the UserID or SessionId configured in the CCM.

When a user accesses an external application after having logged in to the CCM, the Session ID and User ID is validated, and if they have permissions and role permissions for that specific store, the user is automatically authenticated to access the external application.

**Reference Path:** *Presentation/External Links/Application Links*

![Application Links Screen](/Images/ApplicationLinksScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the application. The name is a link to the application, which when clicked opens the selected application.|
