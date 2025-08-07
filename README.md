# Shopify → Home Assistant → Zebra Printer Integration

Este proyecto documenta cómo integrar Shopify con Home Assistant para imprimir automáticamente etiquetas en una impresora Zebra al recibir un nuevo pedido.

## 🧩 Tecnologías utilizadas

- **Shopify** (webhook de pedidos) 
- **Home Assistant instalado en Raspberry PI** (automatización local)
- **Impresora Zebra ZD421** Conectada a la red y con IP fija para evitar desconexiones recurrentes.

---

## 📐 Estructura general del flujo

1. **Shopify** genera un webhook al recibir un nuevo pedido.
2. El webhook llega a Home Assistant a través de un endpoint.
3. Home Assistant recibe los datos, genera una etiqueta en formato ZPL.
4. La etiqueta se envía a la impresora Zebra vía `shell_command`.

---

## 📁 Estructura del repositorio

├── README.md
├── home_assistant/
│ ├── automation.yaml
│ ├── shell_command.yaml
│ └── configuration.yaml

**TIP EXTRA**

- Para conocer en tiempo real el estado de conexion de la impresora al homeassistant, configura la integracion nativa "PING" con la IP de la impresora. 


