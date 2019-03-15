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
2. If your registry is not in us-east-2 region change region in `jib.to.auth.password` field.
3. If you have more than one profiles in the `~/.aws/credentials` file you should specify which one you want to use by adding to `jib.to.auth.password` field `--profile` parameter. 
4. Run `./gradlew clean build jib` in root directory.

#### And thats it! 

After gradle build will be finished successfully you should be able to see builded image in ecr registry.