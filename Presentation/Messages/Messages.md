## Messages

**Messages** is used to view the messages displayed at the POS terminal, e.g., a message prompted when a business event is triggered.

New messages are created in the specific module in which they are used. For example, messages displayed when a business rule is triggered are created in the Business Rule module. Messages are created for Business Rules, EPS, Central Returns, Self Scan, Reason Codes, Alerts and Voucher flows. Messages created in a specific module are used only in that module. For example, a message created for Business Rules in the Business Rules module, is available only for business rules, and cannot be selected in other modules. When viewing the messages in this screen, the module the message is relevant to is displayed.

The message text and the actions, which are required by the end-user can vary based on the actual POS client in which the event is triggered, and the physical device which is used.

For example, the store prevents the sale of alcohol to underage customers. A message is set up to prompt the cashier to request customer ID when alcoholic items are scanned.

A message can include text, and fields. Fields are populated by the system during transactions, such as POS ID, Transaction Number, etc.

Data Entry fields can be defined which are populated by the user during the transaction – such as: Customer Age, POS ID, Number of Traveling Days, etc. or by the application itself following the context. The message layout is automatically formatted by the system.

In addition, messages can be linked to different cultures, and displayed in the language linked to the specific culture.

**Reference Path:** *Presentation/Messages/Messages*
