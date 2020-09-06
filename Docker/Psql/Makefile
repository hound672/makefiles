# Make file for Postgresql server
# and psql client

VOLUME_NAME := 
POSTGRES_PASS := 
POSTGRES_USER := 
POSTGRES_DB := 
CONTAINER_NAME := 

.PHONY: run
run:
	echo "Start Psql server: ".$(VOLUME_NAME)
	docker run --rm -it --name $(CONTAINER_NAME) -e POSTGRES_USER=$(POSTGRES_USER) -e POSTGRES_PASSWORD=$(POSTGRES_PASS) -e POSTGRES_DB=$(POSTGRES_DB) \
	    -p 5432:5432 -v test_psql:/var/lib/postgresql/data postgres:11

.PHONY: psql
psql:
	docker exec -it $(CONTAINER_NAME) psql -U $(POSTGRES_USER) -d $(POSTGRES_DB)

.PHONY: bash
bash:
	docker exec -it $(CONTAINER_NAME) bash
