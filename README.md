# JIB ECR Example

### [Jib](https://github.com/GoogleContainerTools/jib)

Tool for building optimized Docker and OCI images for your Java applications without a Docker daemon

### [ECR](https://aws.amazon.com/ru/ecr/)

AWS fully-managed Docker container registry

### Requirements

1. You have the AWS CLI installed and configured. 
2. Your user has the required IAM permissions to access the Amazon ECR service. 

For more information, see [Docker Basics for Amazon ECR](https://docs.aws.amazon.com/AmazonECR/latest/userguide/docker-basics.html#use-ecr) page.

### How to run

1. Open `build.gradle` file and change `jib.to.image` to your ecr registry address.
2. Run `./gradlew clean build jib` in root directory.

And thats it! After gradle build will finished successufully you should be able to see builded image in ecr registry.