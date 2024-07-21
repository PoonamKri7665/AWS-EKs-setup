# AWS-EKs-setup
steps to create EKS on aws console
```
Login to the AWS console 
go to Eks service 
name the cluster and configure the setting of the cluster that will be the master node managed by AWS
```
Create a cluster role mentioned in AWS documentation 
go to the IAM console, create a role for the cluster amazonEKSclusterpolicy
```
select vpc configure network security groups according to the use case
```
# setup AWS CLI on your laptop
Install aws cli on your local computer (sudo apt install aws-cli) and for latest version use this command given below
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```
aws --version
bash: /usr/bin/aws: No such file or directory
poonam@vm:~$ hash aws
poonam@vm:~$ aws --version
aws-cli/2.17.14 Python/3.11.9 Linux/5.15.0-113-generic exe/x86_64.ubuntu.20

# configure aws cli 
aws configure (this access key and secret key of the same user who has created the cluster)
# now install kubectl to access kubernetes cluster
# setup kubectl 
```
aws eks update-kubeconfig --region ap-south-1 --name demo_eks
kubectl get svc (coomand to verify)
```
# to create worker node go to console cluster and click on compute resources
go to node group add
give IAM role to node group (use documentation)
Allow remote access to node 




