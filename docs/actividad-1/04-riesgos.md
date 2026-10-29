# 04. Registro de riesgos

Escala: Probabilidad (P) e Impacto (I) en Alta (A), Media (M) o Baja (B).

| ID | Riesgo | Causa probable | P | I | Consecuencia | Mitigación inicial (idea, no diseño final) |
|---|---|---|---|---|---|---|
| R1 | Duplicación de pedidos | El mismo pedido entra por Discord y por la web, o se reintenta un pago | A | A | Doble despacho y costos extra | Identificador único y reglas de deduplicación |
| R2 | Inconsistencias de inventario | Inventarios distribuidos con actualización tardía; ediciones limitadas | A | A | Ventas sin stock y cancelaciones | Fuente única de inventario y sincronización frecuente |
| R3 | Entregas fallidas o retrasadas | Mala asignación de rutas, direcciones erróneas, nadie en casa | A | A | Clientes insatisfechos y reentregas | Seguimiento de estado y gestión de incidencias |
| R4 | Pérdida de trazabilidad | Datos dispersos y estados sin registrar | M | A | No se sabe dónde está un pedido | Historial de eventos por pedido |
| R5 | Mala coordinación almacén, rutas y soporte | Cada área usa su propia información | A | M | Errores operativos y reprocesos | Vista compartida del estado del pedido |
| R6 | Crecimiento operativo sin control | Picos por lanzamientos, eventos de la comunidad y temporada alta | M | A | Colapso operativo cuando más se vende | Definir requisitos de escalabilidad antes de diseñar |
| R7 | Seguridad y datos de menores | Muchos clientes son menores y se manejan datos personales y de ubicación | M | A | Sanciones y pérdida de confianza | Control de acceso, autorización de acudientes y protección de datos desde el inicio |
| R8 | Dependencia de sistemas externos | Caída de pagos, geolocalización, notificaciones o ERP/CRM | M | A | Operación detenida | Identificar puntos de falla y alternativas |
| R9 | Fraude y suplantación | Pedidos falsos, estafas con tarjetas de regalo físicas, entregas a quien no es | M | M | Pérdidas económicas y reclamos | Validar pedidos y confirmar entrega con evidencia |
| R10 | Mala experiencia de usuario | Interfaces confusas para repartidores o clientes | M | M | Baja adopción y errores de captura | Validar con usuarios reales más adelante |
| R11 | Alcance sin control del proyecto | Intentar resolver todo desde el inicio | M | M | Entregas incompletas | Delimitar alcance por fases |
