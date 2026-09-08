# Requerimientos no funcionales

| # | Atributo | Metrica | Umbral | Condicion de carga | Verificacion | Consecuencia si no se cumple |
|---|---|---|---|---|---|---|
| 1 | Rendimiento | p95 de latencia | menor a 400 ms | 200 usuarios concurrentes | Prueba de carga | El usuario abandona la operacion |
| 2 | Disponibilidad | Tiempo de actividad | mayor a 99.5% mensual | Operacion continua | Monitoreo de uptime | El servicio queda inaccesible para los usuarios |
| 3 | Seguridad | Autenticacion requerida | 100% de los endpoints protegidos | Cualquier solicitud a la API | Revision de codigo y pruebas de acceso | Datos expuestos a usuarios no autorizados |

## Escenarios completos

### Escenario 1
-Fuente: Usuario autenticado
-Estimulo: Realiza una solicitud a la aplicacion en horario pico
-Artefacto: Servidor de aplicacion / base de datos
-Entorno: Operacion normal, 200 usuarios concurrentes
-Respuesta: El sistema procesa la solicitud y responde
-Medida: p95 de latencia menor a 400 ms
