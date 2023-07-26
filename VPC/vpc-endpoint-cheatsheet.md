- VPC Endpoints help keep traffic between AWS services within the AWS Network
- There are two types of VPC Endpoints
    - Interface Endpoints
    - Gateway Endpoints 

| Interface Endpoints | Gateway Endpoints |
| --------------------| ------------------|
| <b> Cost money </b> | <b> free </b>|
|  Uses as <b> Elastic Network Interface (ENI) </b> with private IP (powered by AWS PrivateLink) | a target for a specific route in the route table |
| support many AWS services | only supports S3 and DynamoDB |
    