# 01. Análisis del problema

## ¿Qué ocurre hoy?
- BloxShop recibe pedidos por **varios canales**: tienda web, app móvil, servidor de Discord, redes sociales y marketplaces. Cada canal guarda su propio registro.
- Los **inventarios están distribuidos** entre un almacén central y varias tiendas o puntos de despacho, y no siempre reflejan el stock real.
- Las **rutas y repartidores** se coordinan aparte de los pedidos y del inventario.
- No existe una **vista centralizada** del estado real de cada pedido: almacén, rutas y soporte tienen cada uno su versión.
- En **lanzamientos, eventos de la comunidad y temporadas altas** (vacaciones, Navidad) llegan muchos pedidos de golpe y los errores se multiplican.

## ¿Por qué es un problema?
- La información está **fragmentada y duplicada**, así que nadie puede confiar plenamente en ella.
- Un mismo pedido puede entrar por Discord y por la web, y despacharse dos veces.
- Se pueden vender productos de **edición limitada** que ya no existen en inventario.
- Almacén prepara sin saber de rutas y soporte responde sin saber el estado real.
- El cliente no sabe cuándo llegará su pedido, lo que genera incertidumbre y contactos innecesarios a soporte.
- Muchos clientes son menores de edad: las compras las hacen familias o acudientes, y una entrega fallida afecta la confianza de ambos.

## Consecuencias
| Ámbito | Consecuencia |
|---|---|
| Operativo | Pedidos duplicados, errores de despacho, entregas fallidas o tardías |
| Inventario | Ventas sin stock, sobrestock en un punto y faltantes en otro |
| Cliente | Mala experiencia, desconfianza, cancelaciones y reclamos |
| Soporte | Sobrecarga de consultas "¿dónde está mi pedido?" y resolución lenta |
| Negocio | Pérdidas por reprocesos y devoluciones, pérdida de clientes y crecimiento sin control |

## Variables que importan
- Volumen de pedidos por canal y por franja horaria, con picos en lanzamientos y fechas especiales.
- Disponibilidad de inventario por almacén o tienda y frecuencia de actualización.
- Stock de productos de edición limitada.
- Capacidad de repartidores y zonas de cobertura.
- Ventanas de entrega prometidas frente a las reales.
- Tasa de entregas fallidas y sus causas.
- Tiempo de respuesta de soporte e incidencias abiertas.
- Disponibilidad de los servicios externos (pagos, geolocalización, notificaciones, ERP/CRM).

## Formulación del problema
> Los jugadores y sus familias no saben cuándo llegará su pedido, y BloxShop no puede coordinar almacén, rutas y soporte porque no existe una vista centralizada y confiable del estado real de cada pedido. Esto genera duplicación de información, retrasos, errores operativos y poca trazabilidad, especialmente en los picos de demanda.
