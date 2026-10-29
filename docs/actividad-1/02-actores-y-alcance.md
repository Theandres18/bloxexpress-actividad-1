# 02. Actores, alcance y restricciones

## Actores
| Actor | Tipo | Qué necesita del sistema |
|---|---|---|
| Cliente (jugador o familia) | Usuario | Hacer pedidos, ver estado y hora estimada, recibir avisos, reportar problemas |
| Operador de comercio o tienda | Usuario | Registrar y consultar pedidos, validar inventario local, preparar despachos |
| Administrador de almacén | Usuario | Controlar inventario, preparación y salida de pedidos, asignar rutas |
| Repartidor | Usuario | Ver ruta y pedidos asignados, actualizar estado de entrega, reportar incidencias |
| Soporte al cliente | Usuario | Consultar trazabilidad, gestionar incidencias y reclamos |
| Canales de venta (web, app, Discord, redes, marketplaces) | Externo | Enviar pedidos al sistema y recibir su estado |
| Sistema de pagos | Externo | Confirmar o rechazar pagos y reembolsos |
| Servicio de geolocalización | Externo | Direcciones, rutas y ubicación en tiempo real |
| Sistema de notificaciones | Externo | Enviar avisos (WhatsApp, SMS, correo, push) |
| ERP / CRM interno | Externo | Intercambiar datos de clientes, productos, facturación e inventario maestro |

## Alcance (dentro del sistema)
- Registro y consolidación de pedidos de todos los canales.
- Validación de inventario distribuido, incluyendo productos de edición limitada.
- Asignación de rutas y repartidores.
- Seguimiento (tracking) del estado de cada pedido.
- Gestión de incidencias: entregas fallidas, retrasos y reclamos.
- Notificaciones al cliente sobre cambios de estado.

## Fuera de alcance (por ahora)
- Diseño técnico final, arquitectura interna y elección de tecnologías.
- Implementación de código.
- Entrega de productos digitales dentro de Roblox (Robux, ítems virtuales). Este proyecto solo cubre productos físicos.
- Integración con la plataforma o API de Roblox: Roblox es solo el tema del negocio.
- Optimización avanzada de rutas con algoritmos y analítica predictiva.
- Procesamiento interno de pagos (lo hace el sistema de pagos externo).
- Reemplazo del ERP/CRM: el sistema se integra con ellos.

## Restricciones (a confirmar)
- La plataforma debe integrarse con el ERP/CRM existente y con los servicios externos listados.
- Los datos de clientes y ubicación requieren protección de datos personales (en Colombia, Ley 1581 de 2012). Como muchos jugadores son menores, el tratamiento de sus datos exige autorización de sus representantes legales.
- Los repartidores probablemente usan celular con conectividad variable.
- Tiempo y recursos limitados del curso: el objetivo es formular el problema, no resolverlo.
