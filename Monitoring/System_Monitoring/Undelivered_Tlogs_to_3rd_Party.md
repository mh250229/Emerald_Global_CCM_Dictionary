### Undelivered Tlogs to 3rd Party

**Undelivered Tlogs to 3rd Party** is used to view transactions that were not delivered to a third party when the Rabbit was offline.

If the Rabbit is offline, transactions are added to the Retail database. When the connection to the Rabbit is restored, the system collects the transactions from the Retail database. New transactions continue to be added to the Retail database until the Retail database queue is empty, after which the transactions are sent directly to the RabbitMQ queues.

**Reference Path:** *Monitoring/System Monitoring/Undelivered Tlogs to 3rd Party*

![Undelivered Tlogs to 3rd Party Screen](/Images/UndeliveredTlogsto3rdPartyScreen.png)

View the fields as follows:

|**Field**|**Description**|
|---------|----------|
|Entity Types|The transaction that failed to be sent according to the transaction type, e.g., Retail transaction, Control transaction, Fund transaction.|
|From|The date and time from which the transactions were not sent to the server.|
|To|The date and time up to the transactions that were not sent to the server.|
|**Undelivered Tlogs to 3rd Party**||
|Token ID|The ID of the Token which includes the transactions that meet the selected filter criteria. A Token is the equivalent to a content of unit of work. may include more than one entity type.|
|Creation Date|The date and time of the first failure.|
|Entity Types|The type of transactions included in the Token, e.g., Retail transaction, Control transaction, Fund transaction. If there is more than one entity type in the token, each type is displayed with a separator.|
|Reason|The reason the token was not sent. The reason is received from the server.|