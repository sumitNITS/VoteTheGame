## VoteTheGame

![Cricket-vs-Soccer](https://user-images.githubusercontent.com/37767537/232277919-bd2644f9-422e-4be6-8ffc-c92155e33c95.jpg)

It is a voting application which is based on microservices as architecture.

![voteapp-vote](https://user-images.githubusercontent.com/37767537/232232535-f0495bca-4dde-4720-b1ae-345142040bbe.png)

### About this app

The working of microservices are as follows

- The main application (Vote) is based on Flask connected to a Redis database
- The Redis database is connected to a Worker service for processing the vote
- The Worker service is connected to a Postgresql database for storing the vote result
- The vote results are being showcased using the result app

![voteapp-result](https://user-images.githubusercontent.com/37767537/232237663-4927df8b-0ae6-4ee4-bb47-5ffe25a0ea31.png)

### Instructions to run this project using Docker Compose

- [Clone this repository](https://github.com/sumitNITS/VoteTheGame.git)
- cd to VoteTheGame
- Run the docker-compose file using the command 
```bash
docker-compose up -d
```

![application containers](https://user-images.githubusercontent.com/37767537/232276493-0e85b9d1-7a05-4399-9380-19d578f09cea.png)

Now access the Vote application using "localhost":5000 or "ip-of-machine":5000 🚀 </br>
And access the Result application using "localhost":5001 or "ip-of-machine":5001 🚀

OR

```bash
docker-compose -f dockerhub-image-compose.yml up -d
```

![application containers-1](https://user-images.githubusercontent.com/37767537/232276185-f725968d-705e-4b31-9dff-40e2f79d33d6.png)

Now access the Vote application using "localhost":5000 or "ip-of-machine":5000 🚀 </br>
And access the Result application using "localhost":5001 or "ip-of-machine":5001 🚀

![voteapp-result-1](https://user-images.githubusercontent.com/37767537/232276221-a5f77451-60c3-4e9f-8451-8a5cced43b24.png)

### Instructions to run this project in local Kubernetes minikube 

- [Clone this repository](https://github.com/sumitNITS/VoteTheGame.git)
- Start minikube 
- cd to VoteTheGame
- Run the below commands
```bash
kubectl apply -f kubernetes/
```
```bash
kubectl port-forward service/voteapp 5000
```
```bash
kubectl port-forward service/resultapp 5001
```

![kubernetes-status](https://user-images.githubusercontent.com/37767537/232277287-f2e29b5d-5f16-4fde-ae8c-08e6cb4fe174.png)


Now access the Vote application using "localhost":5000 or "ip-of-machine":5000 🚀 </br>
And access the Result application using "localhost":5001 or "ip-of-machine":5001 🚀