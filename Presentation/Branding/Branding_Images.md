## Branding Images

**Branding Images** is used to add, change or delete branding images from the POS and Customer Display screens.

Users can select the screen on which you want the image displayed, indicate the position of the image for each screen, as well as specify the touchpoints, touchpoints groups and business units in which the image is displayed. If an image is not associated to a Touchpoint Group, it is applied to all Touchpoint groups. If an image is assigned to both a primary and secondary touchpoint group, the secondary touchpoint group is taken in to account. Images can be added, changed or deleted. There are default local images in case no image was uploaded for a certain view.

Images can be added, changed or deleted. Any supported image format, e.g., jpg, jpeg, bmp, png, gif, can be added. The supported file size is 3mb by default but can be changed by configuration

The configured image list is located in a js file, which is saved by the POS on the local disk in the same location as the PosClient/GraphicsCustomerDisplayBanners files (Default images). The HTML includes a link to the external file and a script to set and manage the images based on the image format, i.e., Jpg, png, etc. The HTML file reads the image file names from the js file and display the files accordingly.

If no image is uploaded for a specific screen, the system applies the default image. Each default image is hardcoded and saved as HTML files which are associated to a specific screen.

The default images include:

* PosClient\GraphicsCustomerDisplayBanners
* ActionOnbanner.html
* Banner.html
* LaneClosebanner.html
* Salebanner.html
* Tenderbanner.html
* TenderWithActionbanner.html

**Reference Path:** *Presentation/Branding/Branding Images*

![Branding Images Screen](/Images/BrandingImagesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Business Unit**|The business unit in which the images are displayed.
|**Touchpoint Type**|The touchpoint type in the selected Business Unit to which the images are displayed.<br>The touchpoint type in the selected touchpoint group on which the images are displayed|
|**Touchpoint Group Type**|The touchpoint group type either Primary or Secondary in which the images are displayed.<br>For example, all POS touchpoints are assigned to the same Primary Touchpoint Group, however, some of the POS touchpoints may require a different images. Those POS touchpoints are assigned to a Secondary Touchpoint Group, and different Branding images are assigned to the Secondary Touchpoint Group only. The Branding Images are then applied only to the touchpoints in the Secondary Touchpoint Group and not to all the touchpoints in the Primary Touchpoint Group.
|**Touchpoint Group**|The specific touchpoint group containing the touchpoints you want to assign the Branding Images.|
|**Left Pane**|Displays the POS states/screen in the Customer Display, and Cashier Display in which an image can be applied, as well as the option to add a logo to the CCM Office.|
|**Customer Display**|Lists the screens on which the images are displayed on the Customer Display.|
|Lane Closed|The screen displayed when the POS is closed, locked , or logged out.|
|No Sale (Next Customer)|The screen displayed when the POS is in Idle mode (Next Customer Please).|
|Sale Mode Ads (No Action Window)|The screen displayed in Sale Mode when there are promotions/advertisements without the Action Window.<br>Images can be positioned in three positions: Upper, Middle, Bottom.|
|Sale Mode Ads (With Action Window)|The screen displayed in Sale Mode when there are promotions/advertisements and the Action Window is displayed.<br>Images can be positioned in two positions: Middle, Bottom.|
|Tender Mode Ads (No Action Window)|The screen displayed in Tender Mode when there are promotions/advertisements without the Action Window.<br>Images can be positioned in three positions: Upper, Middle, Bottom.|
|Tender Mode Ads (With Action Window)|The screen displayed in Sale Mode when there are promotions/advertisements and the Action Window is displayed.<br>Images can be positioned in two positions: Middle, Bottom.|
|**Cashier Display**|Lists the screens on which the images are displayed on the Cashier Display/POS.|
|Logo|The logo image displayed on all the screens on the POS.<br>The image is placed in a set position and cannot be moved.<br>The Position option is not enabled.|
|Logo (Training Mode)|The logo image displayed on all the screens on the POS when working in Training Mode.<br>The image is placed in a set position and cannot be moved.<br>The Position option is not enabled.|
|No sale mode (Right up)|The image is displayed in the top right side in the No Sale screen.|
|PLU menu (Right up)|The image is displayed in the top right side of the PLU Menu screen.|
|Thank you prompt (Cashier/Customer)|The image displayed in the Thank you screen displayed on the Cashier and Customer Displays.|
|Item not found prompt|The image displayed on the item not found screen displayed when a scanned item is not found.|
|Login Screen|The Cashier Login screen used to log in to the POS.|
|**CCM Office**||
|Logo|The logo image displayed on the screens in the CCM Office. The image is placed in a set position and cannot be moved.<BR>The Position option is not enabled.|
|**Grid**||
|Image|The image name and type displayed on the selected screen.<BR>Once the image is added, the image type, e.g., MP4 (Video), JPEG, BMP, PNG, GIF is automatically populated next to the image name.<BR>The following image formats are supported:<BR><BR>**States**<BR>Lane Closed<BR>No Sale (Next Customer)<BR>**Image File Formats**<BR>JPG, JPEG, BMP, PNG, GIF<BR><BR>**States**<BR>Sale Mode (No Active Window)<BR>Sale Mode (With Active Window)<BR>Tender Mode (No Active Window)<BR>Tender Mode (With Active Window)<BR>Logo<BR>Logo (Training)<BR>Login Screen<BR>**Image File Formats**<BR>JPG, JPEG, BMP, PNG, GIF|
|Business Unit|The business unit in which the selected images are displayed on the touchpoint.|
|Touchpoint Type|The touchpoint type: POS, QSR, Fuel POS, KeyBoard POS, and Self Checkout.|
|Touchpoint Group|The main Touchpoint Group the touchpoint is assigned to.|
|Secondary Touchpoint Group|The secondary Touchpoint Group the touchpoint is assigned to.|
|Position|The position the image is displayed in the selected screen.|
|Display Condition|Specifies when the image is displayed. You can configure default images that are displayed on the Customer Display and additional images displayed specifically for when a Loyalty card is added to the transaction.<BR>In a scenario in which the store configures different images for the same Store, Touchpoint, and Touchpoint Group for the same positions, the Loyalty images are displayed only if a loyalty card is identified, otherwise the default images are displayed.<BR>The options are:<BR>Default - indicates that the image is displayed on the Customer Display<BR>Loyalty - indicates that the image is displayed only when a Loyalty card is added to the transaction.<BR>**Note:** The ‘Loyalty’ option is relevant only to the Customer Display and not the Cashier Display.|
