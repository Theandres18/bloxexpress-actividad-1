# BloxExpress — Plataforma de logística de última milla para BloxShop

> **Actividad 1: Diagnóstico y contexto arquitectónico**
> Proyecto académico y ficticio. Está inspirado en la comunidad de Roblox y no está afiliado a Roblox Corporation.

## Resumen ejecutivo

**Producto:** BloxExpress, plataforma centralizada para gestionar la logística de última milla de **BloxShop**, una empresa de retail digital (ficticia) que vende productos físicos temáticos de Roblox: peluches, figuras, ropa, accesorios gamer y tarjetas de regalo físicas.

**Problema principal:** BloxShop recibe pedidos desde varios canales (tienda web, app móvil, servidor de Discord, redes sociales y marketplaces), maneja inventarios distribuidos en varios puntos y coordina entregas con distintas rutas y repartidores. Sin embargo, no tiene una vista centralizada del estado real de cada pedido. Esto causa información duplicada, retrasos, errores operativos y poca trazabilidad. Los jugadores y sus familias no saben cuándo llegará su pedido, y el operador no puede gestionar las entregas con información confiable. El problema se agrava en los lanzamientos y eventos de la comunidad, cuando la demanda se dispara.

**Usuarios:** cliente (jugador o familia), operador de tienda, administrador de almacén, repartidor y soporte al cliente.

**Sistemas externos:** sistema de pagos, servicio de geolocalización, sistema de notificaciones, ERP/CRM interno y canales de venta (web, app, Discord, redes y marketplaces).

**Objetivos:**
1. Tener una única fuente de verdad sobre el estado de cada pedido.
2. Evitar pedidos duplicados e inconsistencias de inventario, sobre todo en ediciones limitadas.
3. Reducir entregas fallidas o retrasadas con asignación y seguimiento de rutas.
4. Dar trazabilidad de extremo a extremo, desde el pedido hasta la entrega.
5. Gestionar incidencias desde un solo lugar.

**Alcance de esta actividad:** formular el problema, identificar actores, delimitar los límites del sistema, riesgos, supuestos y decisiones iniciales. **No** incluye diseño detallado, elección de tecnologías ni código.

## Contenido del repositorio

| Documento | Descripción |
|---|---|
| [01-analisis-del-problema](docs/actividad-1/01-analisis-del-problema.md) | Qué ocurre hoy, por qué es un problema, consecuencias y variables |
| [02-actores-y-alcance](docs/actividad-1/02-actores-y-alcance.md) | Actores, alcance, fuera de alcance y restricciones |
| [03-diagrama-de-contexto](docs/actividad-1/03-diagrama-de-contexto.md) | Diagrama de contexto del sistema |
| [04-riesgos](docs/actividad-1/04-riesgos.md) | Registro de riesgos |
| [05-supuestos-y-decisiones](docs/actividad-1/05-supuestos-y-decisiones.md) | Supuestos, decisiones iniciales y pendientes por confirmar |
| [06-guion-video](docs/actividad-1/06-guion-video.md) | Guion del video de sustentación |

## Video de sustentación

[Ver video en YouTube](https://youtu.be/XhE7qe8llr4?si=pzamFv4HHOkEKNE9)

## Autor

Andres Felipe Barrera Claros, 650202019-1 OPTATIVA II-VIRTUAL 2026-2, Actividad 1. Diagnóstico y contexto arquitectónico — 25% 
