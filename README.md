## VoteTheGame

It is a voting application which is based on microservices as architecture.

![voteapp-vote](https://user-images.githubusercontent.com/37767537/232127010-f1bc4b69-7c55-46bd-9c5b-4a4f99d8ca68.png)

### About this app

The working of microservices are as follows

- The main application (vote) is based on flask connected to a Redis database
- The Redis database is connected to a worker service for processing the vote
- The worker service is connected to a Postgresql database for storing the vote result
- The vote results are being showcased using the result service

