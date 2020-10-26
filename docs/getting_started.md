# Getting started

## Setting up the Frontend

The following steps can be used to deploy the frontend:

1. Clone the aws-serverless-feedback-app project

- **`git clone https://github.com/aws-samples/aws-serverless-feedback-app.git`**

2. Navigate to the CDK Application to that will be used to create the following infrastructure: CodeCommit Repository (used as source repo) and AWS Amplify Application (used for hosting the frontend)

- **`cd aws-serverless-feedback-app/feedback-app-frontend/amplify-infra-code/`**

3. Install the packages required by the CDK Application

- **`npm install/`** (ignore any the warnings)

4. Build the CDK Application

- **`npm run build/`**

5. Deploy the CDK Application

- **`cdk deploy --require-approval never/`**

(Note: ensure there are no duplicates in the resource names otherwise change the names in the file /feedback-app-frontend/amplify-infra-code/global/constant.json )

6. Navigate back to the feedback-app-frontend folder

- **`cd /home/ec2-user/environment/aws-serverless-feedback-app/feedback-app-frontend//`**

7. Run the following git commands to commit code to the CodeCommit repository created in 5 above

- **`git init/`**
- **`git add ./`**
- **`git commit -m "first commit"/`**
- **`git remote add codecommit codecommit::eu-west-1://feedback-app-repo-frontend/`**
- **`git push -u codecommit master/`**