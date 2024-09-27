We will be creating  a DynamoDB table full of employees and their status. when there's any change occurs in the table streams, a Lambda will be triggered that will send an email saying that “[employee status] has been changed!”

when changing an item in the table, dynamo db will update the stream of its table with the new item, and the trigger for that will be the lambda function, sp it will send these new records through the lambda function, then the lambda function will pass those records to SNS service which will send an e-mail with the new records and the updated status.

NOTE**: when we use scan operation on the dynamo db by using filters we're consuming 4 times the reading capacity units compared to using queries, that's why it's much better to create indexies use queries in dynamo db.

SNS: create topic for notifications which will be sent to us by the dynamo db trigger.

![Screenshot (407)](https://github.com/user-attachments/assets/6c669576-3554-483a-9d0d-46cb41b48928)
![Screenshot (406)](https://github.com/user-attachments/assets/e8f17644-ec57-48ae-aa35-0def0c1ab773)
![Screenshot (404)](https://github.com/user-attachments/assets/c7eb8da9-e1c8-4c1c-8f4a-7ef8be921698)
![Screenshot (403)](https://github.com/user-attachments/assets/cbdb2bd5-4331-4d1d-bca0-e3934085cb5d)
![Screenshot (402)](https://github.com/user-attachments/assets/65bf905a-6bda-4954-94fb-e1871e200c2a)
![Screenshot (401)](https://github.com/user-attachments/assets/77e5c948-e407-4a2c-92bc-692cb963d25a)
