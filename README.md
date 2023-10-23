# 3.5-assignment

**Step-by-step on how to create an image until it is deployed to AWS**

1) Set up your AWS Elastic Container Registry Repository (sharir-ecr-repo)

2) Authenticate docker client to registry -> aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 255945442255.dkr.ecr.us-east-1.amazonaws.com
  
3) Start terraform and cd into a folder with a dockerfile

4) Build the docker image -> docker build -t sharir .

5) Tag the image -> docker tag sharir:latest 255945442255.dkr.ecr.us-east-1.amazonaws.com/sharir-ecr-repo:latest

6) Push the image to aws -> docker push 255945442255.dkr.ecr.us-east-1.amazonaws.com/sharir-ecr-repo:latest

Docker image is now within sharir-ecr-repo
