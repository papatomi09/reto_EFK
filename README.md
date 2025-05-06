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

