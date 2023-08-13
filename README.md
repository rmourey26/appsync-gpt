#Convert any NextJS web app to a full stack AWS CloudFormation including:

- Amazon Cognito: This will provide both user sign in with user pools, as well as setting service authorization via identity pools
- AWS AppSync: Our managed GraphQL API that offers real-time support via WebSockets
- Amazon DynamoDB: NoSQL database for persisting data
- Amazon CloudFront: Asset caching for the files stored in our S3 bucket
- Amazon Simple Storage Service (S3): File storage. Public images are delivered via CloudFront while protected content is served with a pre-signed URL.


To run this automation, you'll need:

- github token which can be created using the link below
https://github.com/settings/tokens/new

- AWS Access Key-ID and Secret Key stored in your AWS config file on your local machine 

Once you create the github token, store it in AWS Secrets manager using the plain text method rather
than the key/value method. In this case, you'll want to use 'github-token' but you of course may modify the 
naming conventions as you see fit provided you're modifying the code as well

Within the ./bin/cdk-appsync-images.ts file, enter the name
of the repo associated with your NextJS app. 

After installing the dependencies using npm or yarn, deploy 
your full stack cloudformation by running

#todo add backticks 

npx aws-cdk deploy --all

#todo add backticks 


Credit: Inspired by an article written by Michael Liendo 



