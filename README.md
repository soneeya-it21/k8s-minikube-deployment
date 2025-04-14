🚀 Kubernetes Minikube Deployment - Build a Kubernetes Cluster Locally with Minikube

This project demonstrates how to build a Kubernetes cluster locally using **Minikube** and deploy a simple **NGINX application**.

🛠 Tools Used

- Minikube
- kubectl
- Docker
- EC2 Ubuntu Instance

📦 What’s Inside

- `deployment.yaml` - Kubernetes Deployment configuration for the NGINX app  
- `service.yaml` - NodePort Service to expose the app  
- Sample commands to interact with the cluster

⚙️ Steps to Run

1. Install Prerequisites

- Docker
- Minikube
- kubectl
- cri-dockerd (for none driver)
- container networking plugins

2. Start Minikube
minikube start --driver=none
Make sure Docker and required plugins are set up properly.

3. Apply Deployment
kubectl apply -f deployment.yaml

5. Expose the Deployment via NodePort
kubectl apply -f service.yaml

7. Verify Resources
kubectl get pods
kubectl get svc

9. Scale the App
kubectl scale deployment nginx-deployment --replicas=3

11. Check Logs
kubectl logs <pod-name>

✅ Output Sample
kubectl get pods
NAME                              READY   STATUS    RESTARTS   AGE
nginx-deployment-96b9d695-abcde   1/1     Running   0          2m
...
kubectl get svc
NAME            TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)        AGE
nginx-service   NodePort    10.106.138.253   <none>        80:30094/TCP   2m
Visit your app: http://<your-EC2-public-IP>:30094

📸 Screenshots
![Nginx deployment](https://github.com/user-attachments/assets/9d14b5b3-a952-4903-b8a2-8a314dcaa8cc)
![Pods running](https://github.com/user-attachments/assets/3a241820-154e-4131-b097-ba2d6367735d)
![kubectl get svc ](https://github.com/user-attachments/assets/764e362b-27a2-4bb6-a792-5898a2f04216)
![log of pod-nginx-deployment-96b9d695-dx5k2](https://github.com/user-attachments/assets/5448071a-d256-4530-9ca8-bcc4230f130a)
![pod log](https://github.com/user-attachments/assets/6cc9cfa7-1589-4fca-bed5-dc62fc598144)

🙌 Author
GitHub: @soneeya-it21
