## UPC5 Value Codes

**UPC5 Value Codes** display the predefined codes for redemption values in UPC5 coupons. UPC5 Coupons are also known as vendor coupons. On scanning a UPC5 coupon, a tender is automatically added to the transaction, which has a value according to the UPC Coupon value code. The reward is retrieved from the coupon, reducing the ticket balance accordingly. UPC5 coupons represent a promotion type. The coupon reduction amount is treated as a tender.

**UPC5 coupon barcode structure:**

* **Prefix** – Always 5 (UPC5)    [**5**] 12345 87890 4
* **Manufacturer Number** - identifies the manufacturer of the item linked to the coupon. In item UPCs, the same 5 digits reflect the manufacturer of the item. 5[**12345**] 87890 4
* **Family Code** – this is a type of item reference number assigned by the manufacturer, to group products together within a family. For example, same size items but with different flavors e.g., flavored mineral water. The Family Code is added as an attribute to a product, and once assigned, remains the same through the lifetime of that product. 5 12345 [**878**]90 4
* **Value Code** – redemption value of the coupon based on a predefined value code table. This code table is created and distributed by a joint industry coupon committee. 5 12345 878[**90**] 4

For example: Value Code 05 represents $1.40 Off, Value Code 07 represents Buy 3 or more get $1.50 Off.

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/UPC5 Value Codes*

![UPC5 Value Code Screen](/Images/UPC5ValueCodeScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Code**|The two-digit value code that identifies the value of the coupon.
|**Face Value**|The reward type issued for each value code, e.g., Free Merchandise, Buy X - Get Y Free<BR>**Get Value** - The reward amount or value received when the coupon is redeemed. For example, Value Code 41 represents Buy 3 or more get $0.50 off. In this example, the Get Value is $0.50.<BR>**Buy Quantity** - The amount or value that triggers the promotion linked to the coupon. For example, Value Code 41 represents Buy 3 or more get $0.50 off. In this example, the Buy Value is 3.|
|**Value**||

**Reference Path:** *Sales/General/UPC5 Value Codes*

![UPC5 Value Code Form](/Images/UPC5ValueCodeForm.png)

|**Field**|**Description**|
|---------|----------|
|**Value Code**|The two-digit value code that identifies the value of the coupon.|
|**Face Value**|The reward type issued for each value code, e.g., Free Merchandise, Buy X - Get Y Free|
|**Get Value**|The reward amount or value received when the coupon is redeemed. For example, Value Code 41 represents Buy 3 or more get $0.50 off. In this example, the Get Value is $0.50.-|
|**Buy Quantity**|The amount or value that triggers the promotion linked to the coupon. For example, Value Code 41 represents Buy 3 or more get $0.50 off. In this example, the Buy Value is 3.|