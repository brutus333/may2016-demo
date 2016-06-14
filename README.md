Example Voting App
==================

This is an example Docker app with multiple services. 

It is run with Rancher compose.

Architecture
-----

* A Python webapp which lets you vote between two options
* A Redis queue which collects new votes
* A Java worker which consumes votes and stores them in…
* A Postgres database backed by a Docker volume
* A Node.js webapp which shows the results of the voting in real time

Running
-------

Run in this directory:

    $ rancher-compose up

The voting app will be running behind a load balancer started on port 5000 while the result app will be running on host port 5001.

Docker Hub images
-----------------

Docker Hub images for services in this app are built automatically from master:

 - [brutus333/voting-app](https://hub.docker.com/r/brutus333/voting-app/)
 - [brutus333/result-app](https://hub.docker.com/r/brutus333/result-app/)
 - [brutus333/voting-worker](https://hub.docker.com/r/brutus333/voting-worker/)
