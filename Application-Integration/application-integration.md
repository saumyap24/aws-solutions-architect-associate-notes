- [Queueing (SQS) ](#queueing-sqs)
- [Streaming and Kinesis](#streaming-and-kinesis)
- [Pub-Sub and SNS](#pubsub-sns)
    - [What is Pub/Sub ?](#what-is-pub-sub)
---
## Queueing (SQS) 
---
- <b> What is Messaging System ?</b>
    - Used to provide asynchronous communication and decouple processes via messages / events from sender and receiver (producer and consumer)

- <b> What is Queuing System ?</b>
    - A queueing system is a <ins> messaging system that generally will <b> delete </b> messages once they are consumed </ins>.
    - Simple Communication
    - <ins> <i> Not Real-time </ins> </i>
    - Have to pull
    - Not reactive

- <b> Simple Queuing System (SQS) </b>
    - Fully managed <b><ins> queuing service that enables you to decouple </ins> </b>and scale mircroservices, distributed systems, and serverless applications 
    - Use Case: You need to queue up transaction emails to be sent 
    - e.g. Signup, Reset Password

    <img src="../images/Application-Integration/SQS.jpg" width="45%" />

---
## Streaming and Kinesis
---
- <b> What is Streaming ? </b>
    - Multiple consumers can <b> react </b> to events (messages)
    - Events live in the stream for long periods of time, so complex operations can be applied 
    - <b><ins> Real-time </ins> </b>
    - <b> Amazon-Kinesis </b>
        - Amazon Kinesis is the AWS fully managed solution for collecting, processing and <ins> analyzing streaming data in the cloud </ins>

        <img src="../images/Application-Integration/amazon-kinesis.jpg" width="65%" />

---
## Pub-Sub and SNS
---
-  ### <b> What is Pub / Sub ? </b>
    - Publish-subscribe pattern commonly <i> <ins> implemented in <b> messaging systems. </b> </ins></i>
    - In a pub/sub system the sender of messages <ins> <b> (publishers)</b> do not send their messages directly to receivers.</ins>
    -  They instead send their messages to an <ins> <b> event bus </b> </ins>. The <ins> event bus categorizes their messages into groups</ins>.
    - The receivers of messages <ins> <b> Subscribers </ins></b> subscribe to these groups
    - Whenever new messages appear within their subscription the messages are immediately delivered to them

        <img src="../images/Application-Integration/pub-sub.jpg" width="35%" />

    - Publisher have no knowledge of who their subscribers are
    - Subscribers do not pull for messages
    - Messages are instead <ins> automatically and immediately pushed to subscribers</ins>
    - Messages and events are interchangeable terms in pub/sub 
    - Use case:
        - A real-time chat system
        - A web-hook system
- ### <b> Simple Notification Service </b>
    - It is a highly available, durable, secure,  <ins> <b> fully managed pub/sub messaging service </b> </ins> that enables you to  <i> <ins> decouple</ins> microservices, distributed systems and serverless applications </i>

    <img src="../images/Application-Integration/sns.jpg" width="55%" />



