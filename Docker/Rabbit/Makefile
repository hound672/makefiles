# Make file for Postgresql server
# and psql client

.PHONY: run
run:
	echo "Start Rabbit server"
	docker run --rm -it --name rabbit-docker -v ~/Projects/Docker/Rabbit/home:/var/lib/rabbitmq -v ~/Projects/Docker/Rabbit/config:/etc/rabbitmq/rabbitmq.config  -p 5672:5672 rabbitmq:3.8

.PHONY: bash
bash:
	docker exec -it rabbit-docker bash

