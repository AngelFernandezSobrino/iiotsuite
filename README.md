# iiotsuite


To create a new independent telegraf agent add a new service on docker-compose.yml, like the telegraf service, with a new name. Create another .env-"newfilename" file, with the INFLUX_TOKEN value shown by the new configuration created at influx and update the services url to point the version of the new configuratio.

Its recomended to update previous configuration with new features than creating a new one. You can also add a new plugin just update the configuration file and restart the telegraf service.

Create .env file with

```bash
DOMAIN=10.1.0.1
GRAFANA_ROOT = http://127.0.0.1:3000/
GRAFANA_SUBPATH = true

PROXY_PORT=1890
INFLUX_PORT=1891
INFLUX_CONFIG_TOKEN=asdf
INFLUX_CONFIG_ID=asdf
DOCKER_INFLUXDB_INIT_MODE=setup
DOCKER_INFLUXDB_INIT_USERNAME=admin
DOCKER_INFLUXDB_INIT_PASSWORD=supersecretpassword
DOCKER_INFLUXDB_INIT_ORG=IIoTSuite
DOCKER_INFLUXDB_INIT_BUCKET=IIoTSuite

V1_USERNAME=admin
V1_PASSWORD=123456768
```