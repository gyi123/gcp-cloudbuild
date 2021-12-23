# gcp-cloudbuild:
Assume you know how to create GCP projects and Enable Billing, CloudBuild, Kubernetes, IAM
1. Create cluster: gcloud container clusters create gyi-cluster --zone us-central1-c
2. Grant access: gcloud projects add-iam-policy-binding qk-docker --member=serviceAccount:269642988761-compute@developer.gserviceaccount.com --role=roles/container.developer
3. Configure trigger for push update. (follow the direction to setup up github permission)
4. Make a code change and push to github
5. Go to Kubernetes Engine dashboard, click Service and Ingress.
6. Choose hellospring-service.
7. Expose Service with Port: 80, Node Port:	#####, Target Port	8080, Protocol:	TCP
8. Back to hellospring-service. 
9. Click the link under EndPoints. (this should be the loadbalancer ip and port)
10. You should see the "Greetings from Spring Boot!"
