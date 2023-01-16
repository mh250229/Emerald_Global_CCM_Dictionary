## Coupon Series

**Coupon Series** is used to define a coupon series, which are a ranges of coupons based on defined attributes that can be controlled centrally.

Each coupon series can be set up with specific attributes to determine how the system handles the coupon when identified at the touchpoint. Once the coupon is scanned, the system validates the rules defined for that coupon series, for example, how many times the coupon can be scanned in one transaction, can the reward be entered manually, or is the cashier allowed to override the coupon reward, etc. Specific conditions are defined which determine how the coupon is handled.

Each coupon series is linked to a single Data Pattern, which defines the barcode structure, and can comprise a number of coupon instances.  A coupon Instance is a sub-group of a Coupon Series. Its unique identifiers are the Series ID and Offer Code.

Single and multi-coupon instances can be linked to a single Coupon Series and their properties are inherited from the Coupon Series properties. However, each instance can be defined with a range of specific attributes at the instance level, overriding the general coupon series attributes.

**Coupons Repository (Database)**

Coupons are saved in the Coupons Repository (database). The Coupons Repository is considered the third level after the Coupon Series and Coupon Instance. The Coupon Repository holds the full barcodes for each coupon that is either issued by Emerald Global during promotions or imported from an external system.

Each coupon in the Coupons Repository is linked to a Coupon Instance. The connection between a coupon instance and coupon in the Coupon Repository is 1 to many. The data saved for each coupon may consist of a combination of many fields (optional), e.g., Reward Value, Validity Period (start and end dates), Blocked indication, Customer ID, etc.

The coupons are saved in the Coupons Repository to accommodate unique coupon mechanisms, same household mechanisms, customer specific unique business scenarios, described in the Business Coupon Types section.

Coupons that are not valid or contain the wrong coupon format are rejected at the POS touchpoint, and prompt different errors, for example, Coupon Has Expired, Invalid Coupon Format, Coupon Does Not Correspond to Known Promotion, Purchase Does Not Include Products Needed to Qualify for the Promotion, etc.

The following Business Coupon types are supported:
* Unique Coupons
* UPC5 Coupons
* Databar Coupons

**Coupon Issuing**

An issuing coupon is the coupon reward issued during a promotion.

For example, Buy 3 Pizzas, Get a $5.00 off Coupon for your next Pizza purchase. If the customer purchases 3 pizzas, the promotion is triggered.
There are two issuing coupon types:

* **Coupon Instance** - coupon instances are linked to promotions in order to issue a coupon reward. On creating the promotion, the coupon reward is linked to the Coupon Instance. A Coupon Instance is a specific coupon within a Coupon Series, and the Coupon Series is always linked to a matching Data Pattern. When the promotion is triggered, the system identifies the coupon instance linked to the promotion. The system prints the coupon with a barcode, which is printed according to the defined Data Pattern structure linked to the Coupon Series, containing the Coupon Instance. The barcode includes a reward value. When the coupon is redeemed, the system validates the barcode that was issued before triggering the reward. See Coupon Redemptions.
* **Full Coupon Barcode** - a predefined full barcode can be linked to a promotion to issue a coupon reward. A full barcode indicates that the exact full barcode, defined in the Barcode field in the Coupon Reward option is printed on the coupon receipt when the promotion is triggered. When the coupon is redeemed, the system validates the barcode against the data pattern, which is linked to a Coupon Series.

**Coupon Redemption**

A coupon redemption promotion is the option of using a coupon to redeem the reward in a promotion.

For example, the customer has a coupon that specifies Buy 3 Pizzas, Get $5.00 off your next Pizza purchase. If the customer purchases 3 pizzas and presents the coupon, the promotion is triggered and $5.00 is deducted from the total amount.

A redemption promotion may be created according to different options:

* Option 1:  
The coupon is issued according to a predefined barcode. In this scenario, the redemption promotion must be configured with the full predefined barcode as a condition, which must be met, i.e., the coupon triggers the promotion in order to redeem the promotion reward. The coupon value is generally embedded in the barcode, which is linked to a data pattern.
* Option 2:  
The coupon is issued according to a Coupon Instance, which is part of a Coupon Series. In this scenario, the redemption promotion must be configured with the Coupon Instance as the condition.
During the transaction, when the coupon is scanned, the system identifies the Coupon Instance, and the Coupon Series, which is linked to a Data Pattern.
If all conditions are met, the promotion reward is redeemed. The reward is retrieved according to the reward logic.
A redemption promotion can be linked to many Coupon Series and many Coupon Instances.

