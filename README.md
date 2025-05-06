# reto_EFK

En este reto se busca una integracion que permita recolectar, almacenar y visualizar logs de aplicaciones usando Kubernetes, Fluentd, Elasticsearch y Kibana.

## Requisitos

- Kubernetes (MicroK8s recomendado)
- Docker
- `kubectl` configurado

## Pasos para desplegar el stack

### 1. Ejecutar el archivo `namespace.yaml`

Para crear el espacio de nombres y los recursos necesarios en Kubernetes, ejecuta el siguiente comando:

```bash
microk8s kubectl apply -f namespace.yaml
```

Una vez ejecutado el comando, debes esperar unos minutos para que los pods se desplieguen y estén en funcionamiento. Puedes verificar el estado de los pods usando:

```bash
microk8s kubectl get pods -n logging
```
## 2. Visualizacion con kibana

Para ver los logs en Kibana, sigue estos pasos:

#### 1. Accede a Kibana en tu navegador usando el siguiente enlace

```bash
http://<NODE_IP>:30002
```
donde <NODE_IP> sera reemplazado por cualquiera de las maquina virtuales de tu cluster, en nuestro caso un ejemplo seria
```bash
http://10.6.101.97:30002
```
#### 2. En la interfaz de Kibana, ve a la sección de "Discover" y selecciona el índice de logs. Puedes usar un índice como logstash-* o el que hayas configurado en Fluentd.

#### 3. Ajusta los filtros y las visualizaciones de acuerdo a tus necesidades.



