### Student Performance Data

### Docker Setup In EC2 commands to be Executed

`sudo apt-get update -y`   
`sudo apt-get upgrade`          
`curl -fsSL https://get.docker.com -o get-docker.sh`            
`sudo sh get-docker.sh`           
`sudo usermod -aG docker ubuntu`           
`newgrp docker`            

### Configure EC2 as self-hosted runner
Using Linux, Create a new self-hosted runner

```
mkdir actions-runner && cd actions-runner   

curl -o actions-runner-linux-x64-2.317.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.317.0/actions-runner-linux-x64-2.317.0.tar.gz

echo "9e883d210df8c6028aff475475a457d380353f9d01877d51cc01a17b2a91161d  actions-runner-linux-x64-2.317.0.tar.gz" | shasum -a 256 -c

tar xzf ./actions-runner-linux-x64-2.317.0.tar.gz

./config.sh --url https://github.com/imsalik/mlproject --token ALNVJWPIRPB6GYTQY3XPMMDGSOOEG

./run.sh

runs-on: self-hosted
```
### Setup github secrets:

AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = 

AWS_ECR_LOGIN_URI = 

ECR_REPOSITORY_NAME = 
