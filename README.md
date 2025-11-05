# pinot_minion_minio
##Basic setup for batch ingest data from minio to pinot using minions

- Add schema and table configs  to pinot with relevant properties of minio  with docker /curl command or thru pinot swagger ui
- Data dump (json/csv etc ) should be available in minio bucket.
- kick off the  MINION job i.e SegmentGenerationAndPushTask thru available apis in swagger ui / curl cmnds 
  eg:curl -X POST "http://localhost:9000/tasks/schedule?taskType=SegmentGenerationAndPushTask&tableName=movies_OFFLINE"   -H "accept: application/json"
- minion batch ingestion scheduling can be ither manual or automatic change the configuaratons as per the requirements
