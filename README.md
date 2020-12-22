# Kinesis data stream Consumer as a SpringBoot application

This is a simple Kinesis data stream custom consumer using KCL library. Amazon Kinesis Data Streams is a massively scalable and durable real-time data streaming service. KDS can continuously capture gigabytes of data per second from hundreds of thousands of sources such as website clickstreams, database event streams, financial transactions, social media feeds, IT logs, and location-tracking events. 

This consumer will consume the data from Kinesis data stream process the data according to the processing logic given by the developer.

## Prerequisites

- AWS credentials provided in environment variable.
- Create a data stream name "test", or you can name it something else and change the stream name in application.
- Data streamed in KDS through a producer or other AWS services so that consumer have something to consume.

# How does the consumer work?

The application once connected to your AWS account will start streaming the data as soon as  the application starts. The **streamName** and region are hard coded in the application. You can change it according to you.

The **processRecords** method in the **SampleRecordProcessor** class is where the heart of the consumer lies. The logic for what to do with the incoming data lies here. Right now the application is doing just logging dummy data, But you can write your own logic and perform operation on the data. This application will consume data but not process it. 
You can write the process logic according to your needs.

## To remember

- Delete your kinesis data stream after testing.
- Application creates DynamoDb instance internally for maintaining lease record. Charges will apply for that.

 
