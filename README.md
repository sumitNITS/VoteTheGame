## VoteTheGame

It is a voting application which is based on microservices as architecture.

![voteapp-vote](https://user-images.githubusercontent.com/37767537/232232535-f0495bca-4dde-4720-b1ae-345142040bbe.png)

### About this app

The working of microservices are as follows

- The main application (Vote) is based on Flask connected to a Redis database
- The Redis database is connected to a Worker service for processing the vote
- The Worker service is connected to a Postgresql database for storing the vote result
- The vote results are being showcased using the result service

