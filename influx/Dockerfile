FROM influxdb:2.6.0

RUN BUCKET_ID=$(influx bucket list | awk '{if($2=="IIoTSuite")print $1}') \
    influx v1 auth create --username $(V1_USERNAME) --password $(V1_PASSWORD) --read-bucket $BUCKET_ID --write-bucket $BUCKET_ID