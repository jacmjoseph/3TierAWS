This project would create a completely serverless 3-tier implementation stack in AWS with cloudformation template 'Project1.template'. This template would create an API gateway, its resources and methods, set CORS headers, then create nodejs based lambda as the business tier which would then interact with a dynamoDB table that is also created.

The template expects 2 parameters. These parameters are the S3 bucket name and the path/key for the zip file where the source code of the lambda must be uploaded. In this case, index.js file should be zipped up and uploaded into an S3 bucket and use the relevant details as parameters.

The front-end is a simple HTML file (index.html) that can be used to insert a key and a value to the dynamoDB. It also has a retrieve feature where you can provide an inserted key to retrieve its value.
Please note that the API gateway has request templates for JSON transformation from the front-end to a format that can be directly used by the lambda.

The output of the stack includes the URL to the API Gateway created, in addition to some other data. The only change needed to index.html file is to update the POST URLs used by the fetch API for insert and retreive (2 places).

This implementation is edge optimized.




