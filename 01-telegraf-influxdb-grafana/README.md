## Telegraf InlfuxDB y Grafana 

Un ejemplo simple para probar Grafana con telegraf y influxdb.

### Ejecucion 

Después de clonar el proyecto:

`git clone https://github.com/thecookieproject/docker.git`


```
cd 01-telegraf-influxdb-grafana
mkdir {grafana,data}
docker-compose up 
```
### Diretorios 

* grafana : Almacena las configuraciones localmente 
* data    : Almacena los datos de influxdb 

### Grafana dashboards 

 http://localhost:3000

 En primera instancia se debe configurar un nuevo datasource --> http://influxdb:8086.
 Importar el dashboard ID: 11912.