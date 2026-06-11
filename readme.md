# EJERCICIO LAB 

Se desarrollo la actividad de laboratorio del dia miercoles.


## COMANDOS
```bash
SIRVE PARA MONTAR LAS IMAGENES:

docker compose up -d --build

PARA RESETEAR TODO:

docker compose down -v   # borra también dashboards/alarmas creados
```

## Servicios y URLs
| Servicio       | URL                         | Notas                                  |
|----------------|-----------------------------|----------------------------------------|
| Frontend       | http://localhost:8080       | Hello World + botones de tráfico/carga |
| Backend (API)  | http://localhost:3001       | `/api/hello`, `/metrics`, `/load`      |
| Grafana        | http://localhost:3000       | admin / admin                          |
| Prometheus     | http://localhost:9090       | datasource ya provisionado             |
| Loki           | http://localhost:3100       | datasource ya provisionado             |
| Alloy (UI)     | http://localhost:12345      | estado del recolector de logs          |
| cAdvisor       | http://localhost:8081       | métricas por contenedor                |
| node-exporter  | http://localhost:9100/metrics | métricas del host                    |

## Configuraciones
- **Datasources** Prometheus y Loki (provisionados automáticamente).
- Logs etiquetados por Alloy con `tier=application` o `tier=infrastructure`.

## ADVERTENCIA

- Este docker compose tiene una pequeña variacion con el docker compose original del repo, se comentaron las lineas 48-49 para evitar problemas de permisos con el montaje de todo el host
