## Till Business Period

**Till Business Periods** (edit) is used to view, modify, approve, and settle the accounts in a Business period in a store operating in Till Accountability.

**Note:** In Cashier Accountability, the Cashier Business Period is displayed.

**Reference Path:** *Cash Office/Business Periods/Till/Cashier Pending Periods/Edit*

![Till Business Period Screen](/Images/TillBusinessPeriodScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store for which the Till Business period is shown.|
|**Started**|The date from which the Business Period started.|
|**End by**|The date on which the Business Period ended.|
|**Business Periods**||
|Account|The touchpoint account in the Touchpoint Group. The hyperlink opens the Till Transactions. See also: [Till Transaction.](<../../Cash_Office/Business_Periods/Till Transactions.md>)|
|Opening Amount|The money that came in from sales, loans, Paid-in's, etc.|
|Expected Amount|The money that was taken out of the touchpoint by pickups, paid-out, etc.|
|Over / Short|The actual over/short amount in each touch point account. For example:<BR>* Over amounts have a red up arrow ![Red Up Arrow](/Images/reduparrow.png) and a positive number with the text “(Over)” next to the amount.<BR>* Short amounts have a red down arrow ![Red Down Arrow](/Images/reddownarrow.png) and a negative number with the text “(Short)” next to the amount.<BR>* Balanced accounts have the text “Balanced” in green.
|Approve|Indicates that the account is approved. Accounts are approved only when balanced or when the Over/Short amount has been approved. When approving an Over/Short amount, a reason must be given. Once an account is approved, the user can perform a settlement to balance the period.<br>On approving a Cashier Account, if configured, a cashier report is automatically printed at shift closing via an External Application.<br>This is configured via the ApplicationLinkMaintenance RTI.<BR>The ApplicationLinkMaintenance RTI must be configured as follows:<br>* Name = Link - Report<br>* linkType = CashierReport<br>* hideLink = true (indicates the link is available from the CCM/Cash Office / Edit Till/Cashier Pending Period screen.)<br><br>On selecting Approve, the system sends a request to check the linkType parameter value defined, and if the parameter is set to CashierReport, a new tab is opened that redirects the system to the URL link defined in the ApplicationLinkMaintenance RTI.<br>Emerald Global sends the following information in the request to the external application, which is used by the External Application to print the cashier report at shift closing:<br>* Start Period Date Time<br>* End Period Date Time<br>* Cash Office Account ID<br>* Cashier Name (only relevant to the Cashier and Drawer Accountability environments)<br>* Shift Time (only relevant to Cashier Accountability environments)<br>* Store ID<br>* Session ID<br>* Logged in User ID – to start the session<br><br>RTI Example<br>
```json
<ApplicationLinkMaintenanceRequest xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" MajorVersion="1" xmlns="http://retalix.com/R10/services">
  <Header>
    <MessageId Name="777" />
  </Header>
  <ApplicationLinks>
    <!--Available Action:'Add','Update','Delete' -->
    <ApplicationLink Action="Add">
      <Name>Link - Report</Name>
     <Url>https://stackoverflow.com/questions/7256142/way-to-quickly-check-if-string-is-xml-or-json-in-c-sharp/</Url>
       <LinkType>CashierReport</LinkType>
       <HideLink>true</HideLink> 
      <AuthenticationMode>UserID</AuthenticationMode>
    </ApplicationLink>
  </ApplicationLinks>
</ApplicationLinkMaintenanceRequest>
```
|Reason|The reason for the over/short amount. A reason must be entered before a short or over business period can be approved.|