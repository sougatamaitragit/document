# Setup ekcsctl 

       curl --silent --location "https://github.com/weaveworks/eksctl/releases/download/latest_release/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
       mv /tmp/eksctl /usr/local/bin
       eksctl version
       
# Setup AWS CLI Configure
  apt  install awscli
  aws configure 
# Create Cluster 

eksctl create cluster --name prod --version 1.14 --nodegroup-name standard-workers --node-type t3.medium --nodes 3 --nodes-min 1 --nodes-max 4 --node-ami auto
# Setup kubectl
curl -o kubectl https://amazon-eks.s3-us-west-2.amazonaws.com/1.14.6/2019-08-22/bin/linux/amd64/kubectl



 
