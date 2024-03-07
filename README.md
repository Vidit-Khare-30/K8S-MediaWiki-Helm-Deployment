# K8S-MediaWiki-Helm-Deployment

The helm chart is used to  deploy MediaWiki application along with its dependencies.

It contains deployment, service, configmap and hpa objects.

##  Steps for Deployment

To install the chart on aks please run the following commands in azure cloudshell

1. az aks get-credentials -g  'AKS Resource Group Name' -n  'AKS cluster name'

2. helm install MediaWikiApp ./MediWikiApp

3. You can check pods and service by running below commands
kubect get pods
kubectl get svc

4. Get the public ip of your loadbalancer and do  the setup of Mediawiki using steps specified.

5. Get the  localsettings.php content and and update the configmap object file with  generated values.

6. Upgrade the app using

   helm upgrade MediaWikiApp ./MediWikiApp
