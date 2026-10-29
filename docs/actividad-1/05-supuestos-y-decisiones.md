# 05. Supuestos y registro de decisiones iniciales

## Supuestos
- A1. BloxShop ya opera con varios canales de venta y varios puntos de inventario.
- A2. Existe un ERP/CRM interno que sigue siendo la fuente de datos maestros (clientes, productos, facturación).
- A3. Los pagos, mapas y notificaciones se consumen como servicios externos, no se construyen.
- A4. Los repartidores pueden usar un celular durante la entrega.
- A5. El volumen de pedidos va a crecer y tendrá picos fuertes en lanzamientos y fechas especiales.
- A6. Una parte importante de los clientes son menores de edad que compran con acudientes.
- A7. Se debe cumplir la normativa de protección de datos personales aplicable.
- A8. Solo se venden productos físicos; los productos digitales de Roblox quedan fuera.

## Registro de decisiones iniciales (ADR simplificado)

| ID | Decisión | Justificación | Alternativa descartada | Estado |
|---|---|---|---|---|
| D1 | Construir una plataforma **centralizada** para pedidos, inventario, rutas, tracking e incidencias | Resuelve la fragmentación de información, que es la causa raíz | Mantener sistemas separados por área | Aceptada |
| D2 | Integrar (no reemplazar) el ERP/CRM | Reduce riesgo y costo y respeta los datos maestros existentes | Sustituir el ERP/CRM | Aceptada |
| D3 | Delegar pagos, geolocalización y notificaciones a servicios externos | No son el núcleo del negocio y ya existen soluciones | Desarrollarlos internamente | Aceptada |
| D4 | No elegir tecnologías, frameworks ni estilo arquitectónico en esta etapa | La actividad pide comprender el problema primero | Escoger el stack desde el inicio | Aceptada |
| D5 | Priorizar la trazabilidad del pedido como capacidad central | Es la principal carencia actual | Priorizar la optimización de rutas | Aceptada |
| D6 | Entregar el sistema por fases | Controla el riesgo de crecimiento sin control | Construir todo de una vez | Aceptada |
| D7 | Roblox es el contexto del negocio, no una integración técnica; solo se cubren productos físicos | Mantiene el alcance acotado a la última milla | Integrar con la API de Roblox o entregar ítems digitales | Aceptada |

## Lo que aún no sabemos
- Volumen real de pedidos por día y tamaño de los picos en lanzamientos.
- Cantidad de canales, almacenes, tiendas y repartidores.
- Si los repartidores son propios o de terceros.
- Qué APIs ofrecen el ERP/CRM y los servicios externos.
- Tiempos de entrega prometidos (SLA) y metas de negocio.
- Presupuesto, plazos y equipo disponible.

## Por confirmar más adelante
- Requisitos no funcionales (disponibilidad, rendimiento, seguridad).
- Modelo de datos del pedido y estados válidos.
- Cómo se manejan los datos de menores y la autorización de acudientes.
- Estrategia de integración con sistemas externos.
- Estilo arquitectónico y tecnologías (actividades siguientes).
