- CloudFront is a CDN (Content Distribution Network). It makes website load fast by serving cached content that is nearby
- CloudFront distributes cached copy at <ins> Edge Locations </ins>
- Edge Locations aren't just not read-only , you can write them eg. PUT objects 
- TTL (Time to live) defines how long until the cache expires (refreshes cache)
- When you invalidate your cache, you are forcing it to immediately expire (refreshes cached data)
- Refreshing the cache costs money because of transfer costs to update Edge locations 
- Origin is the address of where the original copies of your files reside eg. S3, EC2, ELB, Route53
- <b> Distribution </b> defines a collection of Edge Locations and behavior on how it should handle your cached content 
- Distributions has 2 Types : 
    - Web Distribution (statis website content) 
    - RTMP (steaming media)
- Origin Identity Access (OAI) is used access private S3 buckets 
- Access to <b> cached content can be protected</b> via <ins> Signed URLs or Signed Cookies </ins>
- Lambda@Edge allows you to pass each request through a Lambda to change the behavior of the response
