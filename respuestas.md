1. ¿Por qué necesitamos Loki además de Prometheus si ya tenemos `/metrics`?
    - Porquie prometheus recolecta metricas numericas , loki recolecta logs, son complementarios, sin loki tendriamos que entrar manualmente a cada contenedor para revisar.
2. ¿Qué ventaja aporta que las fuentes de datos de Grafana estén aprovisionadas como código y no creadas a mano?
    - creo que las mayores ventajas que aporta es la consistencia y la reproducibilidad , osea no hay riesgo que nos olvidemos de crear un datasource.
3. El panel "CPU contenedor" y el panel "CPU host" pueden mostrar valores muy distintos. ¿Por qué? ¿Cuál usarías para alertar sobre una aplicación concreta?
    - el cpu host mide el uso total de la maquina y el cpu contenedor solo el uso de este mismo , para alertar sobre una aplicacion concreta utilizairamos el cpu contenedor
4. ¿Qué diferencia hay entre el *evaluation interval* y el *pending period* de una alarma?
    - la diferencia es que evaluation interval mide  cada cuánto tiempo Grafana evalúa la condición de la alerta y pending period mid cuánto tiempo la condición debe mantenerse activa antes de disparar la alerta