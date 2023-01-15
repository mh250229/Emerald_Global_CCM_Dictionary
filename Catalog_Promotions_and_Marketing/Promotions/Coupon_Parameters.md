## Coupon Parameters

**Coupon Parameters** is used to define general coupon parameters, such as the coupon search logic or specifying the tender used for coupons manually entered by the cashier.

On scanning or manually entering a coupon at the touchpoint, the system validates the parameters, and applies the defined parameter value where relevant.

For example, the cashier scans a vendor coupon at the POS touchpoint. To determine which items the reward is applied to, the system checks the value defined in the Vendor Coupon Search Logic parameter in **Coupons Parameters** and applies the defined search logic.

Different parameters values can be configured in different Business Units.

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/Coupon Parameters*

![Coupon Parameters Screen](/Images/CouponParametersScreen.png)

|**Field**|**Description**|
|---------|----------|
|**ID**|The number and name of the store in which the coupon parameters are defined.|
|**Vendor Coupon Search Logic**|The search logic the Promotion Engine applies to a vendor coupon to determine the items the reward is applied to.
|**Coupon amount Limitation**|The limitations applied to the coupon amount when tendering with a coupon.|

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/Coupon Parameters/Add New*

![Coupon Parameters Form](/Images/CouponParametersForm.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which the coupon can be issued or redeemed.|
|**Manufacturer Coupons area**|Coupons issued by manufacturers to reward customers. These coupons are not issued in our system but can be redeemed. There are no predefined redemption promotions for these coupons. The redemption promotions are created by the Promotion Engine (PE) on the fly when the coupons are scanned, by a logic that is determined by the coupon type.<BR>Manufacturer Coupon rewards are handled as a tender.<BR>Two types of manufacturer coupons are supported: UPC5 and GS1 Databar.<BR>When a Manufacturer Coupon is scanned, the PE searches for items in the transaction that match the coupon. The rewarded items are retrieved by the Family Code or Manufacturer Code/Company Prefix. UPC5 coupons correlate to the Manufacturer Code, and Databar coupons to the Company Prefix.<BR>The search logic (Manufacturer Number/Company Prefix, Family Code or None) used to validate a coupon is configured in the Vendor Coupon Search Logic field.<BR>Each Manufacturer Coupon type should have a predefined data pattern. Databar Coupons have an 'extended' version of the Manufacturer Code used by UPC5 coupons. It may include additional digits, such as leading zeros and digits from the item’s barcode.<BR>All products produced by a specific company use the same manufacturer code.|
|Vendor Coupon Search Logic|The search logic used by the Promotion Engine to validate a coupon.<BR>The options are<BR>**None** - indicates that no search logic is applied<BR>**Manufacturer Number / Company Prefix** – The coupon reward is applied to items in the transaction that match the Manufacturer Number/Company Prefix of the scanned coupon.<BR>**Manufacturer / Company Prefix And Family Code** - The coupon reward is applied to the items in the transaction that belong to the Family Code and Manufacturer Number defined in the coupon data pattern.<BR>**Note:** A Family Code is assigned to a product by the Manufacturer to group products together within a family. For example, same size items but with a different flavor e.g., flavored mineral water.|
|Start Date Grace Period (days)|The number of days the coupon validity period can be extended before the coupon validity date. For example, if the Start Date grace period is 3 days and the validity period is from 13.7.3012 - 13.8.2013. The coupon can be accepted from 10.7.2013.<BR>The coupon validity period is defined when setting up the coupon data pattern.|
|End Date Grace Period (days)|The number of days the coupon validity period can be extended after the coupon validity period has expired. For example, if the End Date grace period is 3 days and the validity period is from 13.7.3012 - 13.8.2013. The coupon can be accepted up to 16.8.2013.<BR>The coupon validity period is defined when setting up the coupon data pattern.|
|Promotion Group|The Promotion Group the coupon is linked to. Promotion Groups define the execution priority of promotions and strategies for handling the use of multiple discounts.<BR> An explanation of the Promotion Groups grid, see *Organization/Promotions/Promotion Groups*.|
|Allow Multiply Coupon Rewards|Specifies if the coupon reward be multiplied. <BR>The options are:<BR>**No** - the coupon reward amount cannot be increased.<BR>**Double** - the coupon reward amount can be doubled.<BR>**Triple** - the coupon reward amount can be tripled.<BR>**Quad** - the coupon reward amount can be increased four times.<BR>**Note:** The coupon reward amount is funded by the manufacturer who issued the coupon, while the increased reward amounts are funded by the retailer.|
|**Manual Coupons area**||
|Manual Coupon Tender|The tender used to report the coupon reward when the coupon amount is manually entered by the cashier.<BR>For example, when a coupon barcode cannot be scanned, or cannot be entered. The cashier selects the Manual Coupon function, and the selected tender is displayed in Tender mode. The cashier then manually enters the coupon reward so that the customer can receive the reward.|
|Coupon Barcode Required|Indicates that the coupon barcode must be entered by the cashier after the coupon is scanned.|