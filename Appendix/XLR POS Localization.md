## XLR POS Localization

Emerald Global supports the ability to modify the text configuration for Messages, Titles, Labels, and Button text displayed on the XLR POS.

When there is no configured data available, the default text configuration is applied.

The text configuration is applicable per Retailer, Store, and Region.

The configuration is done via the DefaultResourcesManagement.xml file and then imported to Emerald Global.

The following steps describe how to update text that is displayed on the POS.

1. Go to the POS machine C:\Retalix\StoreServices\PosClient\Utils\Resources\RTI and Copy POSClient.POSClient.2.xml & POSClient.1.xml  
Then go to HQIIS machine and paste them into the following folder:  
C:\Retalix\StoreServices\Server\PosService\Utils\Resources\RTI 
1. Go to C:\Retalix\StoreServices\Server\PosService\Utils and Edit - RunPostInstall.cmd  
As follow (change the server URL to your HQIIS LAB)  
set ServerUrlMask=https://SRRAALABWHQIIS.QAlabdom.local/Storewebservices/{0}.rti?token={1}
1. Save the File
1. Execute RunPostInstall.cmd in the CMD prompt, enter User: QA Password: Qwe12345 – wait until it finishes processing. Check C:\Retalix\StoreServices\PosClient\Utils for the log file to see that it is completed.
1. Open the OfficeClient > Resources module.
1. From the Export section choose:
    * Application: POSClient
    * Version: Choose your version e.g., 5.14.11000
    * Context: POSClient
    * Culture: English (United Kingdom) `<You can choose any culture you need>`
1. Click the EXPORT button then wait for the ZIP file to be created and download it to your PC.
1. Open the Zip file and extract the files to any folder (make a note where it located).
1. Open the file, e.g., POSClient.en-GB.resx (recommended via Visual Studio for easy table view of parameters)
1. Change the parameter you want to translate and Save the file (example: Name: UCLoginScreen_Hello.Text  Value: Hello > Change Value to: Hello World then SAVE.
1. Open the OfficeClient > Resources module
1. From the Import section choose:
    * Choose File: direct it to your translated POSClient.en-GB.resx
    * Application: POSClient
    * Version: 5.14.11000 (example: choose your version)
1. Click IMPORT, then wait for the message “resources file import completed”
1. Open the POS (on the first screen you should see Hello World)






