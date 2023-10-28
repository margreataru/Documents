**AWS CLI installation:**
1)	you must uninstall the pre-installed yum version using the following command: <br />
sudo apt remove awscli -y
2)	Install or update the AWS CLI (Ubuntu) <br />
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" <br />
unzip awscliv2.zip <br />
sudo ./aws/install<br />
3)	Check aws cli installed or not. <br />
aws –version<br />

**EKSCTL installation:**
1)	Set Up the environment variables. <br />
ARCH=amd64 <br />
PLATFORM=$(uname -s)_$ARCH <br />
2)	Install tar file. <br />
curl -sLO https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz <br />
3)	Extract the file using tar and delete the tar file. <br />
tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp && rm eksctl_$PLATFORM.tar.gz <br />
4)	Move the eksctl to bin directory. <br />
sudo mv /tmp/eksctl /usr/local/bin
 
**Install kubectl on ubuntu:**

1)	Download Binary file. <br />
curl -LO https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl <br />
2)	Install the kubectl and set file permission. <br />
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl <br />
3) Check the kubectl version. <br />
kubectl version –client <br />


**Helm installation:** <br />
1)	Install binaries. <br />
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 <br />
3)	Set file permisstion. <br />
chmod 700 get_helm.sh <br />
4)	Install Helm in linux. <br />
  	./get_helm.sh
