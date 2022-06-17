# eng110-helm

To use this helm repository, make sure you first have helm installed with these commands:

> 1. Download helm with `curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3`.
> 2. Make the file executable with `chmod 700 get_helm.sh`.
> 3. Run the script with `./get_helm.sh`.

Once helm is installed, you can add this repository with the command `helm repo add custom-name-here https://samuel-walters.github.io/eng110-helm/`. To install the cluster, you should then run the command `helm install custom-name-here custom-name-here/eng110-nodeapp`. 