# AWS-Cloud-Fun-Fact-Generator

#Part 1

-  Using AWS management console I first created a Lambda function and added Python code to it that included AWS fun facts
- Then I created a test event in Lambda to manually trigger the function to see if it would successfully return a JSON response, which it did
- After I created a API Gateway and selected HTTP to make it accessible for people over the internet to access the function
- API Gateway acts as a gateway/front door to trigger the Lambda function and it returns a fun fact
  
#Part 2

  - Created a DynamoDB table, and created facts in the table 
  - After that we had to find a way for the Lamdba and DynamoDB table to communicate so we than went to IAM roles
  - Then we attached a policy to Lambda to be able to read items from the DynamoDb table
  - Then we had to update the code for the Lambda function and deploy(save) it
  - Lastly we went back to API Gateway to get the invoke url and test to see if it worked and it did

    Summary: the whole point of this part was to be able to better scale and effectiently insert facts to dynamodb instead of having to change the code in the lambda function everytime you want to add a new fact

#Part 3

  -The last part was AI integration in your application but I did not complete the Amazon Bedrock integration because I wanted to avoid using a paid model before fully understanding the pricing and billing setup. However, I understand the intended architecture: Lambda would send the cloud fact to Bedrock, Bedrock would use a foundation model like Claude to rewrite the fact in a more engaging style, and Lambda would return the enhanced response through the API.
