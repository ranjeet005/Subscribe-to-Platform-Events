# Subscribe-to-Platform-Events
Subscribe to a Platform Event in an Apex Trigger
Your Salesforce app uses a trigger to listen to events. Once your app receives the notification from the order system through the trigger, it creates a task to follow up on the order shipment.
Create an Apex trigger named OrderEventTrigger for Order_Event__e. This trigger will be similar to the CloudNewsTrigger trigger, but operates on the Order_Event__e event and creates tasks instead of cases.
If the order has shipped (event.Has_Shipped__c == true), create a task with the following values:
Priority: 'Medium'
Subject: 'Follow up on shipped order ' + event.Order_Number__c
OwnerId: event.CreatedById
