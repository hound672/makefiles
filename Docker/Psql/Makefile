# Make file for Postgresql server
# and psql client

.PHONY: run
run:
	echo "Start Psql server"
	docker run --rm -it --name pg-docker -e POSTGRES_PASSWORD=psql -p 5432:5432 -v test_psql:/var/lib/postgresql/data postgres:11

.PHONY: psql
psql:
	docker exec -it pg-docker psql -U postgres

.PHONY: bash
bash:
	docker exec -it pg-docker bash

