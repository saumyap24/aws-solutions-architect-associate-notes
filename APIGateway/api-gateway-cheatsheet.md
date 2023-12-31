- Enables developers to create, publish, maintain, monitor, and secure APIs at any scale
- HIPAA eligible service
- Allows creating, deploying and managing a RESTful API to expose backend HTTP endpoints, Lambda functions or other AWS services
- Concepts 
    - API deployment 
        - a point-in-time snapshot of your API Gateway API resource and methods. To be available for clients to use, the deployment must be associated with one or more API stages
    - API endpoints 
        - host names APIs in API Gateway, which are deployed to a specific region and of the format: rest-api-id.execute-api.region.amazonaws.com
    - Usage Plan 
        - Provides selected API clients with access to one or more deployed APISs. You can use a usage plan to configure throttling and quota limits, which are enforced on individual client API keys 
- Features:
    - Amazon API Gateway provides <b> <ins> throttling at multiple levels including global and by a service call.</ins></b> Throttling limits can be set for standard rates and bursts.
        -  For example, API owners can set a rate limit of 1,000 requests per second for a specific method in their REST APIs, and also configure Amazon API Gateway to handle a burst of 2,000 requests per second for a few seconds.