- [CloudFront](#cloudfront)
- [CloudFront Core Components](#cloudfront-core-components)
- [CloudFront Distributions](#cloudfront-distributions)
---
## CloudFront
---

- Content Distribution Network (CDN) creates cached copies of your website at various Edge locations around the world
- Content Delivery Network (CDN) 
    - A CDN is a distributed network of servers which delivers web pages and conetent to users based on their geographical location, the origin of the webpage and a content delivery server 
        - Can be used to deliver an entire website including static, dynamic and streaming
        - Requests for content are served from the nearest Edge Location for the best possible performance

        <img src="../images/CloudFront/CDN.jpg" width="77%" height="40%"/>

---
## CloudFront Core Components
---
- <b> Origin </b> 
    - The location where all of original files are located. For example an S3 Bucket, EC2 Instance, ELB or Route53
- <b> Edge Location </B> 
    - The location where web content will be cached. This is different than an AWS Region or AZ
- <b> Distribution </b>
    - A collection of Edge locations which defines how cached content should behave

    <img src="../images/CloudFront/cloudfront-core-components.jpg" width="77%" height="40%"/>

---
## CloudFront Distributions
---
