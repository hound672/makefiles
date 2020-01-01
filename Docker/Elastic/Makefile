# Make file for Postgresql server
# and psql client

.PHONY: run
run:
	echo "Start Elastic server"
	docker run -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" -e "xpack.ml.enabled=false" docker.elastic.co/elasticsearch/elasticsearch:7.5.1

