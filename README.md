## VoteTheGame

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

- Clone this repository
- cd to VoteTheGame
- Run the docker-compose file using the command 
```bash
docker-compose up -d
```
Now access the Vote application using "localhost":5000 or "ip-of-machine":5000 🚀 </br>
And access the Result application using "localhost":5001 or "ip-of-machine":5001 🚀

OR

```bash
docker-compose -f dockerhub-image-compose.yml up -d
```
Now access the Vote application using "localhost":8000 or "ip-of-machine":8000 🚀 </br>
And access the Result application using "localhost":8001 or "ip-of-machine":8001 🚀

![voteapp-result-1](https://user-images.githubusercontent.com/37767537/232247328-2e4d05f5-6774-4b58-8b6c-010b6d6ee2dc.png)
