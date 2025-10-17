# OpenSearch
export OPENSEARCH_INITIAL_ADMIN_PASSWORD="D0cker#OpenSearch"
docker-compose up -d

# find password:
docker inspect --format '{{range .Config.Env}}{{println .}}{{end}}' opensearch-single-node | grep OPENSEARCH_INITIAL_ADMIN_PASSWORD
