# Deploy a simple application using Helm

You need to have a Kubernetes cluster with ingress controller to deploy the application

1). Add custom helm repository specifying the <repo_name>
	
	helm repo add juiceshop-new https://dulanjanad.github.io/OWASPJuiceShop-helm-chart

2). Verify if repository added successfully

    helm repo list

3). Update helm repos

	helm repo update
 
4). Install the application

	helm install helm install new-deploy juiceshop-new/owaspjuiceshop
	(Make sure to provide above created repo name correctly)

5). Verify the deployment.
	
    kubectl get ingress -n development

## Destroy Resources

1). Delete the deployment with helm
	
    helm delete new-deploy (Make sure to put the given deployment name)

2). Destroy AWS resources 
    
    terraform destroy
#
