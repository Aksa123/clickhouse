docker run -d -p 8123:8123 -p 9000:9000 --name clickhouse-server --ulimit nofile=262144:262144 \
-v ./volume/ch_data:/var/lib/clickhouse/ \
-v ./volume/ch_logs:/var/log/clickhouse-server/ \
-e CLICKHOUSE_DB=zero -e CLICKHOUSE_DEFAULT_ACCESS_MANAGEMENT=1 -e CLICKHOUSE_USER=zero -e CLICKHOUSE_PASSWORD=zero123 \
--network peerdb_network \
 clickhouse/clickhouse-server


 -v /path/to/your/config.xml:/etc/clickhouse-server/config.xml \
