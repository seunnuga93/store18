==Steps to deploy==

1. Create an ACR and AKS in Azure  - (This can be automated using AZ CLI commands in devops or ARM templates) 
2. Import Github codebase repo into Azure Repos
3. Create a Build pipleline to with 2 docker-compose tasks (Docker compose run and docker compose push to ACR you have cretaed in step 1)
4. Build your pipeline
5. Create a release pipeline to deploy docker containers into kubernetes using the deployment and service files in repo.
6. Access your app via kubernetes external IP
7. You can get the external IP by typing 'kubectl get services' in Azure cloud shell. 