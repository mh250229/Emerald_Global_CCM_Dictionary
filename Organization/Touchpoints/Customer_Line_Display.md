## Customer Line Display

The Customer Line Display module is used to import and export XAML files containing the text, location and fields displayed the Customer Line Display.

Each XAML file is imported into the CCM Office, and then linked to a specific Touchpoint Group and State.

When viewing the Customer Line Display, linked to the selected touchpoint group, the texts, fields and locations defined in the XAML file are displayed.

You can import as many XAML files as required, however only one XAML file can be linked to a specific State and Touchpoint Group.

In addition, you can modify the data in an XAML files by exporting the file, and changing the relevant fields. Once updated, you can then import the XAML file back into the CCM Office, and link the file to the relevant view and touchpoint group. All the changes are immediately applied.

The XAML files are saved locally.

**Reference Path:** *Organization/Touchpoints/Customer Line Display*

![Customer Line Display Screen](/Images/CustomerLIneDisplayScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Import XAML**|To import Customer Line Display configuration.|
|State|The State on the Customer Line Display in which the imported configuration is displayed.<BR>The supported States are:<BR><BR>CashChangeView<BR>CustomerDepositView<BR>CustomerView<BR>IdleView<BR>NoSaleView<BR>PersonalAccountView<BR>SaleView<BR>SignInView<BR>TenderView|
|Select File|To select the XAML file containg the configuration for the selected State.|
|Touchpoint Groups|The Touchpoint Group you want to the apply the imported Customer Line Display configuration.<BR>On selecting a Touchpoint Group, the imported configuration is applied only to the Customer Line Display in the selected Touchpoint Group.<BR>If a Touchpoint Group is not selected, the configuration is applied to Customer Line Displays in all the Touchpoint Groups.|
|**Export XAML**|To export Customer Line Display configuration. For example, if you want to edit the configuration, you can export the XAML file, and change the configuration and then import the updated file.|
|State|The State on the Customer Line Display in which the configuration is exported.<BR>The supported States are:<BR><BR>CashChangeView<BR>CustomerDepositView<BR>CustomerView<BR>IdleView<BR>NoSaleView<BR>PersonalAccountView<BR>SaleView<BR>SignInView<BR>TenderView|
|Select File|To select the XAML file containg the configuration for the selected State to be exported.|
|Touchpoint Groups|The Touchpoint Group from which you want to export the configuration|