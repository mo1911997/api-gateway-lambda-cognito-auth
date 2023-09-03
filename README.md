# api-gateway-lambda-cognito-auth
This simple application demonstrates the use of cognito as an authentication mechanism with api gateway and lambda
For this application to work , first login to AWS management console and follow along 

# Lambda Function Configuration
1. Go To Lambda Console. Under Basic Information , provide function name.
2. Select Nodejs (18.04) as a Runtime.
3. Select execution role (Create new if not present )
4. Keep rest of the settings as it is .
5. Click on "Create Function".
6. We are done with the lambda setup.

# Cognito Setup Configuration
1. Go to Cognito service.
2. Click on "Create User Pool".
3. Tick Username and Email under "Cognito user pool sign-in options" and click Next
4. Under Multi Factor Authentication , select "No MFA" keep rest of the settings unchanged. 
5. Configure Sign-Up option will come up.Keep all the settings as it is . You may select any extra attributes for the user while signing up .
6. Under "Configure Message Delivery", select "Send Email with Cognito" and click on Next .
7. Add User Pool Name
8. Check "Use the Cognito Hosted UI".
9. Select/add any domain
10. Provider App Client Name.
11. 

# API Gateway Configuration
1. Go to API Gateway . Select Rest API (without VPC) and click on "Build".
2. Choose Protocol as Rest. Under "Create New API",select New API.
3. Under settings, provide name,description and endpoint type
4. Now click on "Actions" and select "Create Resource".Provide any resource name of your choice then click on "Create Resource" button.I will use "/users" as a reference. 
5. Now select your resource "/users".Then click on Actions and choose "Create Method".Select "GET" and click on the checkmark next to it.
6. Select "Lambda Function" as an integration type
7. Type the above defined function name inside Lambda Function textfield and click on "Save".
8. It will ask you to add permission to invode lambda function .Click on "OK".
9. 
