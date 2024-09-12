Testing the security of RDS DB instance in AWS cloud by accessing it both, publicly and privatey. First by accesing it publicly 
through triggering a lambda function to access the database "after editing its security group inbound rules". Then trying accessing it 
when the RDS instance is in a private VPC which for sure won't work as the lambda function is notin the same VPC as the instance,
so I had to create a new lambda function inside the same VPC as the RDS instance to be able to connect to it and make queires on it 
as this is the only way to connect to an RDS inside a private VPC.
