# Make file for Postgresql server
# and psql client

.PHONY: run
run:
	echo "Start Psql server"
	docker run --rm -it --name pg-docker -v ~/Projects/Docker/Psql/postgres-data:/var/lib/postgresql/data postgres:11

.PHONY: psql
psql:
	docker exec -it pg-docker psql -U postgres

.PHONY: bash
bash:
	docker exec -it pg-docker bash

