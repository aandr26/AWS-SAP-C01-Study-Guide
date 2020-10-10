# API Gateway

* [Return to table of contents](../../../README.md)

* **Useful Links:**
  * [Operating Your Serverless API](https://www.youtube.com/watch?v=tIfqpM3o55s)
  * [API gateway caching](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-caching.html)
  * [HTTP integrations](https://docs.aws.amazon.com/apigateway/latest/developerguide/getting-started-http-integrations.html)
  * [Proxy](https://docs.aws.amazon.com/apigateway/latest/developerguide/getting-started-aws-proxy.html)

* **Exam Tips:**
  * Used to create and manage APIs.
  * Endpoint/entry-point for applications.
  * Sits between applications and integrations (services).
  * Highly available, scalable, handles authorization, throttling, caching, CORS, transformations, OpenAPI spec, direct integration and much more.
  * Can connect to services/endpoints in AWS or on premises.
  * Remember you have the option between WebSocket APIs and REST.
  * API can have different stages/versions.
  * **Endpoint Types:**
    * Edge-optimized.
      * Routed to the nearest CloudFront POP.
    * Regional: Clients in the same region.
    * Private - Endpoint accessible only within a VPC via interface endpoint.
  * **Know this:**
    * **Errors:**
      * 4xx Client error - Invalid request on client side.
        * 400 Bad request - Generic
        * 403 Access denied - Authorizer denies
        * 429 API gateway can throttle - You've exceeded your that amount.
      * 5xx server error - Valid request, backend issue.
        * 502 Bad gateway exception - bad output returned by Lambda.
        * 503 Service unavailable - backing endpoint offline - could be major service issue.
        * 504 Integration failure/timeout - 29s limit.
    * **Caching:**
      * Defined per stage within API Gateway.
      * Reduced load and cost.
        * Improved performance.
      * Cache default TTL is 300 seconds.
        * Min 0 and max 3600s
        * Size 500MB to 237 GB
      * Can be encrypted.
      * Calls only made to backend integrations if request is a cache miss.
