Create a system that monitors an S3 bucket for new file uploads, by triggering a Lambda function to process the uploaded files, then sending a notification using SNS, and finally stores metadata in an SQS queue.
This project includes S3 event triggering, a simple lambda function to process the uploaded files, using SNS and SQS, and finally integrating S3 service with all these previous services.
