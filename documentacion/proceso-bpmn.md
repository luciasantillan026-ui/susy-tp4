Modelado de Procesos de Negocio (BPMN)

Proceso: Reposición de stock – Supermercado Susy

Objetivo
Representar el proceso de reposición de stock del Supermercado Susy, desde el registro de una venta y la detección de un nivel mínimo de inventario hasta la solicitud de mercadería al proveedor, su recepción y la actualización del stock disponible.

Participantes
El proceso se organiza en tres Pools:

- Cliente: realiza la compra de productos y recibe el comprobante.
- Supermercado Susy: desarrolla las actividades internas mediante las siguientes Lanes:
  -Cajero: registra y cobra las ventas.
  -Sistema de Gestión de Stock: descuenta las unidades vendidas, controla los niveles de inventario, genera alertas y actualiza las cantidades.
  -Depósito y Control de Stock: recibe y verifica la mercadería.
  -Compras y Proveedores: revisa las alertas, define los pedidos y se comunica con los proveedores.

- Proveedor: recibe los pedidos, verifica la disponibilidad y realiza la entrega de mercadería.

Descripción del proceso
- El cliente realiza una compra y el cajero registra y cobra la venta.
- El sistema descuenta del inventario las unidades vendidas.
- Se compara el stock actual con el nivel mínimo establecido.
- Si el stock no está por debajo del mínimo, finaliza el proceso de venta sin generar una alerta.
- Si el stock está por debajo del mínimo, el sistema genera una alerta de reposición.
- El área de Compras revisa la alerta, define el pedido y lo envía al proveedor.
- El proveedor verifica la disponibilidad de los productos y comunica su respuesta.
- Si el pedido no puede confirmarse, Compras busca un proveedor alternativo.
- Si el pedido se confirma, el proveedor prepara y envía la mercadería.
- Depósito recibe y controla los productos y las cantidades entregadas.
- Si la mercadería no es conforme, se realiza un reclamo al proveedor.
- Si la mercadería es conforme, se registra el ingreso.
- El sistema actualiza las cantidades disponibles y finaliza el proceso.

Decisiones y excepciones
El proceso contempla tres decisiones principales:
- Control del stock mínimo: determina si es necesario generar una alerta de reposición.
- Confirmación del pedido: permite buscar un proveedor alternativo cuando no se confirma la disponibilidad.
- Conformidad de la mercadería: permite registrar el ingreso o realizar un reclamo al proveedor.

Datos involucrados
El proceso utiliza las entidades Producto, Proveedor, Movimiento de stock y Usuario, definidas en el diccionario de datos del proyecto.

Automatización del sistema
El Sistema de Gestión de Stock automatiza el descuento de las unidades vendidas, la comparación con el stock mínimo, la generación de alertas de reposición y la actualización de las cantidades disponibles luego de registrar el ingreso de mercadería.
