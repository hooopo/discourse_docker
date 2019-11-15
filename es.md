sudo sysctl -w vm.max_map_count=262144
mkdir -p data
docker run -d --rm --name es -p 9200:9200 -p 9300:9300 -v $(pwd)/data:/usr/share/elasticsearch/data peterzhang/elasticsearch-analysis-ik