All coupon redemptions are recorded in the Tlog for reporting and tracking purposes. Once a coupon is redeemed, you can track it by the Coupon Barcode, Coupon Amount, or Offer Code.

**Coupon Reward Logic**

Upon triggering a redemption promotion, the reward is given according to the following logic:

* If the coupon exists in the coupon repository and is updated with a reward value, the reward is taken from the coupon repository.
* If the coupon does not exist in the coupon repository, the reward is taken from the coupon’s barcode (‘Reward Value’ attribute in the matching data pattern).
* If the embedded Reward Value is equal to the definition in the Coupon Series in a field called ‘Prompt Reward Value’, the reward must be entered by the cashier/attendant.

If there is no embedded reward, the reward is retrieved from the promotion (=‘Triggering Coupon’).

* If there is no redemption promotion defined, however the Coupon Series is defined with a ‘Fallback Strategy’: 
* If the coupon exists in the coupon repository with a reward value, the reward is taken from the coupon repository, and the reward type (amount off or points) is calculated according to the fallback definition.
* If the coupon does not exist in the coupon repository, the reward is taken from the coupon’s barcode (‘Reward Value’ attribute in the matching data pattern).
* If the embedded Reward Value is equal to the definition in the Coupon series in a field called ‘Prompt Reward Value’, the reward is entered by cashier.

If the coupon does not have an embedded reward, a dead end is reached, and the coupon cannot be accepted.

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/Coupon Series*

![Coupon Series Form](/Images/CouponSeriesForm.png)

|**Field**|**Description**|
|---------|----------|
|**ID**|The unique ID of the coupon series.|
|**Name**|The name of the coupon series.|
|**Data Pattern**|The name of the data pattern (barcode) to which the coupon series is linked.|
|**Printing Template**|The name of the template to which the coupon series is linked. You can connect a single message to a coupon series. This message would be Type - Voucher, and is the message printed when the coupon is issued.|

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/Coupon Series/Add New*

![Coupon Series Add New](/Images/CouponSeriesAddNew.png)

|**Field**|**Description**|
|---------|----------|
|**ID**|The unique ID of the coupon series.|
|**Name**|The name of the coupon series.|
|**Data Pattern**|The name of the data pattern to which the coupon series is linked.|
|**Printing Template**|The name of the template to which the coupon series is linked.|
|**Attributes tab**|Defines specific attributes to determine how the system handles the coupon when identified at the touch point.<BR>Each coupon series can be comprised of a number of coupon instances. Each instance inherits the specific coupon series’ defined attributes|
|**Coupon Instances tab**|Defines the instances in each coupon series, and comprises a number of coupons.<BR>A coupon instance is a refinement of coupon series; Its unique identifiers are the ‘Series ID’ and ‘Offer Code'. Each instance inherits the specific coupon series’ defined attributes, however, can override them with its own attributes.|

### Attributes Tab

The **Attributes tab** defines general coupon series attributes and link promotions to the different coupon series.

![Attributes Tab](/Images/AttributesTab.png)

