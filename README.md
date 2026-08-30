# DeliveryBot – Gestión de Pedidos Internos de Cafetería.

DeliveryBot es una solución de automatización desarrollada en **n8n** que transforma Telegram en una terminal de pedidos interactiva e inteligente para entornos institucionales.

## 🚀 Funcionalidades Principales:
* **Menú Digital Interactivo:** Consulta de catálogo organizado por categorías.
* **Gestión de Pedidos:** Selección de productos, cálculo de totales y generación de ID de orden.
* **Persistencia en la Nube:** Registro automatizado de datos y transacciones en Google Sheets.
* **Notificaciones Push:** Confirmaciones instantáneas al usuario vía Telegram.

## 🛠️ Arquitectura del Sistema:
* **Telegram Bot API:** Interfaz conversacional.
* **n8n:** Motor de flujos de trabajo, validación y enrutamiento con nodos Switch.
* **Google Sheets:** Base de datos relacional simplificada.

## 📊 Estructura de la Base de Datos (`DeliveryBot_DB`)
* `MENU`: id_producto, nombre, descripcion, precio, categoria, stock.
* `SESSIONS`: telegram_id, pantalla_actual, carrito_temporal, ultimo_cambio.
* `USUARIOS`: telegram_id, nombre_completo, departamento_oficina, puntos_lealtad.
* `PEDIDOS`: id_pedido, id_usuario, detalles_pedido, total_pago, estado, fecha, hora.

🔗 **[Enlace a la Base de Datos Google Sheets](https://docs.google.com/spreadsheets/d/1O1_bP95YgChjqCCPe8lchl7y9TuEf0NwLwXINWd6Ds8/edit?usp=sharing)**

## 📦 Contenido del Repositorio
* `workflow.json`: Flujo completo de n8n.
* `README.md`: Documentación del proyecto.
