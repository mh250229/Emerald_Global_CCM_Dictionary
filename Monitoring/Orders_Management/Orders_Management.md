### Orders Management

**Orders Management** enables you to track customer orders via an online snapshot of the current active customer orders in the system.

A Customer Order is a transaction that is not yet paid. Transactions are defined as customer orders until the payment stage, and if the transaction does not reach the stage of full payment, it remains a customer order. Once full payment is made, the customer order becomes a retail transaction.

Customer orders can be created on different touchpoints, for example, Self Scan devices, Home Shopping applications, Mobile Shoppers, such as smart phones, etc.

The module enables the option of filtering the customer orders view according to different criteria parameters.

**Reference Path:** *Monitoring/Orders Management/Orders Management*

![Orders Management Screen](/Images/OrdersManagementScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store to which the customer order is linked.|
|**Creation Channel**|The channel the Customer Orders were originally generated on.<BR>The available channels include:<BR>* **POS** - the regular point of sale<BR>* **SelfScanDevice** - a self-service solution that enables customers to scan their own items<BR>* **SelfScanEU** - a touch screen kiosk located at the front of the store from which shoppers release a self-scan device for self-scan shopping and which communicates with them.<BR>* **SelfCheckout** - a self-service solution for customers purchasing items. The customer scans and bags the items themselves.<BR>* **FuelPOS** - Not yet supported<BR>* **Homeshopping** – a web application to purchase items over the web<BR>* **KeyboardPOS** - a non-touch POS terminal|
|First Name|The name of the customer for whom the Online Order was generated.|
|Last Name|The surname of the customer for whom the Online Order was generated.|
|Loyalty Member Card|The customer's Loyalty Card number.|
|**Orders Found grid**||
|Order ID|The unique transaction ID generated for the order by the touchpoint.|
|First name|The first name of the customer who performed the transaction.|
|Last name|The surname of the customer who performed the transaction.|
|Creation date|The date the order was created.|
|Time|The time the order was created.|
|Creation Channel|The touchpoint on which the order was created.|
|Status|Current status of the customer order. The options are:<BR><BR>* **Suspended** – The transaction is suspended, for example, if the battery on the device dies, or the transaction is saved at the POS terminal.<BR>* **Totaled** – The transaction was completed on the touchpoint, but not paid for, e.g. on the self-scan when the end of trip barcode is scanned.<BR>* **Voided** – The transaction was voided.<BR>* **Finished** – The transaction was paid and transferred to a retail transaction.|
|Transaction total|The current total amount of the specific customer order.|