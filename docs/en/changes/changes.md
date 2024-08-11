## 10.1.0

#### Project

* E2E: bump up the version of the opentelemetry-collector to 0.102.1.
* Push snapshot data-generator docker image to ghcr.io.
* Bump up skywalking-infra-e2e to work around GHA removing `docker-compose` v1.

#### OAP Server

* Fix wrong indices in the eBPF Profiling related models.
* Support exclude the specific namespaces traffic in the eBPF Access Log receiver.
* Add Golang as a supported language for Elasticsearch.
* Remove unnecessary BanyanDB flushing logs(info).
* Increase `SW_CORE_GRPC_MAX_MESSAGE_SIZE` to 50MB.
* Support to query relation metrics through PromQL.
* Support trace MQE query for debugging.
* Add Component ID(158) for the Solon framework.
* Fix metrics tag in HTTP handler of browser receiver plugin.
* Increase `alarm_record#message` column length to 2000 from 200.
* Remove `alarm_record#message` column indexing.
* Add Python as a supported language for Pulsar.
* Make more proper histogram buckets for the `persistence_timer_bulk_prepare_latency`,
  `persistence_timer_bulk_execute_latency` and `persistence_timer_bulk_all_latency` metrics in PersistenceTimer.
* [Break Change] Update Nacos version to 2.3.2. Nacos 1.x server can't serve as cluster coordinator and configuration server.
* Support tracing trace query(SkyWalking and Zipkin) for debugging.
* Fix BanyanDB metrics query: used the wrong `Downsampling` type to find the schema.
* Support fetch cilium flow to monitoring network traffic between cilium services.
* Support `labelCount` function in the OAL engine.
* Support BanyanDB internal measure query execution tracing.
* BanyanDB client config: rise the default `maxBulkSize` to 10000, add `flushTimeout` and set default to 10s.
* Polish BanyanDB group and schema creation logic to fix the schema creation failure issue in distributed race conditions.
* Support tracing topology query for debugging.
* Fix expression of graph `Current QPS` in MySQL dashboard.
* Support tracing logs query for debugging.
* BanyanDB: fix Tag autocomplete data storage and query.
* Support aggregation operators in PromQL query.
* Update the kubernetes HTTP latency related metrics source unit from `ns` to `ms`.
* Support BanyanDB internal stream query execution tracing.
* Fix Elasticsearch, MySQL, RabbitMQ dashboards typos and missing expressions.
* BanyanDB: Zipkin Module set service as Entity for improving the query performance.
* MQE: check the metrics value before do binary operation to improve robustness.
* Replace workaround with Armeria native supported context path.
* Add an http endpoint wrapper for health check.
* Bump up Armeria and transitive dependencies.
* BanyanDB: if the model column is already a `@BanyanDB.TimestampColumn`, set `@BanyanDB.NoIndexing` on it to reduce indexes.
* BanyanDB: stream sort-by `time` query, use internal time-series rather than `index` to improve the query performance.
* Bump up graphql-java to 21.5.
* Add Unknown Node when receive Kubernetes peer address is not aware in current cluster.
* Fix CounterWindow concurrent increase cause NPE by PriorityQueue
* Fix format the endpoint name with empty string.
* Add Datadog java agent tracing support as a Zipkin trace input

#### UI

* Highlight search log keywords.
* Add Error URL in the browser log.
* Add a SolonMVC icon.
* Adding cilium icon and i18n for menu.
* Fix the mismatch between the unit and calculation of the "Network Bandwidth Usage" widget in Windows-Service Dashboard.
* Make a maximum 20 entities per query in service/instance/endpoint list widgets.
* Polish error nodes in trace widget.

#### Documentation

* Update the version description supported by zabbix receiver.
* Move the Official Dashboard docs to marketplace docs.
* Add marketplace introduction docs under `quick start` menu to reduce the confusion of finding feature docs.
* Update Windows Metrics(Swap -> Virtual Memory)

All issues and pull requests are [here](https://github.com/apache/skywalking/milestone/205?closed=1)
