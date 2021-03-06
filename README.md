# Generating CloudWatch metrics for ECS Clusters

Currently tagging is not supported for ECS services, a work around is to generate regular Cloudwatch metrics using a scheduled Lambda.

## Installing library dependencies

### Install Homebrew and Node.js

The project uses Node.js which you can install using Homebrew using [these instructions](https://www.dyclassroom.com/howto-mac/how-to-install-nodejs-and-npm-on-mac-using-homebrew). 

### Install Serverless

It uses the [Serverless Framework](https://serverless.com/) for deployment you will need to [install it](https://serverless.com/framework/docs/providers/aws/guide/installation/):

	npm install -g serverless

## Create a named AWS profile locally

If you are deploying from an EC2 instance you can skip this step and remove the profile reference from the serverless.yml file.

Otherwise create a named user in your AWS account and generate an access key and secret key and create a named AWS credential profile using:

	aws configure --profile ecs-monotoring
	
## Deploy to AWS

Deploy to your AWS account using:

	serverless deploy
	
## Inspect the metrics in CloudWatch

	...

### Authors

**Josh Passenger** AWS Solutions Architect - [jospas@amazon.com](mailto:jospas@amazon.com)

### License

This project is licensed under the Apache 2 License - see the [LICENSE.txt](LICENSE.txt) file for details

### Warranty

No warranty is provided or implied with this software, 
it is provided as a Proof of Concept (POC) example and will require additional error checking code and testing.	