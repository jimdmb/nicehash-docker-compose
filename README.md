NiceHash CPU Mining Docker
==================================

It's a lab project to learn docker and docker-compose.
It use the miner from nicehash : https://github.com/nicehash/nheqminer


Install docker and docker-compose on Linux
==================================

Ubuntu/debian :

        sudo apt install docker.io docker-compose

Deploying the dockers
======================

Start two nodes with docker-compose :

	docker-compose up -d --scale wrk0=2


Start one node with docker command :

	docker run -d --rm -e THREAD=1 -e NH_REGION=eu jimjace/miner:latest
	
N.B.: see the .env file for the others variables name to parse with -e


Usefull commands
====================

Decommission dockers:

	docker-compose down

Remove builded images:

	docker image prune

Really remove all images:

	docker image prune -a


Logs
=======

	docker-compose logs -f --tail=30

Variables
===========

Variables are in the .env file.

