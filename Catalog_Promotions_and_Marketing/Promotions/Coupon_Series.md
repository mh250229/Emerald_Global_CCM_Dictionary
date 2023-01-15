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

The Attributes tab defines general coupon series attributes and link promotions to the different coupon series.
