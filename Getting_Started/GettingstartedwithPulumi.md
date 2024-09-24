### Getting started with Pulumi

Pulumi is a modern [**infrastructure as code**](https://www.pulumi.com/what-is/what-is-infrastructure-as-code/) and [**secrets management**](https://www.pulumi.com/what-is/what-is-secrets-management/) platform that allows you to use familiar programming languages and tools to automate, secure and manage everything you run in the cloud.

Pulumi IaC is free, open source, and optionally pairs with the Pulumi Cloud to make managing infrastructure secure, reliable, and hassle-free.

(Helps you create, deploy, and manage AWS containers, serverless functions, and infrastructure.)

**Note:Can work with multiple languages e.i. golang, python, typescript, etc..**

#### Supported infrastructure:
-    AWS
-    Azure
-    Google Cloud
-    Kubernetes

#### Install Pulumi on Linux
```curl -fsSL https://get.pulumi.com | sh``` 

### When the installation completes, you can test it out by reading the current version:
```pulumi version```

If this doesn't work, you may need to restart your terminal to ensure the folder containing the `pulumi` command is on your `PATH`.

Other installation options are available [**here**](https://www.pulumi.com/docs/install/).

### Install Language Runtime

Debian/Ubuntu you must run `sudo apt install python3-venv python3-pip`


### For a quick example of how Pulumi deploys infrastructure on AWS, this tutorial takes you through the following steps to easily deploy a static website:
-    Setting up and configuring Pulumi to access your AWS account.
-    Creating a new Pulumi project.
-    Provisioning a new AWS S3 bucket.
-    Adding an index.html file to the bucket and serving it as a static website.
-    Cleaning up your deployment by destroying the resources you've provisioned.

### Configure Pulumi to access your AWS account

If you have previously [installed](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html) and [configured](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html) the AWS CLI, Pulumi will respect and use your configuration settings.

If you don’t have the AWS CLI installed, or you plan on using Pulumi in a CI/CD pipeline, [retrieve your access key ID and secret access key](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html#access-keys-and-secret-access-keys) and then set the `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` environment variables on your workstation:

### Configure AWS_ACCESS_KEY and AWS_SECRET_ACCESS_KEY in linux system(Ubuntu/Debian)
```
export AWS_ACCESS_KEY_ID="<YOUR_ACCESS_KEY_ID>" 
export AWS_SECRET_ACCESS_KEY="<YOUR_SECRET_ACCESS_KEY>"
```
**Pulumi also support AWS profiles:**
```
export AWS_PROFILE="<YOUR_PROFILE_NAME>"
```
#### For additional information on setting and using AWS credentials, see [AWS Setup](https://www.pulumi.com/registry/packages/aws/installation-configuration/).

### Pulumi & AWS: Create new project

#### Step 1: Create your first Pulumi program.
`pulumi new aws-python`

**The `pulumi new` command creates a new Pulumi project with some basic scaffolding based on the cloud and language specified.**

#### Step 2: Next, you will be asked for a stack name. Hit ENTER to accept the default value of dev.

#### Step 3: Finally, you will be prompted for some configuration values for the stack.

#### Step 3: You can accept the default value or choose another value like `ap-south-1`.

#### After the command completes, the project and stack will be ready.

### Pulumi & AWS: Deploy stack
#### To deploy use simple command: `pulumi up`
### Pulumi & AWS: Destroy stack
#### To destroy resources: `pulumi destroy`

**Congratulations! You’ve successfully provisioned some cloud resources using Pulumi.**
**(For more details. Visit [**here**](https://www.pulumi.com/docs/iac/get-started/aws/deploy-stack/)!!)**