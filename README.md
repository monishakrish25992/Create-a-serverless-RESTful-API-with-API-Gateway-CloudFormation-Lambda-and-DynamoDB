
Create a serverless RESTful API with API Gateway, Swagger, Lambda, and DynamoDB
        
   This article teaches you how to create a serverless RESTful API on AWS. You will use OpenAPI Specification formerly known as Swagger Specification to define the API and API Gateway in combination with Lambda to implement the API. DynamoDB is used to store the data.
        
Implementing a RESTful API with API Gateway, Lambda, and DynamoDB

   API Gateway provides an HTTP API endpoint that is fully configurable. You define the HTTP resources (like /user), the HTTP methods on that resources (like POST, GET, DELETE, …) and the integration (e.g. Lambda function) that should be called to process the request. The Lambda function can then run whatever logic is needed to answer the request. The result of the Lambda function is returned by the API Gateway to the caller. The following figure demonstrates this flow.

If you want to define a REST API you need to specify:

                Resources (e.g. GET //subject/{Subject}/avg)
                          ( POST /Subject)
                Methods on each resource (e.g. GET and POST)
                Input
                        Body Model
                        Headers
                        Path parameters (e.g. GET //subject/{Subject}/avg)
                Mapping HTTP input to integration input
                Integrations (e.g. Lambda functions)
                Mapping integration output to HTTP output
                Output
                        Body Model
                        Headers
                        
You can use a popular framework called Swagger to define a REST API. You will learn how to use Swagger next.

Defining a RESTful API with Swagger
        Swagger defines a way to describe your RESTful API in a format like JSON. The cool thing about Swagger is that the API definition can be used by:

  the server that implements the API
  the clients that use the API
Swagger offers a large ecosystem offering powerful tools: you are able to generate client SDKs, visually edit your Swagger definition and use many other helpful tools. 
