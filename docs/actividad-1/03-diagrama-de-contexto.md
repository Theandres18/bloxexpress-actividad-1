# 03. Diagrama de contexto del sistema

Muestra a BloxExpress como una caja única, los usuarios y sistemas externos que interactúan con ella, los flujos de información y el límite del sistema.

![Diagrama de contexto de BloxExpress](diagrama-contexto.png)

*Versión editable del mismo diagrama (Mermaid, GitHub la renderiza automáticamente):*

```mermaid
flowchart LR
    subgraph USUARIOS[Usuarios]
        CLI([Cliente: jugador o familia])
        OPE([Operador de tienda])
        ALM([Administrador de almacén])
        REP([Repartidor])
        SOP([Soporte al cliente])
    end

    subgraph LIMITE[Límite del sistema]
        SYS[["BloxExpress<br/>Gestión logística de última milla<br/>(pedidos, inventario, rutas, tracking, incidencias)"]]
    end

    subgraph EXT[Sistemas externos]
        CAN[Canales de venta: web, app, Discord, redes, marketplaces]
        PAG[Sistema de pagos]
        GEO[Servicio de geolocalización]
        NOT[Sistema de notificaciones]
        ERP[ERP / CRM interno]
    end

    CLI -->|Pedido, consulta, reclamo| SYS
    SYS -->|Estado y hora estimada| CLI
    OPE -->|Registra y valida pedidos| SYS
    SYS -->|Pedidos y stock local| OPE
    ALM -->|Inventario y asignación de rutas| SYS
    SYS -->|Pedidos por preparar, alertas de stock| ALM
    SYS -->|Ruta y pedidos asignados| REP
    REP -->|Estado de entrega, evidencia, incidencias| SYS
    SOP -->|Consulta trazabilidad, gestiona incidencias| SYS
    SYS -->|Historial del pedido| SOP

    CAN -->|Pedidos entrantes| SYS
    SYS -->|Estado del pedido| CAN
    SYS -->|Cobro o reembolso| PAG
    PAG -->|Pago confirmado o rechazado| SYS
    SYS -->|Direcciones y solicitud de rutas| GEO
    GEO -->|Coordenadas y rutas| SYS
    SYS -->|Eventos de cambio de estado| NOT
    SYS <-->|Clientes, productos, stock, facturación| ERP
```

## Flujos principales
1. **Pedido:** canal de venta u operador → sistema (valida inventario y pago).
2. **Preparación:** sistema → almacén (pedido por preparar) → sistema (listo para despacho).
3. **Entrega:** sistema → repartidor (ruta) → sistema (estado y evidencia).
4. **Información al cliente:** sistema → notificaciones → cliente.
5. **Incidencias:** cliente, repartidor o soporte → sistema (registro y seguimiento).

## Límites del sistema
- **Dentro:** registro de pedidos, validación de inventario, asignación de rutas, tracking e incidencias.
- **Fuera:** cobro real (pagos), mapas y cálculo de rutas (geolocalización), envío de mensajes (notificaciones), contabilidad y datos maestros (ERP/CRM), y la venta en sí misma (canales).
