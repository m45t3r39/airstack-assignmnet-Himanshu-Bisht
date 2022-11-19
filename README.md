# airstack-assignmnet-Himanshu-Bisht
 


# 1. Prerequisites
AWS CLI
Terraform CLI
Docker CLI
Eksctl
Kubectl


# 2. main.tf

This will allow Terraform to interact with AWS and it’s resources.

I suggest typing "terraform init" after each provider to make sure our resources are running properly.

# 3. vpc.tf

This will provision a vpc via the vpc module and it’s resources. Also added a resource of random_string to include in name.

Hit a "terraform init" to make sure everything is running properly.

# 4. eks.tf

Configure our EKS cluster via the EKS module, This will provision our resources to set up an EKS cluster including our worker groups.

# 5. output.tf

This will give the name of our cluster and expose the endpoint of our cluster.

Hit "terraform init" to make sure everything is working properly.

Hit "terraform validate" to make sure our code is valid.

# 6. Export Variables

You will need to add below variables here.

Add your AWS_ACCESS_KEY_ID.
Add your AWS_SECRET_ACCESS_KEY.
Add your AWS_DEFAULT_REGION. (default set to ap-sout-1)

# 7. terraform plan

# 8. terraform apply

aws eks --region ap-south-1 update-kubeconfig --name test-eks-cluster

I have used ALB Here in the project.

# 9. Installing the AWS Load Balancer Controller.

To deploy the AWS Load Balancer Controller to an Amazon EKS cluster
Follow the below document
https://docs.aws.amazon.com/eks/latest/userguide/aws-load-balancer-controller.html

Building and Pushing docker image to ECR

docker build -t ping-pong .

docker tag ping-pong:latest 016397833229.dkr.ecr.ap-south-1.amazonaws.com/ping-pong:latest

docker push 016397833229.dkr.ecr.ap-south-1.amazonaws.com/ping-pong:latest


http://k8s-pingpong-ingressp-f1c8b89bb3-1416347435.ap-south-1.elb.amazonaws.com/ping
