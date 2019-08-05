## Table of contents
* [GeneralInfo](#about this app)
* [Technologies](#node js)
* [Setup](#setup)

## General info
# ./infrastructure cloudformation templates used to scaffold AWS infrastructure

## To generate new stack

```bash
aws cloudformation create-stack --stack-name UNIQUE_STACK_NAME --template-body file://CLOUD_FORMATION_TEMPLATE.yaml --capabilities CAPABILITY_IAM
```
	
## Technologies
Project is created with:
AWS
AWS CloudFormation
AWS CodeCommit
AWS CodePipeline
AWS ElasticBeanstalk
Node JS
React JS
	
## Setup
To run this project, install it locally using npm:

```
$ cd ./musican-app
$ npm install or npm i
$ node app
```


## The NodeJS content was used from:

NodeJS / React sample app for AWS CI/CD pipeline tutorial

https://www.youtube.com/watch?v=NwzJCSPSPZs



## This application was built upont the AWS Tutorial:

https://docs.aws.amazon.com/codepipeline/latest/userguide/tutorials-cloudformation-codecommit.html


Example 1: Create an AWS CodeCommit Pipeline with AWS CloudFormation
This walkthrough shows you how to use the AWS CloudFormation console to create infrastructure that includes a pipeline connected to a CodeCommit source repository. In this tutorial, you use the provided sample template file to create your resource stack, which includes your artifact store, pipeline, and change-detection resources, such as your Amazon CloudWatch Events rule. After you create your resource stack in AWS CloudFormation, you can view your pipeline in the AWS CodePipeline console. The pipeline is a two-stage pipeline with a CodeCommit source stage and a CodeDeploy deployment stage.

Prerequisites:

You must have created the following resources to use with the AWS CloudFormation sample template:

You must have created a source repository. You can use the AWS CodeCommit repository you created in Tutorial: Create a Simple Pipeline (CodeCommit Repository).

You must have created a CodeDeploy application and deployment group. You can use the CodeDeploy resources you created in Tutorial: Create a Simple Pipeline (CodeCommit Repository).

Download the sample AWS CloudFormation template file for creating a pipeline. You can download the sample template in YAML or JSON format. Unzip the file and place it on your local computer.

Download the SampleApp_Linux.zip sample application file.

Unzip the files from SampleApp_Linux.zip and upload the files into to your AWS CodeCommit repository. You must upload the unzipped files to the root directory of your repository. You can follow the instructions in Step 2: Add Sample Code to Your CodeCommit Repository to push the files to your repository.

Open the AWS CloudFormation console and choose Create Stack.

In Choose a template, choose Upload a template to Amazon S3. Choose Browse and then select the template file from your local computer. Choose Next.

In Stack name, enter a name for your pipeline. Parameters specified by the sample template are displayed. Enter the following parameters:

In ApplicationName, enter the name of your CodeDeploy application.

In BetaFleet, enter the name of your CodeDeploy deployment group.

In BranchName, enter the repository branch you want to use.

In RepositoryName, enter the name of your CodeCommit source repository.


            Create a stack for your CodeCommit pipeline
          
Choose Next. Accept the defaults on the following page, and then choose Next.

In Capabilities, select I acknowledge that AWS CloudFormation might create IAM resources, and then choose Create.

After your stack creation is complete, view the event list to check for any errors.