|**Field**|**Description**|
|---------|----------|
|**External System Validation Required**|Indicates that coupons require validation by an external system (Extension Code). Only if the coupon passes validation is it accepted.|
|**Member Card Required**|Indicates that a loyalty card must be scanned/entered in the transaction. If this option is defined, on scanning a coupon from the specified series, and a member card has not been scanned, the system prompts the cashier to scan/enter a member’s loyalty card.<br>**Note:** This attribute can be overridden for coupon instances.|
|**Coupon Issuing By External System**|Indicates that the coupon series is issued by an external system. The online integration is handled by extension.|
|**Requires External Barcode Generation**|Indicates that the system does not issue the coupon data and uses an external system to retrieve the coupon data when the issuing promotion is triggered.<br>**Note:** This parameter is only displayed if the Coupon Issuing By External System parameter is selected.|
|**Blocked**|Indicates that the coupon series is blocked. When scanned, the coupon is rejected and a message is prompted, for example, 'Sorry the coupon is not valid'.|
|**Virtual Coupon**|Indicates that the coupon series includes electronic coupons, for example, coupons with a barcode on a mobile application that can be scanned by the cashier or at the self-checkout, and the customer is not required to hand the cashier a paper coupon.<br>If a virtual coupon is scanned and not used, the coupon barcode will not be displayed in the unused coupons message after payment.|
|**Allow Coupon Override**|Indicates that **Min** / **Max** values must be entered.  Enables the cashier to select the coupon line in the transaction and override predefined reward values. The system validates if the manually entered reward is within the Min/Max threshold values.<br>For example, if the Min is 10 and Max is 20, the maximum reward value entered manually for a coupon from this coupon series is 20, and the minimum value is 10. Any amount above 20 or below 10 is rejected, and an error message is prompted.<br>You can configure a business rule to determine the action taken when the defined threshold is reached. If the cashier exceeds the threshold, then an error message is prompted. The message, the action (prohibit/information/manager's approval) and thresholds per role are defined in the Business Rules|
|**Prompt Reward Value**|If no value is defined, the cashier cannot manually enter a reward value. If it is 0, the cashier is always prompted to enter a reward value.<br>When the number of digits defined in the Prompt Reward Value field equals the number of digits in the embedded reward value in the scanned coupon barcode in the coupon series, the cashier is automatically prompted to enter the reward.<br>Generally, the value 000 or 999 indicates that the system must prompt the cashier to enter the reward value manually.<br>For example, if the retailer wants to give a reward that is greater than 9.99. You can enter three digits, 000 or 999, and when the coupon is scanned, the cashier is prompted to manually enter the coupon reward.<br>The new reward must be within the minimum and maximum coupon values allowed.|
|**Fallback Reward**|The fallback strategy used when the scanned coupon (part of a coupon series) does not trigger a promotion.<br>The options are:<br>**Points** – the coupon reward is issued as points, and you can select the Member Account in which the points are accumulated. When selected, the Account ID must also be entered.<br>For example, the system is setup as follows:<br>*Fallback Reward* – Points<br>*Account ID* - Account 10<br>*There is no promotion with this coupon defined as its condition.<br>When the cashier scans the coupon, the coupon is accepted.<br>The coupon reward value, e.g., 100 points (embedded reward) is added to the customer member account #10.*<BR>**Amount Off** – the reward is issued as an amount off the product price. The Amount Off reward can be recorded as a discount or as a tender. When selected, the Tender Type can also be entered.<br>For example, the system is set up as follows:<br>*Fallback Reward* - Amount Off<br>*Tender Type* - Cash<br>*There is no promotion with this coupon defined as its condition.*<br>When the cashier scans the coupon, the coupon is accepted. The coupon reward value (embedded reward) is added to the transaction as a cash tender.<br>**Note:** If a Tender Type is not selected, the coupon reward is recorded as a discount.|
|Max Allowed Coupon’s Scanned|The maximum number of coupons (linked to the same coupon series) that can be scanned in the same transaction.<br>For example, you may have a Fixed Points coupon series with Max Allowed Scans defined as 2. The cashier scans the first coupon, and the reward is given. The cashier scans the second coupon and again the reward is given. Then the cashier scans a third coupon, and the coupon is rejected.<br>Not relevant for coupons triggered as part of the Fallback Strategy OR manually entered at the POS and do not trigger a promotion.|
|Max Same Barcode Scans|The number of times the same barcode can be scanned to redeem a coupon at the POS terminal in the same transaction.  Enables the retailer to control the number of same barcode coupon redemptions in a single transaction.|
|Redemption Segmentation|To specify that only members of the same household can redeem the coupon.<br>The options are:<br>**Undefined** - The coupon can be redeemed by any customer. When selected, you must select Unlimited from the Redemption Limit drop-down list, as the coupon cannot be tracked and a redemption limit cannot be enforced. This is the default option.<br>**Same Household** - The coupon can be redeemed by any member of the same household. When selected, the coupon series can be saved with either Redemption Limit option - Single Redemption or Unlimited. If the Single Redemption option is selected, the system validates that the coupon was not already redeemed.<BR>Members are linked to households in the Customer module.|
|Redemption Limit|specify if the coupon can be redeemed more than once. The options are:<br>**Unlimited** - The coupon can be redeemed more than once (default)<br>**Single Redemption** - The coupon can only be redeemed once.|
|**Linked Promotions section**|The promotions linked to a coupon series. Each promotion can be opened in a separate office tab, viewed and edited.|
|Description|The name of the promotion linked to the coupon instance.|
|Linkage type|The context of the coupon’s link to the promotion, i.e., as an issuing or redemption promotion.|

### Coupon Instances Tab

The **Coupon instances** tag defines the subsets of a coupon series. Some properties can be overridden by the coupon instance properties (examples: printing message, tender ID in case of a fallback scenario etc.).

You can also block an instance within the coupon series.

![Coupon Instances Tab](/Images/CouponInstancesTab.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the coupon instance series.<br>**Note:** The list of coupon instances can be filtered by Name and Offer Code.|
|**Offer code**|The logical link between the issuing and redemption promotions linked to the coupon. The Offer Code is embedded in the coupon barcode, and when the coupon is scanned, facilitates identifying the triggering promotion.|
|**Override**|Indicates if the coupon reward for the defined coupon instance can be overridden. If Yes, the cashier can select the coupon line in the transaction and override the value.|
|**Attributes section**||
|Printing Template|The template linked to the coupon instance. This field is integrated with the Message module, and the user can access the Message module to create a new message. If no special template is selected, the Printing Template linked to the coupon series in the Attributes tab is used.|
|Tender Type|The tender that is logged when the defined coupon is redeemed.<br>Note: Coupons that trigger promotions configured as Reward As Tender have their tender defined from the promotion and not the coupon settings. If the Promotion is not found the system retrieves the Tender from the Coupon Settings.|
|Member Card Required|A loyalty card must be scanned or entered during the transaction to accept a scanned coupon (a message is prompted if it has not).<br>This option is only enabled if the checkbox is selected.|
|Blocked|The coupon instance within the coupon series is not valid. When a blocked coupon is scanned at the POS, a message is prompted that the coupon is no longer valid.<br>This option is only enabled if the checkbox is selected.|
|Virtual Coupon|The coupon instance within the coupon series is a virtual coupon. Electronic or virtual coupons are added to loyalty member accounts via a website. The coupons are automatically redeemed during a sales transaction in which the customer meets the condition required to trigger the coupon.<br> Note: If the Coupon Series is virtual, then the coupon instance is also a virtual coupon even if this field is set to No.<br>This option is only enabled if the checkbox is selected.|
|**Linked Promotions section**|Defines the promotions linked to the coupon instance. Each promotion can be opened in a separate office tab, viewed and edited.|
|Description|The name of the promotion linked to the coupon instance.|
|Linkage type|Redemption promotion or Issuing promotion.|
|**Coupons section**||
|Barcode|The full barcode coupon which is linked to each coupon instance.|
|Reward Value|The coupon reward value.<br>Upon triggering a redemption promotion, the coupon reward will be given according to the following logic:<br>If there is a reward value linked to the coupon (barcode level), this reward value will be given.<br>If there is no reward value linked to the coupon, the reward value which is embedded inside the barcode will be retrieved.<br>If this is an embedded reward = coupon series prompts reward value, the reward will be retrieved from the cashier’s entry.<br>If no reward is embedded in the coupon (i.e. the coupon is a ‘trigger coupon’), the reward will be taken from the promotion.|
|Start Date|The date from which the coupon is valid.|
|End Date|The date from which the coupon expires.|
|Blocked|The coupon is blocked if either the coupon full barcode/coupon instance OR coupon series is defined as 'Blocked'.<br>When scanned at the POS, a blocked coupon is rejected.|
|Status|Indicates if the coupon has been redeemed. The options are:<br>**Active** - the coupon has not been redeemed.<br>**Redeemed** - the coupon has been redeemed and is no longer active in the system. The coupon is blocked and rejected.|