# pinot_minion_minio
basic setup for batch ingest data from minio to pinot using minions




docker run \
   --network json \
   -v $PWD/config:/config \
   apachepinot/pinot:1.2.0 AddTable \
     -tableConfigFile /config/table.json   \
     -schemaFile /config/schema.json \
     -controllerHost "pinot-controller-json" \
    -exec



curl -X POST "http://localhost:9000/tasks/schedule?taskType=SegmentGenerationAndPushTask&tableName=movies_OFFLINE"   -H "accept: application/json"

apart from commands (docker / curl )swagger ui can also be used for adding schema, table and minion task scheduling